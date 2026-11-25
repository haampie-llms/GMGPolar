set(DENSITY_PROFILE_COEFFICIENTS_SOURCES
    poissonCoefficients.cpp
    sonnendruckerCoefficients.cpp
    sonnendruckerGyroCoefficients.cpp
    zoniCoefficients.cpp
    zoniGyroCoefficients.cpp
    zoniShiftedCoefficients.cpp
    zoniShiftedGyroCoefficients.cpp
)

add_library(InputFunctions_DensityProfileCoefficients STATIC ${DENSITY_PROFILE_COEFFICIENTS_SOURCES})
gmgpolar_set_kokkos_language(InputFunctions_DensityProfileCoefficients)
target_include_directories(InputFunctions_DensityProfileCoefficients PUBLIC
    ${GMGPOLAR_INCLUDE_DIRS}
)
target_link_libraries(InputFunctions_DensityProfileCoefficients PUBLIC Kokkos::kokkos)
