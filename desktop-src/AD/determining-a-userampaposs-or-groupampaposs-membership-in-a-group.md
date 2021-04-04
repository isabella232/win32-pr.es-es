---
title: Determinar la pertenencia de un usuario o un grupo a un grupo
description: El método IADsGroup. IsMember se puede usar para determinar si un objeto es miembro de un grupo.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Determinar la pertenencia de un usuario o un grupo a un grupo de AD
- agrupa AD, determinar la pertenencia de un usuario o un grupo a un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077531"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a><span data-ttu-id="0924b-105">Determinar la pertenencia de un usuario o un grupo a un grupo</span><span class="sxs-lookup"><span data-stu-id="0924b-105">Determining a User's or Group's Membership in a Group</span></span>

<span data-ttu-id="0924b-106">El método [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) se puede usar para determinar si un objeto es miembro de un grupo.</span><span class="sxs-lookup"><span data-stu-id="0924b-106">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method can be used to determine if an object is a member of a group.</span></span> <span data-ttu-id="0924b-107">Este método devuelve **true** si el objeto especificado es un miembro directo del grupo, es decir, la propiedad de miembro del grupo contiene el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="0924b-107">This method returns **TRUE** if the specified object is a direct member of the group, that is, the group's member property contains the specified object.</span></span>

<span data-ttu-id="0924b-108">Un grupo puede contener otros grupos.</span><span class="sxs-lookup"><span data-stu-id="0924b-108">A group can contain other groups.</span></span> <span data-ttu-id="0924b-109">El método [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) no comprueba de forma recursiva los miembros de los grupos en su propiedad de miembro, los grupos dentro de esos grupos, etc.</span><span class="sxs-lookup"><span data-stu-id="0924b-109">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method does not recursively verify the members of groups in its member property, groups within those groups, and so on.</span></span> <span data-ttu-id="0924b-110">Para comprobar de forma recursiva que un objeto es miembro de un grupo, enumere los grupos en la propiedad de miembro, compruebe los miembros de esos grupos para ver si el objeto es un miembro, y si esos grupos contienen otros grupos, compruebe sus miembros, etc.</span><span class="sxs-lookup"><span data-stu-id="0924b-110">To recursively verify that an object is a member of a group, enumerate the groups in the member property, verify the members of those groups to see if the object is a member, and if those groups contain other groups, check their members, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="0924b-111">Dado que los grupos se pueden anidar, la pertenencia a grupos puede tener bucles.</span><span class="sxs-lookup"><span data-stu-id="0924b-111">Since groups can be nested, group membership may have loops.</span></span> <span data-ttu-id="0924b-112">Cualquier script que Enumere muchos grupos debe mantener una lista interna de grupos para finalizar la recursividad si ya se ha visitado un grupo.</span><span class="sxs-lookup"><span data-stu-id="0924b-112">Any script that enumerates over many groups should keep an internal list of groups to end recursion if a group has already been visited.</span></span>

 

 

 