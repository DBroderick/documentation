---
title: How to upgrade your edge gateway | UKCloud Ltd
description: This article explains how to check the current version of your edge gateway and upgrade to the latest version
services: vmware
author: Sue Highmoor
reviewer:
lastreviewed: 10/05/2019
toc_rootlink: How To
toc_sub1: 
toc_sub2:
toc_sub3:
toc_sub4:
toc_title: Upgrade your edge gateway
toc_fullpath: How To/vmw-how-upgrade-edge.md
toc_mdlink: vmw-how-upgrade-edge.md
---

# How to upgrade your edge gateway

## Overview

This guide shows you how to check the existing version of your edge gateway and, if necessary, upgrade it to the latest available version. If you need any assistance with the upgrade process, contact the support team by raising a service request in the [My Calls](https://portal.ukcloud.com/support/my_calls) section of the UKCloud Portal.

> [!NOTE]
> In preparation for our planned upgrade to vCloud Director 9.7, you must convert your edges to advanced gateways. For more information, see [*How to convert your edge to an advanced gateway*](vmw-how-convert-edge.md).
>
> If you're already using advanced gateways, you should upgrade them to 6.4.*x*.

## Intended audience

To complete the steps in this guide you must have access to the UKCloud Portal and vCloud Director.

## Checking the current version of your edge gateway

Before you attempt to upgrade your edge gateway, check for the existing version of your edge gateway:

1. Log in to the UKCloud Portal.

    For more detailed steps, see the [*Getting Started Guide for the UKCloud Portal*](../portal/ptl-gs.md).

2. If necessary, switch to the appropriate account.

3. Click **My VMs**.

    ![My VMs](images/upgrade-image-1.png)

4. Select the compute service (vOrg) that the edge gateway belongs to.

5. Select the **My VMs** tab.

   ![My VMs tab](images/upgrade-image-2.png)

6. From the **Currently viewing for VDC** list, select the VDC that the edge gateway you want to check belongs to.

7. Select the **Edge Gateway** tab.

   ![Edge Gateway](images/upgrade-image-3.png)

8. From the **Select Edge** list, select the edge gateway that you want to check.

9. The **VM version** field shows the version number of your edge gateway.

    If the version is lower than 6.4.*x* (for example, 6.2.7), make a note that the edge gateway needs upgrading.

   ![VM version](images/upgrade-image-4.png)

10. Repeat these steps for any other edge gateways that you want to check.

## Upgrading your edge gateway to the latest available version

The following steps show how to upgrade your edge gateway using vCloud Director.

> [!NOTE]
> Before you begin the upgrade process, bear in mind that there will be a brief network disruption for the networks that are used by the edge gateway instance.

> [!NOTE]
> You cannot redeploy edge gateways in the new vCloud Director 9.1 tenant portal, you must first switch to the vCloud Director web console. For more information, see [*How to switch to the vCloud Director web console from the tenant portal*](vmw-how-switch-web-console.md).

1. In vCloud Director, select the **Administration** tab.

    ![Administration](images/upgrade-image-8.png)

2. Double-click the VDC that the edge gateway that you want to upgrade belongs to (or right-click the VDC and select **Open**).

3. Select the **Edge Gateways** tab.

    ![Edge gateways](images/upgrade-image-9.png)

4. Right-click the edge gateway that you want to upgrade and select **Re-Deploy**.

5. In the confirmation dialog box, click **Yes**.

    > [!IMPORTANT]
    > This step requires downtime as a new VM needs to be deployed for the edge gateway. You should make sure that you have planned for this downtime before proceeding.

6. You can monitor the status in the *Activity Task Detail* dialog box.

7. After the redeployment has finished, you can check the version of the edge gateway again in the UKCloud Portal to confirm that the upgrade has been successful.

## Next steps

We recommend that you convert your edge gateway to an advanced gateway to take advantage of more features and to access the new HTML5-based tenant portal. For more information, including known issues, see [*How to convert your edge to an advanced gateway*](vmw-how-convert-edge.md). All edge gateways must be converted to advanced gateways before our planned upgrade to vCloud Director 9.7.

## Feedback

If you find an issue with this article, click **Improve this Doc** to suggest a change. If you have an idea for how we could improve any of our services, visit [UKCloud Ideas](https://ideas.ukcloud.com). Alternatively, you can contact us at <products@ukcloud.com>.
