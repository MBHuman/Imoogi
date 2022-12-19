# -- Variables ---------------------------------------------------------------
set(TESTS
    test_1.cpp
)

# -- Executables -------------------------------------------------------------

# testing executable
add_executable(testing test.cpp ${TESTS})

# link libraries to testing
target_link_libraries(testing
    PRIVATE gtest
)

# -- Testing -----------------------------------------------------------------

# enable testing
enable_testing()

# test
add_test(UnitTest testing)
