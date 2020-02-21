# IGCMS Ontology

## System Plugins

The structure can be simplified into a list of plugins. There are dependencies between plugins. Some plugins are mandatory (the system cannot run without them). Each plugin may contain specific features that can introduce specific dependencies and limitations.

  * FillFormPlugin
  * InputVarPlugin (mandatory)
  * MarkdownPlugin
  * ...

Additionally each plugin and its feature has specific complexity index. That determines its initial cost and its maintenance / development fee.

## User Features

There is a hierarchy of supported user features that may require specific plugins or plugin features. Some features are incompatible with static environment.

  * AdminFeature (non-static)
    * CustomOneClickAdminFeature (requires FillFormPlugin)
    * GitRepositoryAdminFeature
    * MarkdownSyntaxAdminFeature (requires MarkdownPlugin)
    * GoogleSpreadsheetAdminFeature
  * ...

Additionally each feature has its usual setup difficulty. That determines its setup cost and influences the maintenance / development fee.

## Website instance

Each website instance consists of plugins inferred from specified subset of features. There are three types of relations -- MUST, SHOULD, and NTH.

  * exampleWebsite
    * CustomOneClickAdminFeature (MUST)
    * GitRepository (SHOULD)
    * MarkdownSyntax (NTH)
    * GoogleSpreadsheet (MUST)
  * ...

## Want to Show

  * Required plugin configurations for each website instance for each type of relation.
  * Total complexity and setup difficulty for each website instance.
  * Compatibility with static environment, ergo list of incompatible features.
