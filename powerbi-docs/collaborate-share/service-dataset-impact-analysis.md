---
title: Dataset impact analysis
description: Learn how to visualize and analyze the downstream impact of making changes to datasets and dashboards.
author: paulinbar
ms.author: painbar
ms.reviewer: 
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: how-to
ms.date: 02/17/2023
LocalizationGroup: 
---

# Dataset impact analysis

When you make changes to a dataset, or are considering making changes, it's important to be able to assess the potential impact of those changes on downstream reports and dashboards that depend on that dataset. **Dataset impact analysis** provides you with information that can help you make this assessment.

* It shows you how many workspaces, reports, and dashboards might be affected by your change, and provides easy navigation to the workspaces where the affected reports and dashboards are located so that you can investigate further.
* It shows you how many unique visitors and the number of views there are on the potentially affected items. This helps you determine the overall impact of the change for the downstream item. For instance, it's probably more important to investigate the effect of a change on a report that has 20,000 unique viewers than it is to investigate the effect of the change on a report that has three viewers.
* It provides an easy way to notify the relevant people about a change you made or are thinking about making.

Dataset impact analysis is easily launched from within [data lineage view](service-data-lineage.md).

## Identify shared datasets

You can perform dataset impact analysis on both shared and unshared datasets. However, it's particularly useful for datasets that are shared across workspaces, where it's much more complicated to get a clear picture of downstream dependencies than it is with unshared datasets, all of whose dependencies are located in the same workspace as the dataset itself.

In lineage view, you can tell the difference between shared datasets and unshared datasets by the icon that appears in the upper left-hand corner of the dataset's card.

:::image type="content" source="media/service-dataset-impact-analysis/shared-unshared-icon.png" alt-text="Screenshot of shared and unshared dataset icons.":::

## Perform dataset impact analysis

You can perform impact analysis on any dataset in the workspace, whether it's shared or not. You can't perform impact analysis on external datasets that are displayed in lineage view but are in fact located in another workspace. To perform impact analysis on an external dataset, you need to navigate to the source workspace.

To perform dataset impact analysis, select the impact analysis button on the dataset card.

:::image type="content" source="media/service-dataset-impact-analysis/open-analysis-pane-button.png" alt-text="Screenshot of the dataset impact analysis button.":::

The impact analysis side panel opens.

:::image type="content" source="media/service-dataset-impact-analysis/service-impact-analysis-pane.png" alt-text="Screenshot of the impact analysis side pane.":::

* The **impact summary** shows you the number of potentially impacted workspaces, reports, and dashboards, as well as the total number of views for all the downstream reports and dashboards that are connected to the dataset.
* The **notify contacts** link opens a dialog where you can create a message about any dataset changes you make, and send it to the contact lists of the affected workspaces. 
* The **usage metrics** show you, for each workspace, the total number of views for the potentially impacted reports and dashboards it contains, and for each report and dashboard, the total number of viewers and views, where:
   * Viewers: The number of distinct users that viewed a report or dashboard.
   * Views: The number of views for a report or dashboard

The usage metrics relate to the last 30 days, excluding the current day. The count includes usage coming via related apps. The metrics help you understand dataset use across the tenant, as well as assess the impact any changes to your dataset might have.

## Notify contacts

If you've made a change to a dataset or are thinking about making a change, you might want to contact the relevant users to tell them about it. When you notify contacts, an email is sent to the [contact lists](../collaborate-share/service-create-the-new-workspaces.md#create-a-contact-list) of all the impacted workspaces. Your name appears on the email so the contacts can find you and reply back in a new email thread. 

1. Select **Notify contacts** in the impact analysis side pane. The notify contacts dialog appears.

    :::image type="content" source="media/service-dataset-impact-analysis/notify-contacts-dialog.png" alt-text="Screenshot of the Notify contacts dialog box.":::

1. In the text box, provide some detail about the change.
1. When the message is ready, select **Send**.

> [!NOTE]
> Notify contacts is not available if the dataset you're performing impact analysis on is located in a classic workspace.

## Privacy

In order to perform impact analysis on a dataset, you must have write permissions to it. In the impact analysis side pane, you only see real names for workspaces, reports, and dashboards that you have access to. Items that you don't have access to are listed as **Limited access**. This is because some item names may contain personal information.

Even if you don't have access to some workspaces, you still see summarized usage metrics for those workspaces, and your notify contacts messages will still reach the contact lists of those workspaces.

## Impact analysis from Power BI Desktop

When you make a change to a dataset in Power BI Desktop and then republish it to the Power BI service, a message shows you how many workspaces, reports, and dashboards are potentially impacted by the change, and asks you to confirm that you want to replace the currently published dataset with the one you modified. The message also provides a link to the full dataset impact analysis in the Power BI service, where you can see more information and take action to mitigate the risks of your change.

:::image type="content" source="media/service-dataset-impact-analysis/service-dataset-impact-analysis-desktop-warning.png" alt-text="Screenshot of the impact analysis message.":::

> [!NOTE]
> The information shown in the message only indicates potential impact. It doesn't necessarily indicate that anything has broken. Dataset changes often have no adverse effect on their downstream reports and dashboards. Still, you get this message that gives you clarity concerning potential impact.
>
>In the message, the number of workspaces is only shown if more than one workspace contains impacted reports and dashboards.

## Considerations and limitations

* Usage metrics aren't supported for personal workspaces.

## Next steps

* [Intro to datasets across workspaces](../connect-data/service-datasets-across-workspaces.md)
* [Data lineage](service-data-lineage.md)

