cmake_minimum_required (VERSION 3.9.0)

if (POLICY CMP0074)
  cmake_policy(SET CMP0074 NEW)
endif ()

project (Suhibd)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/Builds/CMake")
list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/Builds/CMake/deps")

include (CheckCXXCompilerFlag)
if (CMAKE_VERSION VERSION_GREATER_EQUAL 3.11)
  include (FetchContent)
endif ()
if (MSVC AND CMAKE_VERSION VERSION_LESS 3.12)
  message (FATAL_ERROR "MSVC requires cmake 3.12 or greater for proper boost support")
endif ()
include (ExternalProject)
include (CMakeFuncs) # must come *after* ExternalProject b/c it overrides one function in EP
include (ProcessorCount)
if (target)
  message (FATAL_ERROR "The target option has been removed - use native cmake options to control build")
endif ()

include(SuhibdSanity)
include(SuhibdVersion)
include(SuhibdSettings)
include(SuhibdNIH)
include(SuhibdRelease)
# this check has to remain in the top-level cmake
# because of the early return statement
if (packages_only)
  if (NOT TARGET rpm)
    message (FATAL_ERROR "packages_only requested, but targets were not created - is docker installed?")
  endif()
  return ()
endif ()
include(SuhibdCompiler)
include(SuhibdInterface)

###

include(deps/Boost)
include(deps/OpenSSL)
include(deps/Secp256k1)
include(deps/Ed25519-donna)
include(deps/Lz4)
include(deps/Libarchive)
include(deps/Sqlite)
include(deps/Soci)
include(deps/Snappy)
include(deps/Rocksdb)
include(deps/Nudb)
include(deps/date)
include(deps/Protobuf)
include(deps/gRPC)
include(deps/cassandra)
include(deps/Postgres)

###

include(SuhibdCore)
include(SuhibdInstall)
include(SuhibdCov)
include(SuhibdMultiConfig)
include(SuhibdDocs)
include(SuhibdValidatorKeys)
