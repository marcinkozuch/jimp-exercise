
project(wordcounter)

set(HEDEAR_FILES WordCounter.h Counts.h Word.h)
set(SOURCE_FILES WordCounter.cpp Counts.cpp Word.cpp)

add_library(libwordcounter STATIC ${SOURCE_FILES})
target_include_directories(libwordcounter PUBLIC ../wordcounter)

add_executable(wordcounter ${SOURCE_FILES} main.cpp)

target_link_libraries(wordcounter libwordcounter)