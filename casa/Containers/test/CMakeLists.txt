set (tests
tBlock
tBlockTrace
tHashMap
tHashMapIO
tHashMapIter
tList
tObjectPool
tObjectStack
tOrdMap2
tOrdMap
tPoolStack
tQueue
tRecord
tRecordDesc
tSimOrdMap
tStack
tValueHolder
)

foreach (test ${tests})
    add_executable (${test} ${test}.cc)
    target_link_libraries (${test} casa_casa)
    add_test (${test} ${CMAKE_SOURCE_DIR}/cmake/cmake_assay ./${test})
    add_dependencies(check ${test})
endforeach (test)
