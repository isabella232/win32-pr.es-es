---
title: Enumerar miembros de un grupo
description: Obtenga información sobre cómo enumerar los miembros de un Azure Active Directory grupo. Los miembros de un grupo se almacenan en un atributo de varios valores denominado miembro.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerar miembros de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407428"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="c755b-105">Enumerar miembros de un grupo</span><span class="sxs-lookup"><span data-stu-id="c755b-105">Enumerating Members in a Group</span></span>

<span data-ttu-id="c755b-106">Los miembros de un grupo se almacenan en un atributo de varios valores denominado **miembro**.</span><span class="sxs-lookup"><span data-stu-id="c755b-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="c755b-107">En el caso de los grupos con una pertenencia de tamaño pequeño a mediano, use el método [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obtener un puntero a un objeto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contiene la lista de todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="c755b-107">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="c755b-108">A continuación, use [**IADsMembers::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obtener un objeto enumerador que puede usar para enumerar los miembros.</span><span class="sxs-lookup"><span data-stu-id="c755b-108">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="c755b-109">Si la pertenencia a grupos prevista será de 1000 o más miembros, use ranging para recuperar usuarios de un intervalo a la vez.</span><span class="sxs-lookup"><span data-stu-id="c755b-109">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="c755b-110">Para obtener más información sobre el uso de para enumerar miembros, vea [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="c755b-110">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 