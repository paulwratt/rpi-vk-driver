file(GLOB testSrc
	"*.h"
	"*.cpp"
)

add_executable(blending ${testSrc} )
target_compile_options(blending PRIVATE -Wall -std=c++11 -std=c11)

target_link_libraries(blending vulkan  $<TARGET_OBJECTS:QPUassembler>)
