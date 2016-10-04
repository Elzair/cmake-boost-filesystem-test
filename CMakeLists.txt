cmake_minimum_required(VERSION 3.3)

project(test_filesystem)

add_subdirectory(libs)

add_executable(test_filesystem test.cpp)

target_link_libraries(test_filesystem
  boost::align boost::array boost::assert
  boost::bind
  boost::concept_check boost::config boost::conversion boost::core
  boost::detail
  boost::filesystem boost::function boost::function_types boost::functional boost::fusion
  boost::integer boost::io boost::iterator
  boost::move boost::mpl
  boost::numeric::conversion
  boost::optional
  boost::predef boost::preprocessor
  boost::smart_ptr boost::static_assert
  boost::throw_exception boost::tuple boost::type_index boost::type_traits boost::typeof
  boost::utility
  boost::system
  boost::regex)
