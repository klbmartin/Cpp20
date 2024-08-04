# library mathlib
add_library(mathlib)
target_sources(mathlib
  PUBLIC
    FILE_SET CXX_MODULES FILES
      math.ixx
)
add_executable(client client.cpp)
target_link_libraries(client mathlib)

# library mathlib1
add_library(mathlib1)
target_sources(mathlib1
  PUBLIC
    FILE_SET CXX_MODULES FILES
      math1.ixx
)
add_executable(client1 client1.cpp)
target_link_libraries(client1 mathlib1)

# library mathlib1
add_library(mathModuleTemplateLib)
target_sources(mathModuleTemplateLib
  PUBLIC
    FILE_SET CXX_MODULES FILES
    mathModuleTemplate.ixx
)
add_executable(clientTemplate clientTemplate.cpp)
target_link_libraries(clientTemplate mathModuleTemplateLib)

add_executable(requiresClause requiresClause.cpp)
