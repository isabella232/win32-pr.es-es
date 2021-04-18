---
title: Funciones de administración de RAS
description: En esta documentación se describen las funciones RRAS que se usan para desarrollar software para administrar conexiones de acceso telefónico RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357614"
---
# <a name="ras-administration-functions"></a><span data-ttu-id="38cce-103">Funciones de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="38cce-103">RAS Administration Functions</span></span>

<span data-ttu-id="38cce-104">En esta documentación se describen las funciones RRAS que se usan para desarrollar software para administrar conexiones de acceso telefónico RAS.</span><span class="sxs-lookup"><span data-stu-id="38cce-104">This documentation describes RRAS functions that are used to develop software to administer RAS dial-up connections.</span></span> <span data-ttu-id="38cce-105">Estas funciones incluyen:</span><span class="sxs-lookup"><span data-stu-id="38cce-105">These functions include:</span></span>

-   [<span data-ttu-id="38cce-106">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="38cce-106">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [<span data-ttu-id="38cce-107">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="38cce-107">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [<span data-ttu-id="38cce-108">**MprAdminConnectionEnumEx**</span><span class="sxs-lookup"><span data-stu-id="38cce-108">**MprAdminConnectionEnumEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [<span data-ttu-id="38cce-109">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="38cce-109">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [<span data-ttu-id="38cce-110">**MprAdminConnectionGetInfoEx**</span><span class="sxs-lookup"><span data-stu-id="38cce-110">**MprAdminConnectionGetInfoEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [<span data-ttu-id="38cce-111">**MprAdminConnectionRemoveQuarantine**</span><span class="sxs-lookup"><span data-stu-id="38cce-111">**MprAdminConnectionRemoveQuarantine**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [<span data-ttu-id="38cce-112">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="38cce-112">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [<span data-ttu-id="38cce-113">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="38cce-113">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [<span data-ttu-id="38cce-114">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="38cce-114">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [<span data-ttu-id="38cce-115">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="38cce-115">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [<span data-ttu-id="38cce-116">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="38cce-116">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

<span data-ttu-id="38cce-117">Se usan funciones adicionales para la administración de RAS y la administración de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="38cce-117">Additional functions are used for both RAS administration and router administration.</span></span> <span data-ttu-id="38cce-118">Las siguientes funciones documentadas en la referencia de las [funciones de administración del enrutador](router-administration-functions.md) :</span><span class="sxs-lookup"><span data-stu-id="38cce-118">The following functions documented in the [Router Administration Functions](router-administration-functions.md) reference:</span></span>

-   [<span data-ttu-id="38cce-119">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="38cce-119">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [<span data-ttu-id="38cce-120">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="38cce-120">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [<span data-ttu-id="38cce-121">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="38cce-121">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [<span data-ttu-id="38cce-122">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="38cce-122">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [<span data-ttu-id="38cce-123">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="38cce-123">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="38cce-124">Para implementar un archivo DLL de administración de RAS, utilice las funciones descritas en el tema siguiente:</span><span class="sxs-lookup"><span data-stu-id="38cce-124">To implement a RAS administration DLL, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="38cce-125">Funciones de DLL de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="38cce-125">RAS Admin DLL Functions</span></span>](ras-admin-dll-functions.md)

<span data-ttu-id="38cce-126">Para administrar usuarios de un servidor RAS, use las funciones descritas en el tema siguiente:</span><span class="sxs-lookup"><span data-stu-id="38cce-126">To manage users of a RAS server, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="38cce-127">Funciones de administración de usuarios de RAS</span><span class="sxs-lookup"><span data-stu-id="38cce-127">RAS User Administration Functions</span></span>](ras-user-administration-functions.md)

 

 




