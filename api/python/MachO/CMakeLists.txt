set(LIEF_PYTHON_MACHO_SRC
  "${CMAKE_CURRENT_LIST_DIR}/pyMachO.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyDylibCommand.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyBinary.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyLoadCommand.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pySegmentCommand.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyHeader.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pySection.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyParser.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pySymbol.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyUUID.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyMainCommand.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/objects/pyDylinker.cpp"
  "${CMAKE_CURRENT_LIST_DIR}/pyMachOStructures.cpp")

set(LIEF_PYTHON_MACHO_HDR
  "${CMAKE_CURRENT_LIST_DIR}/pyMachO.hpp")

source_group("Source Files\\MachO" FILES ${LIEF_PYTHON_MACHO_SRC})
source_group("Header Files\\MachO" FILES ${LIEF_PYTHON_MACHO_HDR})

target_include_directories(pyLIEF PUBLIC "${CMAKE_CURRENT_LIST_DIR}")
target_sources(pyLIEF PRIVATE "${LIEF_PYTHON_MACHO_SRC}" "${LIEF_PYTHON_MACHO_HDR}")



