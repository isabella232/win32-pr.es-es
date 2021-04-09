---
title: Enumerar miembros de un grupo
description: Los miembros de un grupo se almacenan en un atributo de varios valores denominado Member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerar miembros de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149179"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="5cae4-104">Enumerar miembros de un grupo</span><span class="sxs-lookup"><span data-stu-id="5cae4-104">Enumerating Members in a Group</span></span>

<span data-ttu-id="5cae4-105">Los miembros de un grupo se almacenan en un atributo de varios valores denominado **member**.</span><span class="sxs-lookup"><span data-stu-id="5cae4-105">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="5cae4-106">En el caso de los grupos con una pertenencia de tamaño pequeño a medio, use el método [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obtener un puntero a un objeto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contiene la lista de todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="5cae4-106">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="5cae4-107">A continuación, use [**IADsMembers:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obtener un objeto de enumerador que puede usar para enumerar los miembros.</span><span class="sxs-lookup"><span data-stu-id="5cae4-107">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="5cae4-108">Si la pertenencia al grupo esperada será de 1000 o más miembros, use para recuperar los usuarios de un intervalo a la vez.</span><span class="sxs-lookup"><span data-stu-id="5cae4-108">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="5cae4-109">Para obtener más información sobre cómo utilizar el intervalo para enumerar miembros, vea [enumerar grupos que contienen muchos miembros](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="5cae4-109">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 