cmake_minimum_required(VERSION 2.6)
project (jadesoul)

set(apps
	trim
	body
	caser
	sample
	odd
)

foreach(app ${apps})
	add_executable(${app} ${app}.cpp)
	install(TARGETS ${app} DESTINATION ${BIN_INSTALL_DIR})
	target_link_libraries(${app} soul)
endforeach(app)
