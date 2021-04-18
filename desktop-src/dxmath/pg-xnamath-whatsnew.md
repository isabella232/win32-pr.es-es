---
description: La biblioteca de DirectXMath se basa en la biblioteca SIMD de C++ matemática de XNA versión 2. x. Aquí se describe el modo en que DirectXMath difiere de la matemáticas de XNA y cómo difieren las versiones de DirectXMath.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novedades (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696711"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="51789-104">Novedades (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="51789-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="51789-105">La biblioteca de DirectXMath se basa en la [versión 2,04 de la biblioteca SIMD de C++ matemática de XNA](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="51789-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="51789-106">Aquí se describe el modo en que DirectXMath difiere de la matemáticas de XNA y cómo difieren las versiones de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="51789-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="51789-107">Historial de Rlease</span><span class="sxs-lookup"><span data-stu-id="51789-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="51789-108">Diferencias de DirectXMath con las matemáticas de XNA</span><span class="sxs-lookup"><span data-stu-id="51789-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="51789-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51789-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="51789-110">Historial de versiones</span><span class="sxs-lookup"><span data-stu-id="51789-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="51789-111">SDK de Windows 10 May 2020 Update</span><span class="sxs-lookup"><span data-stu-id="51789-111">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="51789-112">DirectXMath 3,14</span><span class="sxs-lookup"><span data-stu-id="51789-112">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-113">SDK de la actualización 2018 de octubre de Windows 10</span><span class="sxs-lookup"><span data-stu-id="51789-113">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="51789-114">DirectXMath 3,13</span><span class="sxs-lookup"><span data-stu-id="51789-114">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-115">SDK de la actualización de abril de 2018 de Windows 10</span><span class="sxs-lookup"><span data-stu-id="51789-115">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="51789-116">SDK de Windows 10 Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="51789-116">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="51789-117">DirectXMath 3,11</span><span class="sxs-lookup"><span data-stu-id="51789-117">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-118">SDK de Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="51789-118">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="51789-119">DirectXMath 3,10</span><span class="sxs-lookup"><span data-stu-id="51789-119">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-120">SDK de Windows 10 Anniversary</span><span class="sxs-lookup"><span data-stu-id="51789-120">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="51789-121">DirectXMath 3,09</span><span class="sxs-lookup"><span data-stu-id="51789-121">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-122">SDK de Windows 10 (2015 de noviembre)</span><span class="sxs-lookup"><span data-stu-id="51789-122">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="51789-123">DirectXMath 3,08</span><span class="sxs-lookup"><span data-stu-id="51789-123">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-124">Windows SDK para Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="51789-124">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="51789-125">DirectXMath 3,07</span><span class="sxs-lookup"><span data-stu-id="51789-125">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-126">Windows SDK para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="51789-126">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="51789-127">DirectXMath 3,06</span><span class="sxs-lookup"><span data-stu-id="51789-127">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="51789-128">Windows SDK para Windows 8</span><span class="sxs-lookup"><span data-stu-id="51789-128">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="51789-129">DirectXMath 3,03</span><span class="sxs-lookup"><span data-stu-id="51789-129">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="51789-130">Consulte [versiones de DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="51789-130">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="51789-131">Diferencias de DirectXMath con las matemáticas de XNA</span><span class="sxs-lookup"><span data-stu-id="51789-131">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="51789-132">Aquí se muestra cómo la biblioteca de DirectXMath difiere principalmente de la biblioteca matemática de XNA:</span><span class="sxs-lookup"><span data-stu-id="51789-132">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="51789-133">DirectXMath es solo C++ (espacios de nombres, sobrecargas, nuevas plantillas, etc.).</span><span class="sxs-lookup"><span data-stu-id="51789-133">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="51789-134">Requiere compatibilidad con la biblioteca estándar de C++ 11 (es decir, stdint. h, etc.).</span><span class="sxs-lookup"><span data-stu-id="51789-134">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="51789-135">Compatibilidad con las funciones intrínsecas ARM-neón para la plataforma de Windows RT.</span><span class="sxs-lookup"><span data-stu-id="51789-135">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="51789-136">Nueva funcionalidad de color (conversiones de espacio de colores, constantes de color de .NET).</span><span class="sxs-lookup"><span data-stu-id="51789-136">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="51789-137">Tipos de volumen de límite (una versión de que se encontraba anteriormente en el encabezado XNACollision en el ejemplo de colisión del SDK de DirectX).</span><span class="sxs-lookup"><span data-stu-id="51789-137">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="51789-138">No hay disponible ninguna versión de Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="51789-138">No Xbox 360 version is available.</span></span> <span data-ttu-id="51789-139">La consola Xbox 360 XDK continúa distribuyendo XNAMath V2. x; eliminación de tipos de datos específicos de Xbox 360 y variantes de función.</span><span class="sxs-lookup"><span data-stu-id="51789-139">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="51789-140">[**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) trabajada para optimizar la optimización de los intrínsecos SSE y ARM-neón.</span><span class="sxs-lookup"><span data-stu-id="51789-140">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="51789-141">El tipo [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) es totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="51789-141">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="51789-142">Para tener acceso a elementos individuales de **XMMATRIX**, use otros tipos como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="51789-142">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51789-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51789-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51789-144">Guía de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="51789-144">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="51789-145">Versiones de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="51789-145">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
