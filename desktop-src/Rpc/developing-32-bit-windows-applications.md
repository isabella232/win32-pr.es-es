---
title: Desarrollo de aplicaciones de RPC para Windows
description: Al instalar el kit de desarrollo de software (SDK) de la plataforma, el entorno de desarrollo de RPC siguiente, las bibliotecas en tiempo de ejecución y las herramientas se instalan automáticamente.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078259"
---
# <a name="developing-rpc-windows-applications"></a><span data-ttu-id="c013f-103">Desarrollo de aplicaciones de RPC para Windows</span><span class="sxs-lookup"><span data-stu-id="c013f-103">Developing RPC Windows Applications</span></span>

<span data-ttu-id="c013f-104">Al instalar el kit de desarrollo de software (SDK) de la plataforma, se instalan automáticamente el siguiente entorno de desarrollo de RPC, las bibliotecas en tiempo de ejecución y las herramientas:</span><span class="sxs-lookup"><span data-stu-id="c013f-104">When you install the Platform Software Development Kit (SDK), the following RPC development environment, the run-time libraries, and tools are automatically installed:</span></span>

-   <span data-ttu-id="c013f-105">Encabezado del lenguaje C/C++ (. H) archivos</span><span class="sxs-lookup"><span data-stu-id="c013f-105">C/C++ language header (.H) files</span></span>
-   <span data-ttu-id="c013f-106">Archivos de bibliotecas de importación (. lib) de RPC</span><span class="sxs-lookup"><span data-stu-id="c013f-106">RPC import libraries (.lib) files</span></span>
-   <span data-ttu-id="c013f-107">Programas de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c013f-107">Sample programs</span></span>
-   <span data-ttu-id="c013f-108">Archivos de ayuda de referencia de RPC</span><span class="sxs-lookup"><span data-stu-id="c013f-108">RPC reference Help files</span></span>
-   <span data-ttu-id="c013f-109">La utilidad **uuidgen**</span><span class="sxs-lookup"><span data-stu-id="c013f-109">The **uuidgen** utility</span></span>

<span data-ttu-id="c013f-110">Al instalar Windows, se instala lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c013f-110">When you install Windows, the following are installed:</span></span>

-   <span data-ttu-id="c013f-111">Dll en tiempo de ejecución de RPC</span><span class="sxs-lookup"><span data-stu-id="c013f-111">RPC Run-time DLLs</span></span>
-   <span data-ttu-id="c013f-112">Microsoft Locator (no se admite en Windows Vista y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="c013f-112">Microsoft Locator (not supported on Windows Vista and later)</span></span>
-   <span data-ttu-id="c013f-113">Extremo RPC: servicios de asignación</span><span class="sxs-lookup"><span data-stu-id="c013f-113">RPC Endpoint-mapping services</span></span>

<span data-ttu-id="c013f-114">Las siguientes bibliotecas de importación de RPC.</span><span class="sxs-lookup"><span data-stu-id="c013f-114">The following RPC import libraries.</span></span>



| <span data-ttu-id="c013f-115">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="c013f-115">Import library</span></span> | <span data-ttu-id="c013f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c013f-116">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="c013f-117">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="c013f-117">Rpcns4.lib</span></span>     | <span data-ttu-id="c013f-118">Funciones de servicio de nombre</span><span class="sxs-lookup"><span data-stu-id="c013f-118">Name-service functions</span></span>     |
| <span data-ttu-id="c013f-119">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="c013f-119">Rpcrt4.lib</span></span>     | <span data-ttu-id="c013f-120">Funciones en tiempo de ejecución de Windows</span><span class="sxs-lookup"><span data-stu-id="c013f-120">Windows run-time functions</span></span> |



 

> [!Note]  
> <span data-ttu-id="c013f-121">Rpcns4. lib está obsoleto y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="c013f-121">Rpcns4.lib is obsolete and no longer supported.</span></span>

 

<span data-ttu-id="c013f-122">Las siguientes bibliotecas de RPC se incluyen para la compatibilidad de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="c013f-122">The following RPC libraries are included for down-level support.</span></span>



| <span data-ttu-id="c013f-123">Biblioteca de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="c013f-123">Dynamic-link library</span></span> | <span data-ttu-id="c013f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c013f-124">Description</span></span>                 | <span data-ttu-id="c013f-125">Plataforma</span><span class="sxs-lookup"><span data-stu-id="c013f-125">Platform</span></span>                           |
|----------------------|-----------------------------|------------------------------------|
| <span data-ttu-id="c013f-126">Rpcltc1.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-126">Rpcltc1.dll</span></span>          | <span data-ttu-id="c013f-127">Transporte de canalización con nombre de cliente</span><span class="sxs-lookup"><span data-stu-id="c013f-127">Client named-pipe transport</span></span> | <span data-ttu-id="c013f-128">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-128">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-129">Rpclts1.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-129">Rpclts1.dll</span></span>          | <span data-ttu-id="c013f-130">Transporte de canalización con nombre de servidor</span><span class="sxs-lookup"><span data-stu-id="c013f-130">Server named-pipe transport</span></span> | <span data-ttu-id="c013f-131">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-131">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-132">Rpcltc3.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-132">Rpcltc3.dll</span></span>          | <span data-ttu-id="c013f-133">Transporte TCP/IP de cliente</span><span class="sxs-lookup"><span data-stu-id="c013f-133">Client TCP/IP transport</span></span>     | <span data-ttu-id="c013f-134">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-134">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-135">Rpclts3.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-135">Rpclts3.dll</span></span>          | <span data-ttu-id="c013f-136">Transporte TCP/IP del servidor</span><span class="sxs-lookup"><span data-stu-id="c013f-136">Server TCP/IP transport</span></span>     | <span data-ttu-id="c013f-137">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-137">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-138">Rpcltc5.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-138">Rpcltc5.dll</span></span>          | <span data-ttu-id="c013f-139">Transporte NetBIOS de cliente</span><span class="sxs-lookup"><span data-stu-id="c013f-139">Client NetBIOS transport</span></span>    | <span data-ttu-id="c013f-140">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-140">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-141">Rpclts5.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-141">Rpclts5.dll</span></span>          | <span data-ttu-id="c013f-142">Transporte NetBIOS de servidor</span><span class="sxs-lookup"><span data-stu-id="c013f-142">Server NetBIOS transport</span></span>    | <span data-ttu-id="c013f-143">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-143">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-144">Rpcltc6.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-144">Rpcltc6.dll</span></span>          | <span data-ttu-id="c013f-145">Transporte de cliente SPX</span><span class="sxs-lookup"><span data-stu-id="c013f-145">Client SPX transport</span></span>        | <span data-ttu-id="c013f-146">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-146">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-147">Rpclts6.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-147">Rpclts6.dll</span></span>          | <span data-ttu-id="c013f-148">Transporte de servidor SPX</span><span class="sxs-lookup"><span data-stu-id="c013f-148">Server SPX transport</span></span>        | <span data-ttu-id="c013f-149">Windows NT, Windows 98 y Windows 95</span><span class="sxs-lookup"><span data-stu-id="c013f-149">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="c013f-150">Rpcdgc6.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-150">Rpcdgc6.dll</span></span>          | <span data-ttu-id="c013f-151">Transporte IPX de cliente</span><span class="sxs-lookup"><span data-stu-id="c013f-151">Client IPX transport</span></span>        | <span data-ttu-id="c013f-152">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c013f-152">Windows NT</span></span>                         |
| <span data-ttu-id="c013f-153">Rpcdgs6.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-153">Rpcdgs6.dll</span></span>          | <span data-ttu-id="c013f-154">Transporte de servidor IPX</span><span class="sxs-lookup"><span data-stu-id="c013f-154">Server IPX transport</span></span>        | <span data-ttu-id="c013f-155">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c013f-155">Windows NT</span></span>                         |
| <span data-ttu-id="c013f-156">Rpcdgc3.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-156">Rpcdgc3.dll</span></span>          | <span data-ttu-id="c013f-157">Transporte UDP de cliente</span><span class="sxs-lookup"><span data-stu-id="c013f-157">Client UDP transport</span></span>        | <span data-ttu-id="c013f-158">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c013f-158">Windows NT</span></span>                         |
| <span data-ttu-id="c013f-159">Rpcdgs3.dll</span><span class="sxs-lookup"><span data-stu-id="c013f-159">Rpcdgs3.dll</span></span>          | <span data-ttu-id="c013f-160">Transporte UDP de servidor</span><span class="sxs-lookup"><span data-stu-id="c013f-160">Server UDP transport</span></span>        | <span data-ttu-id="c013f-161">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c013f-161">Windows NT</span></span>                         |



 

<span data-ttu-id="c013f-162">También necesitará el compilador Lenguaje de definición de interfaz de Microsoft (MIDL).</span><span class="sxs-lookup"><span data-stu-id="c013f-162">You will also need the Microsoft Interface Definition Language (MIDL) compiler.</span></span> <span data-ttu-id="c013f-163">Para obtener más información, vea [usar el compilador de MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).</span><span class="sxs-lookup"><span data-stu-id="c013f-163">For more information, see [Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span></span>

 

 