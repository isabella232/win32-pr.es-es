---
title: Efecto Rotatation de matiz
description: Use el efecto girar matiz para modificar el matiz de una imagen aplicando una matriz de colores basada en el ángulo de rotación.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- efecto Rotatation de matiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104565405"
---
# <a name="hue-rotatation-effect"></a><span data-ttu-id="8e5e3-104">Efecto Rotatation de matiz</span><span class="sxs-lookup"><span data-stu-id="8e5e3-104">Hue rotatation effect</span></span>

<span data-ttu-id="8e5e3-105">Use el efecto girar matiz para modificar el matiz de una imagen aplicando una matriz de colores basada en el ángulo de rotación.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-105">Use the hue rotate effect to alter the hue of an image by applying a color matrix based on the rotation angle.</span></span>

<span data-ttu-id="8e5e3-106">El CLSID para este efecto es CLSID \_ D2D1HueRotation.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-106">The CLSID for this effect is CLSID\_D2D1HueRotation.</span></span>

-   [<span data-ttu-id="8e5e3-107">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e5e3-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="8e5e3-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8e5e3-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="8e5e3-109">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8e5e3-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="8e5e3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e5e3-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8e5e3-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e5e3-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="8e5e3-112">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e5e3-112">Example image</span></span>

<span data-ttu-id="8e5e3-113">En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto rotar matiz con un ángulo de giro de 270 grados.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-113">The example here shows the input and output images of the hue rotate effect with a rotation angle of 270 degrees.</span></span>



| <span data-ttu-id="8e5e3-114">Antes</span><span class="sxs-lookup"><span data-stu-id="8e5e3-114">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)   |
| <span data-ttu-id="8e5e3-116">Después</span><span class="sxs-lookup"><span data-stu-id="8e5e3-116">After</span></span>                                                        |
| ![la imagen después de la transformación.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="8e5e3-118">El efecto calcula una matriz de colores basándose en el ángulo de rotación (*?*) que se especifica con la propiedad de ángulo de propiedades de D2D1 \_ HUEROTATION \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8e5e3-118">The effect calculates a color matrix based on the rotation angle (*?*) you specify with the D2D1\_HUEROTATION\_PROP\_ANGLE property.</span></span> <span data-ttu-id="8e5e3-119">Estas son las ecuaciones de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-119">Here are the matrix equations.</span></span>

![cálculos de rotación de matiz](images/hue-formula.png)

<span data-ttu-id="8e5e3-121">La matriz creada depende solo del ángulo de rotación.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-121">The matrix created depends only on the rotation angle.</span></span> <span data-ttu-id="8e5e3-122">Puede usar el efecto de la [matriz de colores](color-matrix.md) si necesita una matriz específica.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="8e5e3-123">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8e5e3-123">Effect properties</span></span>



| <span data-ttu-id="8e5e3-124">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="8e5e3-124">Display name and index enumeration</span></span>                         | <span data-ttu-id="8e5e3-125">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8e5e3-125">Type and default value</span></span>           | <span data-ttu-id="8e5e3-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e5e3-126">Description</span></span>                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| <span data-ttu-id="8e5e3-127">Ángulo</span><span class="sxs-lookup"><span data-stu-id="8e5e3-127">Angle</span></span><br/> <span data-ttu-id="8e5e3-128">Ángulo de la D2D1 \_ HUEROTATION \_ \_</span><span class="sxs-lookup"><span data-stu-id="8e5e3-128">D2D1\_HUEROTATION\_PROP\_ANGLE</span></span><br/> | <span data-ttu-id="8e5e3-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8e5e3-129">FLOAT</span></span><br/> <span data-ttu-id="8e5e3-130">0,0F</span><span class="sxs-lookup"><span data-stu-id="8e5e3-130">0.0f</span></span><br/> | <span data-ttu-id="8e5e3-131">Ángulo para girar el matiz, en grados.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-131">The angle to rotate the hue, in degrees.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="8e5e3-132">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8e5e3-132">Output bitmap</span></span>

<span data-ttu-id="8e5e3-133">El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="8e5e3-133">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e5e3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e5e3-134">Requirements</span></span>



| <span data-ttu-id="8e5e3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e5e3-135">Requirement</span></span> | <span data-ttu-id="8e5e3-136">Value</span><span class="sxs-lookup"><span data-stu-id="8e5e3-136">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5e3-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e5e3-137">Minimum supported client</span></span> | <span data-ttu-id="8e5e3-138">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8e5e3-138">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8e5e3-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e5e3-139">Minimum supported server</span></span> | <span data-ttu-id="8e5e3-140">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8e5e3-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8e5e3-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e5e3-141">Header</span></span>                   | <span data-ttu-id="8e5e3-142">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8e5e3-142">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8e5e3-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e5e3-143">Library</span></span>                  | <span data-ttu-id="8e5e3-144">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8e5e3-144">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8e5e3-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e5e3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e5e3-146">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8e5e3-146">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

