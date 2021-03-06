cmake_minimum_required(VERSION 3.5.1)
project(NetworkProgramming)

set(CMAKE_CXX_STANDARD 14)

add_executable(NetworkProgramming main.cpp)
add_executable(echosrv echosrv.cpp)
add_executable(echocli echocli.cpp)
add_executable(echosrv2 echosrv2.cpp)
add_executable(echocli2 echocli2.cpp)
add_executable(echosrv3 echosrv3.cpp)
add_executable(echocli3 echocli3.cpp)
add_executable(echosrv4 echosrv4.cpp)
add_executable(echocli4 echocli4.cpp)
add_executable(echosrv5 echosrv5.cpp)
add_executable(echocli5 echocli5.cpp)
add_executable(echosrv6 echosrv6.cpp)
add_executable(echocli6 echocli6.cpp)
add_executable(echosrv7 echosrv7.cpp)
add_executable(echocli7 echocli7.cpp)
add_executable(conntest conntest.cpp)
add_executable(pollsrv pollsrv.cpp)
add_executable(epollsrv epollsrv.cpp)
add_executable(gethostbyname_test gethostbyname_test.cpp)
add_executable(p2pcli p2pcli.cpp)
add_executable(p2pserv p2pserv.cpp)
add_executable(udpsrv udpsrv.cpp)
add_executable(udpcli udpcli.cpp)
add_executable(udpmulclt udpmulclt.cpp)
add_executable(udpmulsrv udpmulsrv.cpp)
add_executable(unixcli unixcli.cpp)
add_executable(unixsrv unixsrv.cpp)
add_executable(sockpair sockpair.cpp)
add_executable(sockpair02 sockpair02.cpp)
add_executable(msgget msgget.cpp)
add_executable(msgctl01 msgctl01.cpp)
add_executable(msgctl02 msgctl02.cpp)
add_executable(msg_send msg_send.cpp)
add_executable(msg_recv msg_recv.cpp)
add_executable(msgcli msgcli.cpp)
add_executable(msgsrv msgsrv.cpp)
add_executable(mmap_recv mmap_recv.cpp)
add_executable(mmap_send mmap_send.cpp)
add_executable(shmread shmread.cpp)
add_executable(shmwrite shmwrite.cpp)
add_executable(sem sem.cpp)
add_executable(sem02 sem02.cpp)
add_executable(sem03 sem03.cpp)
add_executable(01mqopen 01mqopen.cpp)
add_executable(02myunlink 02myunlink.cpp)
add_executable(03mqgetattr 03mqgetattr.cpp)
add_executable(04mqsend 04mqsend.cpp)
add_executable(05mqreceive 05mqreceive.cpp)
add_executable(06mqnotify 06mqnotify.cpp)
add_executable(01shmopen 01shmopen.cpp)
add_executable(02shmunlink 02shmunlink.cpp)
add_executable(03shmwrite 03shmwrite.cpp)
add_executable(04shmreceive 04shmreceive.cpp)
add_executable(thread_create thread_create.cpp)
add_executable(threadechosrv threadechosrv.cpp)
add_executable(thread thread.cpp)
add_executable(pctest pctest.cpp)
add_executable(condtest condtest.cpp)

add_subdirectory(udpchat)
add_subdirectory(shmfifo)
add_subdirectory(threadpool)

set(semsrc
        sem.cpp)

add_library(semtool ${semsrc})

target_link_libraries(01mqopen rt)
target_link_libraries(02myunlink rt)
target_link_libraries(03mqgetattr rt)
target_link_libraries(04mqsend rt)
target_link_libraries(05mqreceive rt)
target_link_libraries(06mqnotify rt)
target_link_libraries(01shmopen rt)
target_link_libraries(02shmunlink rt)
target_link_libraries(03shmwrite rt)
target_link_libraries(04shmreceive rt)
target_link_libraries(thread_create pthread)
target_link_libraries(threadechosrv pthread)
target_link_libraries(thread pthread)
target_link_libraries(pctest pthread rt)
target_link_libraries(condtest pthread rt)