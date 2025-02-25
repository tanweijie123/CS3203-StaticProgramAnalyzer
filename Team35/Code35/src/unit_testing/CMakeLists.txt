file(GLOB srcs "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")
file(GLOB headers "${CMAKE_CURRENT_SOURCE_DIR}/src/*.h" "${CMAKE_CURRENT_SOURCE_DIR}/src/*.hpp")
add_executable(unit_testing ${srcs}
        src/component/QueryProcessor/types/TestQueryEvaluatorTable.cpp
        src/component/QueryProcessor/TestQueryProjector.cpp
        src/component/QueryProcessor/QueryExtractor/TestQueryExtractor.cpp
        src/component/QueryProcessor/QueryExtractor/TestQueryGrouper.cpp
        src/component/QueryProcessor/QueryExtractor/TestQueryOptimizer.cpp
        src/component/QueryProcessor/QueryEvaluator/TestQueryEvaluator.cpp
        src/component/QueryProcessor/QueryEvaluator/TestClauseStrategy.cpp
        src/component/SourceProcessor/TestTokenizer.cpp
        src/component/SourceProcessor/TestSyntaxValidator.cpp
        src/component/SourceProcessor/TestEntityFactory.cpp
        utils/TestUtils.cpp utils/TestUtils.h
        utils/EntityUtils.h
        src/datatype/TestDataType.cpp
        src/component/SourceProcessor/TestPsubsystem.cpp
        src/component/PKB/TestPKB.cpp src/datatype/TestAssignmentExpression.cpp
        src/datatype/TestDeliverable.cpp utils/EntityUtils.h
        src/component/SourceProcessor/Extractors/TestTransitiveExtractor/TestFollowsT.cpp
        src/component/SourceProcessor/Extractors/TestTransitiveExtractor/TestParentT.cpp
        ../spa/src/exception/SpaException.h
        src/util/TestCommonUtils.cpp src/model/TestEntity.cpp
        src/model/TestStatement.cpp src/datatype/TestConditionalExpression.cpp src/model/TestCFG.cpp
        src/component/SourceProcessor/Extractors/TestNextRelationship.cpp
        src/component/SourceProcessor/TestParser.cpp
        src/component/PKB/TestNextTExtractor.cpp
        src/component/SourceProcessor/Extractors/TestTransitiveExtractor/TestCallsT.cpp
        src/model/TestVariableMapping.cpp
        src/component/PKB/TestAffectsExtractor.cpp
        src/component/SourceProcessor/Extractors/TestVariableTExtractor.cpp
        src/component/SourceProcessor/Extractors/TestTransitiveExtractor/TestCallsT.cpp
        src/component/PKB/TestAffectsTExtractor.cpp)

target_link_libraries(unit_testing spa)
SET(CMAKE_BUILD_TYPE Debug)
