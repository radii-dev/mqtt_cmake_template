CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

set(EXEC_FILE "pub_test")

file(GLOB SOURCE_FILES "*.cpp")
#can also set it as this, but you need to type all names
#set(SOURCE_FILES tester.cpp test_header.cpp)
add_executable( ${EXEC_FILE} ${SOURCE_FILES} )

#This should be added after the add_executable (wherever it its)
target_link_libraries(${EXEC_FILE} pahottpp)
target_link_libraries(${EXEC_FILE} pahomqtt3a)
