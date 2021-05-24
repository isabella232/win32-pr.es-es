---
description: Los sistemas de coordenadas para Direct3D 10 se definen para píxeles y texturas.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemas de coordenadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3da846ae4b989f6d8cb4741f9df8f7228e8970
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335469"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="9880a-103">Sistemas de coordenadas (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9880a-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="9880a-104">Los sistemas de coordenadas para Direct3D 10 se definen para píxeles y texturas.</span><span class="sxs-lookup"><span data-stu-id="9880a-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



<span data-ttu-id="9880a-105">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="9880a-105">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="9880a-106">Direct3D 10 define la esquina superior izquierda del píxel superior izquierdo como el origen de un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="9880a-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span>
- <span data-ttu-id="9880a-107">Direct3D 9 define el centro del píxel superior izquierdo como el origen de un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="9880a-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span>



 

[<span data-ttu-id="9880a-108">Sistema de coordenadas de píxeles</span><span class="sxs-lookup"><span data-stu-id="9880a-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
- [<span data-ttu-id="9880a-109">Sistema de coordenadas de píxeles para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="9880a-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)

[<span data-ttu-id="9880a-110">Sistema de coordenadas de Texel</span><span class="sxs-lookup"><span data-stu-id="9880a-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
- [<span data-ttu-id="9880a-111">Sistema de coordenadas de Texel</span><span class="sxs-lookup"><span data-stu-id="9880a-111">Texel Coordinate System</span></span>](#texel-coordinate-system)

[<span data-ttu-id="9880a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9880a-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="9880a-113">Sistema de coordenadas de píxeles</span><span class="sxs-lookup"><span data-stu-id="9880a-113">Pixel Coordinate System</span></span>

<span data-ttu-id="9880a-114">El sistema de coordenadas de píxeles de Direct3D 10 define el origen de un destino de representación en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="9880a-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="9880a-115">como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="9880a-115">as shown in the following diagram.</span></span> <span data-ttu-id="9880a-116">Los centros de píxeles se desplazan por (0,5f,0,5f) desde ubicaciones de enteros.</span><span class="sxs-lookup"><span data-stu-id="9880a-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![diagrama del sistema de coordenadas de píxeles en direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="9880a-118">Sistema de coordenadas de píxeles para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="9880a-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="9880a-119">Como referencia, este es el sistema de coordenadas de píxeles para Direct3D 9, que definió el origen o un destino de representación como el centro del píxel superior izquierdo ,(0,5,0,5) fuera de la esquina superior izquierda, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="9880a-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="9880a-120">En Direct3D 9, los centros de píxeles están en ubicaciones enteras.</span><span class="sxs-lookup"><span data-stu-id="9880a-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![diagrama del sistema de coordenadas de píxeles en direct3d 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="9880a-122">Sistema de coordenadas de Texel</span><span class="sxs-lookup"><span data-stu-id="9880a-122">Texel Coordinate System</span></span>

<span data-ttu-id="9880a-123">El sistema de coordenadas de texel tiene su origen en la esquina superior izquierda de la textura, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="9880a-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="9880a-124">Esto hace que la representación de texturas alineadas con la pantalla sea trivial (en Direct3D 10), ya que el sistema de coordenadas de píxeles está alineado con el sistema de coordenadas de texel.</span><span class="sxs-lookup"><span data-stu-id="9880a-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![diagrama del sistema de coordenadas de texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="9880a-126">Sistema de coordenadas de Texel</span><span class="sxs-lookup"><span data-stu-id="9880a-126">Texel Coordinate System</span></span>

<span data-ttu-id="9880a-127">Las coordenadas de textura se representan con un número normalizado o escalado; Cada coordenada de textura se asigna a un elemento de textura específico como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="9880a-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="9880a-128">Para una coordenada normalizada:</span><span class="sxs-lookup"><span data-stu-id="9880a-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="9880a-129">Muestreo de punto: Texel \# = floor(U \* Width)</span><span class="sxs-lookup"><span data-stu-id="9880a-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="9880a-130">Muestreo lineal: Texel izquierdo \# = floor(U \* Width), Right Texel \# = Left Texel + \# 1</span><span class="sxs-lookup"><span data-stu-id="9880a-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="9880a-131">Para una coordenada a escala:</span><span class="sxs-lookup"><span data-stu-id="9880a-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="9880a-132">Muestreo de punto: Texel \# = floor(U)</span><span class="sxs-lookup"><span data-stu-id="9880a-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="9880a-133">Muestreo lineal: Texel izquierdo \# = floor(U - 0,5), Right Texel \# = Left Texel + \# 1</span><span class="sxs-lookup"><span data-stu-id="9880a-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="9880a-134">Donde el ancho es el ancho de la textura (en texturas).</span><span class="sxs-lookup"><span data-stu-id="9880a-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="9880a-135">El ajuste de la dirección de textura se produce después de calcular la ubicación del texel.</span><span class="sxs-lookup"><span data-stu-id="9880a-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9880a-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9880a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9880a-137">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9880a-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




