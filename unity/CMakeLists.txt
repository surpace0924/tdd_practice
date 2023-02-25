cmake_minimum_required( VERSION 3.2 )
project( unity_test )

include_directories( lib/Unity/src )
include_directories( lib/Unity/extras/fixture/src )
include_directories( lib/Unity/extras/memory/src )
link_libraries( m )

set(UNITY_FILES
    lib/Unity/src/unity.c
    lib/Unity/extras/fixture/src/unity_fixture.c
)

set(TEST_FILES
    test/stdio/sprintf_test.c
    test/stdio/sprintf_test_runner.c
    test/all_tests.c
)

add_executable( unity_test ${TEST_FILES} ${UNITY_FILES} )
