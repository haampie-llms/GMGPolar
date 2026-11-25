set(DOMAIN_GEOMETRY_SOURCES
    circularGeometry.cpp
    culhamGeometry.cpp
    czarnyGeometry.cpp
    shafranovGeometry.cpp
)

add_library(InputFunctions_DomainGeometry STATIC ${DOMAIN_GEOMETRY_SOURCES})
gmgpolar_set_kokkos_language(InputFunctions_DomainGeometry)
target_include_directories(InputFunctions_DomainGeometry PUBLIC
    ${GMGPOLAR_INCLUDE_DIRS}
)
target_link_libraries(InputFunctions_DomainGeometry PUBLIC Kokkos::kokkos)
