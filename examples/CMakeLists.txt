FetchContent_Declare(
  cli11
  GIT_REPOSITORY https://github.com/CLIUtils/CLI11.git
  GIT_TAG 457839d482455e746faabc07e2e6fa4c30f2d553
)
FetchContent_MakeAvailable(cli11)

add_executable(ex_build_navmesh
	"${CMAKE_CURRENT_SOURCE_DIR}/ex_build_navmesh.cpp"
)

target_link_libraries(ex_build_navmesh PRIVATE
	CLI11::CLI11
	RecastNavigation::Recast
)
