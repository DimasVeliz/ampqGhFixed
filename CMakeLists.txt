set(GCC_COVERAGE_COMPILE_FLAGS "-fPIC")

add_definitions(${GCC_COVERAGE_COMPILE_FLAGS})


add_library(
    amqpGhFixed SHARED
    src/amqpGhFixed/AMQPcpp.h 
    src/amqpGhFixed/AMQP.cpp
    src/amqpGhFixed/AMQPBase.cpp
    src/amqpGhFixed/AMQPException.cpp
    src/amqpGhFixed/AMQPExchange.cpp
    src/amqpGhFixed/AMQPMessage.cpp
    src/amqpGhFixed/AMQPQueue.cpp
)
target_include_directories(amqpGhFixed PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/src") 
target_link_libraries(amqpGhFixed rabbitmq)

