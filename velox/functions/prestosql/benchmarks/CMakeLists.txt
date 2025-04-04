# Copyright (c) Facebook, Inc. and its affiliates.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
set(BENCHMARK_DEPENDENCIES
    velox_functions_test_lib
    velox_exec
    velox_functions_prestosql
    velox_functions_lib
    velox_exec_test_util
    velox_vector_fuzzer
    ${GTEST_BOTH_LIBRARIES}
    ${gflags_LIBRARIES}
    ${FOLLY_WITH_DEPENDENCIES}
    ${FOLLY_BENCHMARK})

add_executable(velox_functions_prestosql_benchmarks_array_contains
               ArrayContainsBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_array_contains
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_array_min_max
               ArrayMinMaxBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_array_min_max
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_width_bucket
               WidthBucketBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_width_bucket
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_string_ascii_utf_functions
               StringAsciiUTFFunctionBenchmarks.cpp)
target_link_libraries(
  velox_functions_prestosql_benchmarks_string_ascii_utf_functions
  ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_not NotBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_not
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_date_time
               DateTimeBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_date_time
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_bitwise
               BitwiseBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_bitwise
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_in InBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_in
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_prestosql_benchmarks_map_input
               MapInputBenchmark.cpp)
target_link_libraries(velox_functions_prestosql_benchmarks_map_input
                      ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_benchmarks_url URLBenchmark.cpp)
target_link_libraries(velox_functions_benchmarks_url ${BENCHMARK_DEPENDENCIES})

add_executable(velox_functions_benchmarks_compare CompareBenchmark.cpp)
target_link_libraries(velox_functions_benchmarks_compare
                      ${BENCHMARK_DEPENDENCIES})
