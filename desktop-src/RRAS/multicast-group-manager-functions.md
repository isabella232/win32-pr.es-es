---
title: Funciones de administrador de grupo de multidifusión
description: Las siguientes funciones se usan para registrar con el administrador del grupo de multidifusión
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357634"
---
# <a name="multicast-group-manager-functions"></a><span data-ttu-id="097e8-103">Funciones de administrador de grupo de multidifusión</span><span class="sxs-lookup"><span data-stu-id="097e8-103">Multicast Group Manager Functions</span></span>

<span data-ttu-id="097e8-104">Las siguientes funciones se usan para registrar con el administrador del grupo de multidifusión:</span><span class="sxs-lookup"><span data-stu-id="097e8-104">The following functions are used to register with the multicast group manager:</span></span>

[<span data-ttu-id="097e8-105">**MgmRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="097e8-105">**MgmRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[<span data-ttu-id="097e8-106">**MgmDeRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="097e8-106">**MgmDeRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

<span data-ttu-id="097e8-107">Las funciones siguientes se usan para administrar la propiedad de la interfaz:</span><span class="sxs-lookup"><span data-stu-id="097e8-107">The following functions are used to manage interface ownership:</span></span>

[<span data-ttu-id="097e8-108">**MgmGetProtocolOnInterface**</span><span class="sxs-lookup"><span data-stu-id="097e8-108">**MgmGetProtocolOnInterface**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[<span data-ttu-id="097e8-109">**MgmTakeInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="097e8-109">**MgmTakeInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[<span data-ttu-id="097e8-110">**MgmReleaseInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="097e8-110">**MgmReleaseInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

<span data-ttu-id="097e8-111">Las funciones siguientes se usan para administrar la pertenencia a grupos:</span><span class="sxs-lookup"><span data-stu-id="097e8-111">The following functions are used to manage group membership:</span></span>

[<span data-ttu-id="097e8-112">**MgmAddGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="097e8-112">**MgmAddGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[<span data-ttu-id="097e8-113">**MgmDeleteGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="097e8-113">**MgmDeleteGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

<span data-ttu-id="097e8-114">Las siguientes funciones se usan para obtener entradas de reenvío de multidifusión (MFEs) y estadísticas de MFE:</span><span class="sxs-lookup"><span data-stu-id="097e8-114">The following functions are used to obtain multicast forwarding entries (MFEs) and MFE statistics:</span></span>

[<span data-ttu-id="097e8-115">**MgmGetFirstMfe**</span><span class="sxs-lookup"><span data-stu-id="097e8-115">**MgmGetFirstMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[<span data-ttu-id="097e8-116">**MgmGetNextMfe**</span><span class="sxs-lookup"><span data-stu-id="097e8-116">**MgmGetNextMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[<span data-ttu-id="097e8-117">**MgmGetMfe**</span><span class="sxs-lookup"><span data-stu-id="097e8-117">**MgmGetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[<span data-ttu-id="097e8-118">**MgmGetFirstMfeStats**</span><span class="sxs-lookup"><span data-stu-id="097e8-118">**MgmGetFirstMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[<span data-ttu-id="097e8-119">**MgmGetNextMfeStats**</span><span class="sxs-lookup"><span data-stu-id="097e8-119">**MgmGetNextMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[<span data-ttu-id="097e8-120">**MgmGetMfeStats**</span><span class="sxs-lookup"><span data-stu-id="097e8-120">**MgmGetMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

<span data-ttu-id="097e8-121">La siguiente función se usa para modificar MFEs:</span><span class="sxs-lookup"><span data-stu-id="097e8-121">The following function is used to modify MFEs:</span></span>

[<span data-ttu-id="097e8-122">**MgmSetMfe**</span><span class="sxs-lookup"><span data-stu-id="097e8-122">**MgmSetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

<span data-ttu-id="097e8-123">Las siguientes funciones se usan para obtener una lista de los grupos que se han unido:</span><span class="sxs-lookup"><span data-stu-id="097e8-123">The following functions are used obtain a list of groups that have been joined:</span></span>

[<span data-ttu-id="097e8-124">**MgmGroupEnumerationStart**</span><span class="sxs-lookup"><span data-stu-id="097e8-124">**MgmGroupEnumerationStart**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[<span data-ttu-id="097e8-125">**MgmGroupEnumerationGetNext**</span><span class="sxs-lookup"><span data-stu-id="097e8-125">**MgmGroupEnumerationGetNext**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[<span data-ttu-id="097e8-126">**MgmGroupEnumerationEnd**</span><span class="sxs-lookup"><span data-stu-id="097e8-126">**MgmGroupEnumerationEnd**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




