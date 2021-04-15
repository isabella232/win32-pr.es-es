---
title: Métodos IBackgroundCopyJob (BITS)
description: La interfaz IBackgroundCopyJob expone los métodos siguientes. | Métodos IBackgroundCopyJob (BITS)
ms.assetid: CB1C6D64-416A-4F31-AC9D-B3C1A6818034
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a7ebeeefa90c90435f1294d78c4816cf77be3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547526"
---
# <a name="ibackgroundcopyjob-methods-bits"></a><span data-ttu-id="cd655-104">Métodos IBackgroundCopyJob (BITS)</span><span class="sxs-lookup"><span data-stu-id="cd655-104">IBackgroundCopyJob Methods (BITS)</span></span>

<span data-ttu-id="cd655-105">La interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="cd655-105">The [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cd655-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cd655-106">In this section</span></span>

-   [<span data-ttu-id="cd655-107">**Método AddFile**</span><span class="sxs-lookup"><span data-stu-id="cd655-107">**AddFile Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
-   [<span data-ttu-id="cd655-108">**Método AddFileSet**</span><span class="sxs-lookup"><span data-stu-id="cd655-108">**AddFileSet Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
-   [<span data-ttu-id="cd655-109">**CANCEL (método)**</span><span class="sxs-lookup"><span data-stu-id="cd655-109">**Cancel Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   [<span data-ttu-id="cd655-110">**Complete (método)**</span><span class="sxs-lookup"><span data-stu-id="cd655-110">**Complete Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
-   [<span data-ttu-id="cd655-111">**Método EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="cd655-111">**EnumFiles Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles)
-   [<span data-ttu-id="cd655-112">**Método GetDescription**</span><span class="sxs-lookup"><span data-stu-id="cd655-112">**GetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdescription)
-   [<span data-ttu-id="cd655-113">**Método GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="cd655-113">**GetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)
-   [<span data-ttu-id="cd655-114">**Método GetError**</span><span class="sxs-lookup"><span data-stu-id="cd655-114">**GetError Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror)
-   [<span data-ttu-id="cd655-115">**Método GetErrorCount**</span><span class="sxs-lookup"><span data-stu-id="cd655-115">**GetErrorCount Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterrorcount)
-   [<span data-ttu-id="cd655-116">**GetId (método)**</span><span class="sxs-lookup"><span data-stu-id="cd655-116">**GetId Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getid)
-   [<span data-ttu-id="cd655-117">**Método GetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="cd655-117">**GetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay)
-   [<span data-ttu-id="cd655-118">**Método GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="cd655-118">**GetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout)
-   [<span data-ttu-id="cd655-119">**Método GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="cd655-119">**GetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyflags)
-   [<span data-ttu-id="cd655-120">**Método GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="cd655-120">**GetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyinterface)
-   [<span data-ttu-id="cd655-121">**Método GetOwner**</span><span class="sxs-lookup"><span data-stu-id="cd655-121">**GetOwner Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)
-   [<span data-ttu-id="cd655-122">**Método GetPriority**</span><span class="sxs-lookup"><span data-stu-id="cd655-122">**GetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getpriority)
-   [<span data-ttu-id="cd655-123">**Método GetProgress**</span><span class="sxs-lookup"><span data-stu-id="cd655-123">**GetProgress Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)
-   [<span data-ttu-id="cd655-124">**Método GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="cd655-124">**GetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getproxysettings)
-   [<span data-ttu-id="cd655-125">**Método GetState**</span><span class="sxs-lookup"><span data-stu-id="cd655-125">**GetState Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate)
-   [<span data-ttu-id="cd655-126">**Método GetTimes**</span><span class="sxs-lookup"><span data-stu-id="cd655-126">**GetTimes Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettimes)
-   [<span data-ttu-id="cd655-127">**Método GetType**</span><span class="sxs-lookup"><span data-stu-id="cd655-127">**GetType Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettype)
-   [<span data-ttu-id="cd655-128">**Resume (método)**</span><span class="sxs-lookup"><span data-stu-id="cd655-128">**Resume Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
-   [<span data-ttu-id="cd655-129">**Método SetDescription**</span><span class="sxs-lookup"><span data-stu-id="cd655-129">**SetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdescription)
-   [<span data-ttu-id="cd655-130">**Método SetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="cd655-130">**SetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdisplayname)
-   [<span data-ttu-id="cd655-131">**Método SetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="cd655-131">**SetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)
-   [<span data-ttu-id="cd655-132">**Método SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="cd655-132">**SetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)
-   [<span data-ttu-id="cd655-133">**Método SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="cd655-133">**SetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)
-   [<span data-ttu-id="cd655-134">**Método SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="cd655-134">**SetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)
-   [<span data-ttu-id="cd655-135">**Método SetPriority**</span><span class="sxs-lookup"><span data-stu-id="cd655-135">**SetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)
-   [<span data-ttu-id="cd655-136">**Método SetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="cd655-136">**SetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)
-   [<span data-ttu-id="cd655-137">**Suspend (método)**</span><span class="sxs-lookup"><span data-stu-id="cd655-137">**Suspend Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)
-   [<span data-ttu-id="cd655-138">**Método TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="cd655-138">**TakeOwnership Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)

 

 




