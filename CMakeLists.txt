cmake_minimum_required(VERSION 2.8)

include(cmake/PICMake.cmake)

pi_add_target(gslamDB_net SHARED src/dbnet REQUIRED GSLAM Qt DEPENDENCY QtNetwork)
pi_add_target(GCSServer BIN src/GCSServer REQUIRED OpenCV Qt DEPENDENCY QtNetwork)
pi_add_target(GCSClient BIN src/GCSClient REQUIRED Qt DEPENDENCY QtNetwork)
pi_report_target()

pi_install(TARGET gslamDB_net)
