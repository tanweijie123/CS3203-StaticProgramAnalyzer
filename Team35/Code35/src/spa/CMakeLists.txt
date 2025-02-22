file(GLOB srcs "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")
file(GLOB headers "${CMAKE_CURRENT_SOURCE_DIR}/src/*.h" "${CMAKE_CURRENT_SOURCE_DIR}/src/*.hpp")
add_library(spa ${srcs} ${headers}
        src/model/Entity.h src/model/Entity.cpp
        src/datatype/DataType.cpp src/datatype/DataType.h
        src/datatype/AssignmentExpression.cpp src/datatype/AssignmentExpression.h
        src/datatype/ConditionalExpression.cpp src/datatype/ConditionalExpression.h
        src/model/Statement.h src/model/Statement.cpp
        src/component/PKB/PKB.cpp src/component/PKB/PKB.h
        src/component/SourceProcessor/Tokenizer.cpp src/component/SourceProcessor/Tokenizer.h
        src/component/SourceProcessor/SyntaxValidator.cpp src/component/SourceProcessor/SyntaxValidator.h
        src/component/SourceProcessor/EntityFactory.cpp src/component/SourceProcessor/EntityFactory.h
        src/datatype/Deliverable.cpp
        src/datatype/Deliverable.h
        src/util/RegexPatterns.h src/util/RegexPatterns.cpp
        src/component/SourceProcessor/SourceProcessor.cpp
        src/component/SourceProcessor/SourceProcessor.h
        src/component/SourceProcessor/Parser.cpp
        src/component/SourceProcessor/Parser.h
        src/component/SourceProcessor/PSubsystem.cpp
        src/component/SourceProcessor/PSubsystem.h
        src/component/SourceProcessor/DesignExtractor.cpp
        src/component/SourceProcessor/Parser.h src/component/SourceProcessor/Parser.cpp
        src/component/SourceProcessor/DesignExtractor.h
        src/component/QueryProcessor/types/Types.h src/component/QueryProcessor/types/Types.cpp
        src/component/QueryProcessor/types/QueryEvaluatorTable.h src/component/QueryProcessor/types/QueryEvaluatorTable.cpp
        src/component/QueryProcessor/types/UnformattedQueryResult.h src/component/QueryProcessor/types/UnformattedQueryResult.cpp
        src/component/QueryProcessor/types/IntermediateTable.h src/component/QueryProcessor/types/IntermediateTable.cpp
        src/component/QueryProcessor/QueryExtractor/QueryTokenizer.h src/component/QueryProcessor/QueryExtractor/QueryTokenizer.cpp
        src/component/QueryProcessor/QueryExtractor/QueryParser.h src/component/QueryProcessor/QueryExtractor/QueryParser.cpp
        src/component/QueryProcessor/QueryExtractor/QueryExtractor.h src/component/QueryProcessor/QueryExtractor/QueryExtractor.cpp
        src/component/QueryProcessor/QueryExtractor/QueryGrouper.h src/component/QueryProcessor/QueryExtractor/QueryGrouper.cpp
        src/component/QueryProcessor/QueryExtractor/QueryOptimizer.h src/component/QueryProcessor/QueryExtractor/QueryOptimizer.cpp
        src/component/QueryProcessor/QueryExtractor/QuerySemanticValidator.h src/component/QueryProcessor/QueryExtractor/QuerySemanticValidator.cpp
        src/component/QueryProcessor/QueryEvaluator/QueryEvaluator.h src/component/QueryProcessor/QueryEvaluator/QueryEvaluator.cpp
        src/component/QueryProcessor/QueryEvaluator/PKBQueryCommand.h src/component/QueryProcessor/QueryEvaluator/PKBQueryCommand.cpp
        src/component/QueryProcessor/QueryEvaluator/ClauseCommand.h src/component/QueryProcessor/QueryEvaluator/ClauseCommand.cpp
        src/component/QueryProcessor/QueryEvaluator/ClauseCommandExecutor.h src/component/QueryProcessor/QueryEvaluator/ClauseCommandExecutor.cpp
        src/component/QueryProcessor/QueryEvaluator/ClauseStrategy.h src/component/QueryProcessor/QueryEvaluator/ClauseStrategy.cpp
        src/component/QueryProcessor/QueryProjector.h src/component/QueryProcessor/QueryProjector.cpp
        src/component/QueryProcessor/QuerySystemController.h src/component/QueryProcessor/QuerySystemController.cpp
        src/util/Logger.cpp src/util/Logger.h
        src/util/TimeUtil.cpp src/util/TimeUtil.h
        ../unit_testing/utils/PKBStub.cpp ../unit_testing/utils/PKBStub.h src/model/CFG.cpp src/model/CFG.h
        src/component/PKB/extractor/RuntimeExtractor.cpp src/component/PKB/extractor/RuntimeExtractor.h
        src/component/PKB/extractor/NextTExtractor.cpp src/component/PKB/extractor/NextTExtractor.h
        src/component/SourceProcessor/Extractors/NextExtractor.cpp src/component/SourceProcessor/Extractors/NextExtractor
        src/component/PKB/DBManager.cpp src/component/PKB/DBManager.h
        src/component/PKB/extractor/AffectsExtractor.cpp src/component/PKB/extractor/AffectsExtractor.h
        src/component/PKB/extractor/AffectsTExtractor.cpp src/component/PKB/extractor/AffectsTExtractor.h
        src/util/Utility.cpp src/util/Utility.h
        src/util/Utility.cpp src/util/Utility.h src/component/PKB/extractor/NextBipExtractor.cpp src/component/PKB/extractor/NextBipExtractor.h
        src/component/SourceProcessor/Extractors/TransitiveExtractor.h
        src/component/SourceProcessor/Extractors/VariableTExtractor.cpp src/component/SourceProcessor/Extractors/VariableTExtractor.h
        src/component/PKB/extractor/NextBipTExtractor.cpp src/component/PKB/extractor/NextBipTExtractor.h src/component/PKB/extractor/RuntimeColleague.h src/component/PKB/extractor/RuntimeMediator.h src/component/PKB/extractor/AffectsBipExtractor.cpp src/component/PKB/extractor/AffectsBipExtractor.h src/component/PKB/extractor/AffectsBipTExtractor.cpp src/component/PKB/extractor/AffectsBipTExtractor.h)

# this makes the headers accessible for other projects which uses spa lib
target_include_directories(spa PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

SET(CMAKE_BUILD_TYPE Debug)
