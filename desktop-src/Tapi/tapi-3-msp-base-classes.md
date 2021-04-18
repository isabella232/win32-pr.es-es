---
description: En este documento se describe el diseño y el uso de las clases base de MSP. El uso de estas clases no es necesario, pero la mayoría de los desarrolladores encontrarán que simplifican la tarea de crear un MSP basado en DirectShow para TAPI 3S New MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Clases base de TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678358"
---
# <a name="tapi-3-msp-base-classes"></a><span data-ttu-id="cc58b-104">Clases base de TAPI 3 MSP</span><span class="sxs-lookup"><span data-stu-id="cc58b-104">TAPI 3 MSP Base Classes</span></span>

<span data-ttu-id="cc58b-105">En este documento se describe el diseño y el uso de las clases base de MSP.</span><span class="sxs-lookup"><span data-stu-id="cc58b-105">This document describes the design and use of the MSP Base Classes.</span></span> <span data-ttu-id="cc58b-106">El uso de estas clases no es necesario, pero la mayoría de los desarrolladores encontrarán que simplifican la tarea de compilar un MSP nuevo basado en DirectShow para MSPI nuevos de TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="cc58b-106">Use of these classes is not required, but most developers will find they simplify the task of building a DirectShow-based MSP for TAPI 3's new MSPI.</span></span>

<span data-ttu-id="cc58b-107">El código fuente de las clases base MSP se puede encontrar en el directorio Samples del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="cc58b-107">Source code for the MSP base classes can be found in the Samples directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="cc58b-108">Se supone que está familiarizado con COM, ATL, DirectShow y C++.</span><span class="sxs-lookup"><span data-stu-id="cc58b-108">Familiarity with COM, ATL, DirectShow, and C++ is assumed.</span></span> <span data-ttu-id="cc58b-109">El lector también debe conocer el material general de [acerca del proveedor de servicios multimedia (MSP)](about-the-media-service-provider-msp-.md) y de la [interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-.md).</span><span class="sxs-lookup"><span data-stu-id="cc58b-109">The reader must also know the general material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) and in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span></span>

<span data-ttu-id="cc58b-110">ATL 2,1 es necesario para Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cc58b-110">ATL 2.1 is required for Windows 2000.</span></span> <span data-ttu-id="cc58b-111">A partir de Windows XP, se compilarán tanto ATL 2,1 como 3,0.</span><span class="sxs-lookup"><span data-stu-id="cc58b-111">Starting with Windows XP, both ATL 2.1 and 3.0 will compile.</span></span>

<span data-ttu-id="cc58b-112">Bibliotecas de clases base MSP (disponibles en el SDK):</span><span class="sxs-lookup"><span data-stu-id="cc58b-112">MSP Base Class Libraries (available in the SDK):</span></span>

-   <span data-ttu-id="cc58b-113">Mspbase. lib</span><span class="sxs-lookup"><span data-stu-id="cc58b-113">Mspbase.lib</span></span>
-   <span data-ttu-id="cc58b-114">Mspid. lib</span><span class="sxs-lookup"><span data-stu-id="cc58b-114">Mspid.lib</span></span>
-   <span data-ttu-id="cc58b-115">Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="cc58b-115">Strmbase.lib</span></span>
-   <span data-ttu-id="cc58b-116">Tmuid. lib</span><span class="sxs-lookup"><span data-stu-id="cc58b-116">Tmuid.lib</span></span>
    > [!Note]  
    > <span data-ttu-id="cc58b-117">Se debe usar la vinculación dinámica en lugar de estática.</span><span class="sxs-lookup"><span data-stu-id="cc58b-117">Dynamic rather than static linking should be used.</span></span>

     

<span data-ttu-id="cc58b-118">Archivos de encabezado de clase base MSP (disponibles en el SDK):</span><span class="sxs-lookup"><span data-stu-id="cc58b-118">MSP Base Class Header Files (available in the SDK):</span></span>

-   <span data-ttu-id="cc58b-119">Mspaddr. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-119">Mspaddr.h</span></span>
-   <span data-ttu-id="cc58b-120">Mspbase. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-120">Mspbase.h</span></span>
-   <span data-ttu-id="cc58b-121">Mspcall. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-121">Mspcall.h</span></span>
-   <span data-ttu-id="cc58b-122">Msplog. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-122">Msplog.h</span></span>
-   <span data-ttu-id="cc58b-123">Mspstrm. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-123">Mspstrm.h</span></span>
-   <span data-ttu-id="cc58b-124">Mspterm. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-124">Mspterm.h</span></span>
-   <span data-ttu-id="cc58b-125">Mspthrd. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-125">Mspthrd.h</span></span>
-   <span data-ttu-id="cc58b-126">Msptmac. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-126">Msptmac.h</span></span>
-   <span data-ttu-id="cc58b-127">Msptmvc. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-127">Msptmvc.h</span></span>
-   <span data-ttu-id="cc58b-128">Msptrmvc. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-128">Msptrmvc.h</span></span>
-   <span data-ttu-id="cc58b-129">Msptrmac. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-129">Msptrmac.h</span></span>
-   <span data-ttu-id="cc58b-130">Msptrmar. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-130">Msptrmar.h</span></span>
-   <span data-ttu-id="cc58b-131">Msputils. h</span><span class="sxs-lookup"><span data-stu-id="cc58b-131">Msputils.h</span></span>

<span data-ttu-id="cc58b-132">Archivos de origen de la clase base MSP (disponibles en los ejemplos del SDK):</span><span class="sxs-lookup"><span data-stu-id="cc58b-132">MSP Base Class Source Files (available in the SDK Samples):</span></span>

-   <span data-ttu-id="cc58b-133">Mspaddr. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-133">Mspaddr.cpp</span></span>
-   <span data-ttu-id="cc58b-134">Mspcall. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-134">Mspcall.cpp</span></span>
-   <span data-ttu-id="cc58b-135">Msplog. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-135">Msplog.cpp</span></span>
-   <span data-ttu-id="cc58b-136">Mspstrm. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-136">Mspstrm.cpp</span></span>
-   <span data-ttu-id="cc58b-137">Mspterm. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-137">Mspterm.cpp</span></span>
-   <span data-ttu-id="cc58b-138">Mspthrd. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-138">Mspthrd.cpp</span></span>
-   <span data-ttu-id="cc58b-139">Msptrmac. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-139">Msptrmac.cpp</span></span>
-   <span data-ttu-id="cc58b-140">Msptrmar. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-140">Msptrmar.cpp</span></span>
-   <span data-ttu-id="cc58b-141">Msptrmvc. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-141">Msptrmvc.cpp</span></span>
-   <span data-ttu-id="cc58b-142">Msputils. cpp</span><span class="sxs-lookup"><span data-stu-id="cc58b-142">Msputils.cpp</span></span>

 

 



