cmake_minimum_required(VERSION 3.11 FATAL_ERROR)

project(CMakeSuiteSparseAMD VERSION 5.4.0 LANGUAGES C)

set(AMD_SRC
    src/amd_1.c
    src/amd_2.c
    src/amd_aat.c
    src/amd_control.c
    src/amd_defaults.c
    src/amd_dump.c
    src/amd_global.c
    src/amd_info.c
    src/amd_l_aat.c
    src/amd_l_control.c
    src/amd_l_defaults.c
    src/amd_l_dump.c
    src/amd_l_info.c
    src/amd_l_order.c
    src/amd_l_post_tree.c
    src/amd_l_postorder.c
    src/amd_l_preprocess.c
    src/amd_l_valid.c
    src/amd_l1.c
    src/amd_l2.c
    src/amd_order.c
    src/amd_post_tree.c
    src/amd_postorder.c
    src/amd_preprocess.c
    src/amd_valid.c)

suitesparse_target(AMD "${AMD_SRC}")

target_link_libraries(amd suitesparse::config)
