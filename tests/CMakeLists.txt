add_executable(Hash_map_test)

find_package(Catch2 REQUIRED)
target_link_libraries(Hash_map_test PRIVATE Catch2::Catch2)
target_compile_definitions(Hash_map_test PRIVATE CATCH_CONFIG_ENABLE_BENCHMARKING)

target_link_libraries(Hash_map_test PRIVATE Hash_map)

target_sources(
    Hash_map_test
        PRIVATE
            "main.cpp"
            "Hash_map.test.cpp"
)

include(Catch)
catch_discover_tests(Hash_map_test)
