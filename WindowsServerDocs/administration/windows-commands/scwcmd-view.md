---
title: Scwcmd view
description: Reference article for **** -




ms.topic: reference
ms.assetid: 7995959a-d93e-4865-a6a0-2ab18c2bb47f
ms.author: lizross
author: eross-msft
manager: mtillman
ms.date: 10/16/2017
---

# Scwcmd: view

> Applies to: Windows Server 2012 R2, Windows Server 2012

Renders an .xml file by using a specified .xsl transform. This command can be useful for displaying Security Configuration Wizard (SCW) .xml files by using different views.

## Syntax

```
scwcmd view /x:<Xmlfile.xml> [/s:<Xslfile.xsl>]
```

#### Parameters

|Parameter|Description|
|---------|-----------|
|/x:\<Xmlfile.xml>|Specifies the .xml file to be viewed. This parameter must be specified.|
|/s:\<Xslfile.xsl>|Specifies the .xsl transform to apply to the .xml file as part of the rendering process. This parameter is optional for SCW .xml files. When the **view** command is used to render an SCW .xml file, it will automatically try to load the correct default transform for the specified .xml file. If an .xsl transform is specified, the transform must be written under the assumption that the .xml file is in the same directory as the .xsl transform.|
|/?|Displays help at the command prompt.|

## Remarks

Scwcmd.exe is only available on computers running Windows Server 2008 R2, Windows Server 2008, or Windows Server 2003.

## Examples

To view Policyfile.xml by using the Policyview.xsl transform, type:
```
scwcmd view /x:C:\policies\Policyfile.xml /s:C:\viewers\Policyview.xsl
```

## Additional References

- [Command-Line Syntax Key](command-line-syntax-key.md)