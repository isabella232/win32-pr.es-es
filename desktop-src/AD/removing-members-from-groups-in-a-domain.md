---
title: Quitar miembros de grupos en un dominio
description: Puede quitar usuarios, grupos o contactos de los grupos.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- agrupa AD, quitar miembros de grupos en un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789484"
---
# <a name="removing-members-from-groups-in-a-domain"></a><span data-ttu-id="9c2c0-104">Quitar miembros de grupos en un dominio</span><span class="sxs-lookup"><span data-stu-id="9c2c0-104">Removing Members from Groups in a Domain</span></span>

<span data-ttu-id="9c2c0-105">Puede quitar usuarios, grupos o contactos de los grupos.</span><span class="sxs-lookup"><span data-stu-id="9c2c0-105">You can remove users, groups, or contacts from groups.</span></span> <span data-ttu-id="9c2c0-106">El atributo **member** del objeto **Group** contiene todos los miembros directos del grupo.</span><span class="sxs-lookup"><span data-stu-id="9c2c0-106">The **member** attribute of the **group** object contains all direct members of the group.</span></span>

<span data-ttu-id="9c2c0-107">La manera más sencilla de quitar un miembro de un grupo es llamar al método [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) en la interfaz [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) del objeto de grupo del que desea quitar miembros.</span><span class="sxs-lookup"><span data-stu-id="9c2c0-107">The simplest way to remove a member from a group is to call the [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) method on the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface of the group object you want to remove members from.</span></span>

 

 