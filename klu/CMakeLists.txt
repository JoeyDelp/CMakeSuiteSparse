cmake_minimum_required(VERSION 3.11 FATAL_ERROR)

project(CMakeSuiteSparseKLU VERSION 5.4.0 LANGUAGES C)

set(KLU_SRC
    src/klu.c
    src/klu_analyze.c
    src/klu_analyze_given.c
    src/klu_defaults.c
    src/klu_diagnostics.c
    src/klu_dump.c
    src/klu_extract.c
    src/klu_factor.c
    src/klu_free_numeric.c
    src/klu_free_symbolic.c
    src/klu_kernel.c
    src/klu_l.c
    src/klu_l_analyze.c
    src/klu_l_analyze_given.c
    src/klu_l_defaults.c
    src/klu_l_diagnostics.c
    src/klu_l_dump.c
    src/klu_l_extract.c
    src/klu_l_factor.c
    src/klu_l_free_numeric.c
    src/klu_l_free_symbolic.c
    src/klu_l_kernel.c
    src/klu_l_memory.c
    src/klu_l_refactor.c
    src/klu_l_scale.c
    src/klu_l_solve.c
    src/klu_l_sort.c
    src/klu_l_tsolve.c
    src/klu_memory.c
    src/klu_refactor.c
    src/klu_scale.c
    src/klu_solve.c
    src/klu_sort.c
    src/klu_tsolve.c
    src/klu_z.c
    src/klu_z_diagnostics.c
    src/klu_z_dump.c
    src/klu_z_extract.c
    src/klu_z_factor.c
    src/klu_z_free_numeric.c
    src/klu_z_kernel.c
    src/klu_z_refactor.c
    src/klu_z_scale.c
    src/klu_z_solve.c
    src/klu_z_sort.c
    src/klu_z_tsolve.c
    src/klu_zl.c
    src/klu_zl_diagnostics.c
    src/klu_zl_dump.c
    src/klu_zl_extract.c
    src/klu_zl_factor.c
    src/klu_zl_free_numeric.c
    src/klu_zl_kernel.c
    src/klu_zl_refactor.c
    src/klu_zl_scale.c
    src/klu_zl_solve.c
    src/klu_zl_sort.c
    src/klu_zl_tsolve.c)

suitesparse_target(KLU "${KLU_SRC}")

target_link_libraries(klu
                      suitesparse::config
                      suitesparse::amd
                      suitesparse::colamd
                      suitesparse::btf)
