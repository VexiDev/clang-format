## My global `~/.clang-format` file

> [!Note]
> For clang-format **19.x.x**
> <br>Tested on `19.1.3` with [stevearc/conform.nvim](https://github.com/stevearc/conform.nvim)

```yaml
# Core
BasedOnStyle: Google
ColumnLimit: 119
Standard: Auto

# Java rules
JavaImportGroups: [com, org, net,java, sun, gg, gg.vexi]
SortJavaStaticImport: After

# JavaScript rules
JavaScriptQuotes: Single
JavaScriptWrapImports: true

# Ignore comments where first nonspace is '$' or '<'
CommentPragmas: "^[ ]*[$<]"
ReflowComments: false

# Custom brace wrapping
BreakBeforeBraces: Custom
Cpp11BracedListStyle: true
InsertBraces: false
BraceWrapping:
  # AfterControlStatements: MultiLine # Unknown key?
  AfterCaseLabel: false
  AfterClass: false
  AfterEnum: false
  AfterFunction: false
  AfterNamespace: false
  AfterObjCDeclaration: false
  AfterStruct: false
  AfterUnion: false
  AfterExternBlock: false
  BeforeCatch: false
  BeforeElse: false
  BeforeLambdaBody: false
  BeforeWhile: true
  IndentBraces: false
  SplitEmptyFunction: false
  SplitEmptyRecord: false
  SplitEmptyNamespace: false

# Indent/Tab Widths
IndentWidth: 4
BracedInitializerIndentWidth: 4
ConstructorInitializerIndentWidth: 4
ContinuationIndentWidth: 4
PPIndentWidth: 4
TabWidth: 4

# Alignemnt options
AlignAfterOpenBracket: BlockIndent # Align|DontAlign|AlwaysBreak|
AlignArrayOfStructures: Left
AlignConsecutiveAssignments:
  Enabled: false
  AcrossEmptyLines: true
  AcrossComments: false
AlignConsecutiveDeclarations:
  Enabled: false
  AcrossEmptyLines: false
  AcrossComments: true
  #AlignFunctionDeclarations: true # Unkown key?
AlignEscapedNewlines: Left
AlignOperands: AlignAfterOperator
AlignTrailingComments:
  Kind: Always
  OverEmptyLines: 1

# Next line rules
AllowAllArgumentsOnNextLine: true
AllowAllParametersOfDeclarationOnNextLine: false

# Single line rules
BinPackArguments: false
BinPackParameters: true # Boolean? Not AlwaysOnePerLine?
AllowShortBlocksOnASingleLine: Always
AllowShortCaseExpressionOnASingleLine: true
AllowShortCaseLabelsOnASingleLine: true
AllowShortCompoundRequirementOnASingleLine: true
AllowShortEnumsOnASingleLine: false
AllowShortFunctionsOnASingleLine: Inline # idk if this is what I want
AllowShortIfStatementsOnASingleLine: AllIfsAndElse
AllowShortLambdasOnASingleLine: Empty
AllowShortLoopsOnASingleLine: true

# Line break rules
AlwaysBreakBeforeMultilineStrings: false
BreakAfterJavaFieldAnnotations: false
BreakAfterReturnType: ExceptShortType
BreakBeforeBinaryOperators: NonAssignment
BreakBeforeConceptDeclarations: Allowed
BreakBeforeTernaryOperators: false
#BreakBinaryOperations: Never # Not available for 19.1.3
BreakConstructorInitializers: AfterColon
BreakFunctionDefinitionParameters: false
BreakInheritanceList: AfterColon
BreakStringLiterals: true
BreakTemplateDeclarations: No
CompactNamespaces: false
EmptyLineAfterAccessModifier: Never
EmptyLineBeforeAccessModifier: Leave
IncludeBlocks: Regroup
PackConstructorInitializers: Never


# Indent rules
IndentAccessModifiers: false
IndentCaseBlocks: false
IndentCaseLabels: true
IndentExternBlock: Indent
IndentGotoLabels: true
IndentPPDirectives: AfterHash
IndentRequires: true
IndentWrappedFunctionNames: true
LambdaBodyIndentation: OuterScope
NamespaceIndentation: All

# Line rules
LineEnding: LF
SeparateDefinitionBlocks: Always
MaxEmptyLinesToKeep: 1
InsertNewlineAtEOF: true
#RemoveEmptyLinesInUnwrappedLines: true # Not available for 19.1.3

KeepEmptyLines:
  AtEndOfFile: true
  AtStartOfBlock: true
  AtStartOfFile: true

# Penalties
PenaltyBreakAssignment: 2
PenaltyBreakBeforeFirstCallParameter: 19
PenaltyBreakComment: 300
PenaltyBreakFirstLessLess: 120
PenaltyBreakOpenParenthesis: 0
PenaltyBreakScopeResolution: 8
PenaltyBreakString: 1000
PenaltyBreakTemplateDeclaration: 10
PenaltyExcessCharacter: 1000000
PenaltyIndentedWhitespace: 15
PenaltyReturnTypeOnItsOwnLine: 200

# Space rules
SpaceAfterCStyleCast: true
SpaceAfterTemplateKeyword: true

SpaceInEmptyBlock: false
SpacesInAngles: Never
SpacesInContainerLiterals: false
SpacesInSquareBrackets: false
SpacesBeforeTrailingComments: 1
SpacesInLineCommentPrefix:
  Minimum: 0
  Maximum: -1
SpacesInParens: Custom
SpacesInParensOptions:
  ExceptDoubleParentheses: false
  InConditionalStatements: true
  InCStyleCasts: false
  InEmptyParentheses: false
  Other: false

SpaceBeforeAssignmentOperators: true
SpaceBeforeCaseColon: true
SpaceBeforeCpp11BracedList: false
SpaceBeforeCtorInitializerColon: true
SpaceBeforeInheritanceColon: true
SpaceBeforeJsonColon: false
SpaceBeforeRangeBasedForLoopColon: true
SpaceBeforeSquareBrackets: false
SpaceBeforeParens: Custom
SpaceBeforeParensOptions:
  AfterControlStatements: true
  AfterFunctionDeclarationName: false
  AfterFunctionDefinitionName: false
  AfterOverloadedOperator: true
  AfterPlacementOperator: true
  AfterRequiresInClause: true
  AfterRequiresInExpression: true
  BeforeNonEmptyParentheses: false

# Other rules
FixNamespaceComments: true
ShortNamespaceLines: 4

InsertTrailingCommas: Wrapped
IntegerLiteralSeparator:
  Binary: 4
  BinaryMinDigits: 5
  Decimal: 3
  DecimalMinDigits: 5
  Hex: 2
  HexMinDigits: 6

RequiresClausePosition: SingleLine
RequiresExpressionIndentation: Keyword

QualifierAlignment: Custom
QualifierOrder:
  - const
  - constexpr
  - friend
  - static
  - inline
  - restrict
  - volatile
  - type
```
