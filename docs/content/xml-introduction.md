# XML Wrapper

Galaxy Visualizations are configured using XML files. The files contain Visualization specific attributes such as the `name`, `description` and the associated npm package details.

```xml
<visualization name="MY_VISUALIZATION">
    <description>MY_DESCRIPTION</description>
    <requirements>
        <requirement type="npm" version="MY_NPM_PACKAGE_VERSION" package="MY_NPM_PACKAGE_NAME"/>
    </requirements>
    <entry_point entry_point_type="script" src="dist/index.js" css="dist/index.css" />
    ...
</visualization>
```

This XML template includes the following variables:

| Variable | Description |
|----------|-------------|
| **MY_VISUALIZATION** | Specifies the name of the visualization. |
| **MY_DESCRIPTION** | Provides a brief description of the visualization, including references if it’s a third-party plugin. |
| **MY_NPM_PACKAGE_NAME** | Indicates the npm package name. Update this field with the correct package name before publishing. |
| **MY_NPM_PACKAGE_VERSION** | Specifies the version number of the npm package upon publishing. |

## Macros

Although less common, you can choose to reuse XML sections by placing them into `macros`. This helps eliminate duplication when the same content is used across multiple XMLs.

Create a macro file e.g. `macro.xml`, and define `macros` like this:

```xml
<macros>
    <xml name="my_macro">
        ...
    </xml>
</macros>
```

In your main XML file, include and reuse the `macros` like this:

```xml
<visualization name="MY_VISUALIZATION">
    <macros>
        <import>macro.xml</import>
    </macros>
    ...
    <expand macro="my_macro"/>
    ...
</visualization>
```
