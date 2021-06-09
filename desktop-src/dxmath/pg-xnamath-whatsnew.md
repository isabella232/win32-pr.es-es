---
description: La biblioteca DirectXMath se basa en la versión 2.x de la biblioteca SIMD de C++ matemática de XNA. Aquí se describe cómo se diferencia DirectXMath de XNA Math y cómo difieren las versiones de DirectXMath.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novedades (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827631"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="41bd0-104">Novedades (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="41bd0-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="41bd0-105">La biblioteca DirectXMath se basa en la versión [2.04](https://walbourn.github.io/xna-math-version-2-04/)de la biblioteca SIMD de C++ matemática de XNA.</span><span class="sxs-lookup"><span data-stu-id="41bd0-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span></span> <span data-ttu-id="41bd0-106">Aquí se describe cómo se diferencia DirectXMath de XNA Math y cómo difieren las versiones de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="41bd0-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="41bd0-107">Historial de versión preliminar</span><span class="sxs-lookup"><span data-stu-id="41bd0-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="41bd0-108">Diferencias de DirectXMath con respecto a XNA Math</span><span class="sxs-lookup"><span data-stu-id="41bd0-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="41bd0-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41bd0-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="41bd0-110">Historial de versiones</span><span class="sxs-lookup"><span data-stu-id="41bd0-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="41bd0-111">Windows 10 SDK (20348), versión 2104</span><span class="sxs-lookup"><span data-stu-id="41bd0-111">Windows 10 SDK (20348), version 2104</span></span></td><td><span data-ttu-id="41bd0-112">DirectXMath 3.16</span><span class="sxs-lookup"><span data-stu-id="41bd0-112">DirectXMath 3.16</span></span></td>
 </td>
 <tr>
  <td><span data-ttu-id="41bd0-113">Windows 10 SDK de actualización de mayo de 2020</span><span class="sxs-lookup"><span data-stu-id="41bd0-113">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="41bd0-114">DirectXMath 3.14</span><span class="sxs-lookup"><span data-stu-id="41bd0-114">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-115">ACTUALIZACIÓN DE OCTUBRE DE 2018 DE WINDOWS 10 SDK</span><span class="sxs-lookup"><span data-stu-id="41bd0-115">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="41bd0-116">DirectXMath 3.13</span><span class="sxs-lookup"><span data-stu-id="41bd0-116">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-117">ACTUALIZACIÓN DE ABRIL DE 2018 DE WINDOWS 10 SDK</span><span class="sxs-lookup"><span data-stu-id="41bd0-117">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="41bd0-118">Windows 10 Fall Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="41bd0-118">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="41bd0-119">DirectXMath 3.11</span><span class="sxs-lookup"><span data-stu-id="41bd0-119">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-120">Windows 10 Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="41bd0-120">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="41bd0-121">DirectXMath 3.10</span><span class="sxs-lookup"><span data-stu-id="41bd0-121">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-122">SDK de Windows 10 Anniversary</span><span class="sxs-lookup"><span data-stu-id="41bd0-122">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="41bd0-123">DirectXMath 3.09</span><span class="sxs-lookup"><span data-stu-id="41bd0-123">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-124">Windows 10 SDK (noviembre de 2015)</span><span class="sxs-lookup"><span data-stu-id="41bd0-124">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="41bd0-125">DirectXMath 3.08</span><span class="sxs-lookup"><span data-stu-id="41bd0-125">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-126">Windows SDK para Windows 8.1 (spring 2015)</span><span class="sxs-lookup"><span data-stu-id="41bd0-126">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="41bd0-127">DirectXMath 3.07</span><span class="sxs-lookup"><span data-stu-id="41bd0-127">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-128">Windows SDK para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41bd0-128">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="41bd0-129">DirectXMath 3.06</span><span class="sxs-lookup"><span data-stu-id="41bd0-129">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="41bd0-130">Windows SDK para Windows 8</span><span class="sxs-lookup"><span data-stu-id="41bd0-130">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="41bd0-131">DirectXMath 3.03</span><span class="sxs-lookup"><span data-stu-id="41bd0-131">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="41bd0-132">Consulte [Versiones de DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="41bd0-132">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="41bd0-133">Diferencias de DirectXMath con respecto a XNA Math</span><span class="sxs-lookup"><span data-stu-id="41bd0-133">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="41bd0-134">Este es el modo en que la biblioteca DirectXMath difiere principalmente de la biblioteca matemática de XNA:</span><span class="sxs-lookup"><span data-stu-id="41bd0-134">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="41bd0-135">DirectXMath es solo C++ (espacios de nombres, sobrecargas, nuevas plantillas, entre otros).</span><span class="sxs-lookup"><span data-stu-id="41bd0-135">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="41bd0-136">Requiere compatibilidad con la biblioteca estándar de C++11 (es decir, stdint.h, y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="41bd0-136">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="41bd0-137">Compatibilidad intrínseca de ARM-NEON con la plataforma Windows RT sistema.</span><span class="sxs-lookup"><span data-stu-id="41bd0-137">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="41bd0-138">Nueva funcionalidad de color (conversiones de espacio de color, constantes de color de .NET).</span><span class="sxs-lookup"><span data-stu-id="41bd0-138">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="41bd0-139">Límite de tipos de volumen (una versión de la que se encontraba anteriormente en el encabezado XNACollision en el ejemplo de colisión del SDK de DirectX).</span><span class="sxs-lookup"><span data-stu-id="41bd0-139">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="41bd0-140">No hay Xbox 360 versión disponible.</span><span class="sxs-lookup"><span data-stu-id="41bd0-140">No Xbox 360 version is available.</span></span> <span data-ttu-id="41bd0-141">El Xbox 360 XDK continúa con el envío de XNAMath v2.x; eliminación de Xbox 360 tipos de datos y variantes de función específicos.</span><span class="sxs-lookup"><span data-stu-id="41bd0-141">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="41bd0-142">[**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) se ha reelatrado para mejorar la optimización de los intrínsecos SSE y ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="41bd0-142">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="41bd0-143">El [**tipo XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) es totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="41bd0-143">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="41bd0-144">Para acceder a elementos individuales **de XMMATRIX,** use otros tipos como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="41bd0-144">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41bd0-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41bd0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41bd0-146">Guía de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="41bd0-146">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="41bd0-147">Versiones de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="41bd0-147">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
