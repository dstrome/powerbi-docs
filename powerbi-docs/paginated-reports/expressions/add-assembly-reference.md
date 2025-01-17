---
title: "Add an assembly reference to a paginated report"
description: Learn how to provide an assembly reference to a report so that the report processor can resolve names in Report Builder.
author: maggiesMSFT
ms.author: maggies
ms.reviewer: rpatkar
ms.date: 06/16/2023
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
ms.custom: updatefrequency5
---
# Add an assembly reference to a paginated report (Power BI Report Builder)

[!INCLUDE [applies-yes-report-builder-no-desktop](../../includes/applies-yes-report-builder-no-desktop.md)]

  When you embed custom code that contains references to Microsoft .NET Framework classes that are not in <xref:System.Math> or <xref:System.Convert>, you must provide an assembly reference to the report so that the report processor can resolve the names. For more information, see [Add Code to a Report (Power BI Report Builder)](./add-code-to-a-report.md).

## Add an assembly reference to a report

1. In **Design** view, right-click the design surface outside the border of the report and select **Report Properties**.

1. Select **References**.

1. In **Add or remove assemblies**, select **Add** and then select the ellipsis button to browse to the assembly.

1. In **Add or remove classes**, select **Add** and then type the name of the class and provide an instance name to use within the report.

    > [!NOTE]  
    >  Specify a class and instance name only for instance-based members. Do not specify static members in the **Classes** list. For more information, see [Custom Code and Assembly References in Expressions (Power BI Report Builder)](./custom-code-and-assembly-references-in-expressions.md).

1. Select **OK**.

## Next steps

- [Expression Uses in Reports (Power BI Report Builder)](./expression-uses-reports-report-builder.md)
- [Expression Examples (Power BI Report Builder)](./report-builder-expression-examples.md)
- [Data Types in Expressions (Power BI Report Builder)](./data-types-expressions-report-builder.md)
- [Expression Scope for Totals, Aggregates, and Built-in Collections (Power BI Report Builder)](./expression-scope-for-totals-aggregates-and-built-in-collections.md)
