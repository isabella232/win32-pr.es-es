---
title: Funciones de grupo
description: Un grupo global contiene cuentas de usuario de un dominio que se agrupan en un nombre de cuenta de grupo.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421236"
---
# <a name="group-functions"></a><span data-ttu-id="10deb-103">Funciones de grupo</span><span class="sxs-lookup"><span data-stu-id="10deb-103">Group Functions</span></span>

<span data-ttu-id="10deb-104">Un *grupo global* contiene cuentas de usuario de un dominio que se agrupan en un nombre de cuenta de grupo.</span><span class="sxs-lookup"><span data-stu-id="10deb-104">A *global group* contains user accounts from one domain that are grouped together under one group account name.</span></span> <span data-ttu-id="10deb-105">Un grupo global solo puede contener miembros (usuarios) del dominio en el que se crea el grupo global; no puede contener grupos locales.</span><span class="sxs-lookup"><span data-stu-id="10deb-105">A global group can contain only members (users) from the domain where the global group is created; it cannot contain local groups.</span></span> <span data-ttu-id="10deb-106">Un grupo global está disponible dentro de su propio dominio y dentro de cualquier dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="10deb-106">A global group is available within its own domain and within any trusting domain.</span></span>

<span data-ttu-id="10deb-107">Las funciones de grupo de administración de red controlan los grupos globales.</span><span class="sxs-lookup"><span data-stu-id="10deb-107">The network management group functions control global groups.</span></span> <span data-ttu-id="10deb-108">A continuación se enumeran las funciones de grupo.</span><span class="sxs-lookup"><span data-stu-id="10deb-108">The group functions are listed following.</span></span>



| <span data-ttu-id="10deb-109">Función</span><span class="sxs-lookup"><span data-stu-id="10deb-109">Function</span></span>                                     | <span data-ttu-id="10deb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="10deb-110">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="10deb-111">**NetGroupAdd**</span><span class="sxs-lookup"><span data-stu-id="10deb-111">**NetGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | <span data-ttu-id="10deb-112">Crea un grupo global.</span><span class="sxs-lookup"><span data-stu-id="10deb-112">Creates a global group.</span></span>                                                           |
| [<span data-ttu-id="10deb-113">**NetGroupAddUser**</span><span class="sxs-lookup"><span data-stu-id="10deb-113">**NetGroupAddUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | <span data-ttu-id="10deb-114">Agrega un usuario a un grupo global existente.</span><span class="sxs-lookup"><span data-stu-id="10deb-114">Adds one user to an existing global group.</span></span>                                        |
| [<span data-ttu-id="10deb-115">**NetGroupDel**</span><span class="sxs-lookup"><span data-stu-id="10deb-115">**NetGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | <span data-ttu-id="10deb-116">Quita un grupo global tanto si el grupo tiene como si no.</span><span class="sxs-lookup"><span data-stu-id="10deb-116">Removes a global group whether or not the group has any members.</span></span>                  |
| [<span data-ttu-id="10deb-117">**NetGroupDelUser**</span><span class="sxs-lookup"><span data-stu-id="10deb-117">**NetGroupDelUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | <span data-ttu-id="10deb-118">Quita un nombre de usuario de un grupo global.</span><span class="sxs-lookup"><span data-stu-id="10deb-118">Removes one user name from a global group.</span></span>                                        |
| [<span data-ttu-id="10deb-119">**NetGroupEnum**</span><span class="sxs-lookup"><span data-stu-id="10deb-119">**NetGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | <span data-ttu-id="10deb-120">Enumera todos los grupos globales en un servidor.</span><span class="sxs-lookup"><span data-stu-id="10deb-120">Lists all global groups on a server.</span></span>                                              |
| [<span data-ttu-id="10deb-121">**NetGroupGetInfo**</span><span class="sxs-lookup"><span data-stu-id="10deb-121">**NetGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | <span data-ttu-id="10deb-122">Devuelve información sobre un grupo global determinado.</span><span class="sxs-lookup"><span data-stu-id="10deb-122">Returns information about a particular global group.</span></span>                              |
| [<span data-ttu-id="10deb-123">**NetGroupGetUsers**</span><span class="sxs-lookup"><span data-stu-id="10deb-123">**NetGroupGetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | <span data-ttu-id="10deb-124">Enumera todos los miembros de un grupo global determinado.</span><span class="sxs-lookup"><span data-stu-id="10deb-124">Lists all members of a particular global group.</span></span>                                   |
| [<span data-ttu-id="10deb-125">**NetGroupSetInfo**</span><span class="sxs-lookup"><span data-stu-id="10deb-125">**NetGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | <span data-ttu-id="10deb-126">Establece información general sobre un grupo global.</span><span class="sxs-lookup"><span data-stu-id="10deb-126">Sets general information about a global group.</span></span>                                    |
| [<span data-ttu-id="10deb-127">**NetGroupSetUsers**</span><span class="sxs-lookup"><span data-stu-id="10deb-127">**NetGroupSetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | <span data-ttu-id="10deb-128">Asigna miembros a un nuevo grupo global; reemplaza los miembros de un grupo existente.</span><span class="sxs-lookup"><span data-stu-id="10deb-128">Assigns members to a new global group; replaces the members of an existing group.</span></span> |



 

<span data-ttu-id="10deb-129">Cuando llame a la función [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) para crear un grupo global, debe proporcionar un nombre de grupo.</span><span class="sxs-lookup"><span data-stu-id="10deb-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span></span> <span data-ttu-id="10deb-130">Inicialmente, un nuevo grupo no tiene miembros.</span><span class="sxs-lookup"><span data-stu-id="10deb-130">Initially, a new group has no members.</span></span>

<span data-ttu-id="10deb-131">Las cuentas de usuario pertenecen automáticamente a los usuarios del dominio del grupo global especial.</span><span class="sxs-lookup"><span data-stu-id="10deb-131">User accounts automatically belong to the special global group Domain Users.</span></span> <span data-ttu-id="10deb-132">La pertenencia a este grupo se controla indirectamente mediante las funciones [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)y [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="10deb-132">Membership in this group is indirectly controlled by the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions.</span></span>

<span data-ttu-id="10deb-133">La información de la cuenta de grupo global está disponible en los siguientes niveles:</span><span class="sxs-lookup"><span data-stu-id="10deb-133">Global group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="10deb-134">**Información de grupo \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="10deb-134">**GROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [<span data-ttu-id="10deb-135">**Información de grupo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="10deb-135">**GROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [<span data-ttu-id="10deb-136">**Información de grupo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="10deb-136">**GROUP\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [<span data-ttu-id="10deb-137">**Información del grupo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="10deb-137">**GROUP\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [<span data-ttu-id="10deb-138">**Información de grupo \_ \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="10deb-138">**GROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [<span data-ttu-id="10deb-139">**Información de grupo \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="10deb-139">**GROUP\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

<span data-ttu-id="10deb-140">Los niveles 1002 y 1005 solo son válidos para la función [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .</span><span class="sxs-lookup"><span data-stu-id="10deb-140">The 1002 and 1005 levels are valid only for the [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) function.</span></span>

<span data-ttu-id="10deb-141">La información de los miembros del grupo global está disponible en el siguiente nivel de información:</span><span class="sxs-lookup"><span data-stu-id="10deb-141">Global group member information is available at the following information level:</span></span>

-   [<span data-ttu-id="10deb-142">**Información de usuarios del grupo \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="10deb-142">**GROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

<span data-ttu-id="10deb-143">Para obtener más información, consulte funciones de [grupo local](local-group-functions.md)de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="10deb-143">For more information, see the network management [Local Group Functions](local-group-functions.md).</span></span>

<span data-ttu-id="10deb-144">Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones del grupo de administración de red.</span><span class="sxs-lookup"><span data-stu-id="10deb-144">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions.</span></span> <span data-ttu-id="10deb-145">Para obtener más información, vea [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span><span class="sxs-lookup"><span data-stu-id="10deb-145">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 