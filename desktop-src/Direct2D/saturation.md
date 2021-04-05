---
title: Efecto de saturación
description: Utilice este efecto para modificar la saturación de una imagen.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- efecto de saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079246"
---
# <a name="saturation-effect"></a><span data-ttu-id="092ce-104">Efecto de saturación</span><span class="sxs-lookup"><span data-stu-id="092ce-104">Saturation effect</span></span>

<span data-ttu-id="092ce-105">Utilice este efecto para modificar la saturación de una imagen.</span><span class="sxs-lookup"><span data-stu-id="092ce-105">Use this effect to alter the saturation of an image.</span></span> <span data-ttu-id="092ce-106">El efecto de saturación es una especialización del efecto de la [matriz de colores](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="092ce-106">The saturation effect is a specialization of the [color matrix](color-matrix.md) effect.</span></span>

<span data-ttu-id="092ce-107">El CLSID para este efecto es CLSID \_ D2D1Saturation.</span><span class="sxs-lookup"><span data-stu-id="092ce-107">The CLSID for this effect is CLSID\_D2D1Saturation.</span></span>

-   [<span data-ttu-id="092ce-108">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="092ce-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="092ce-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="092ce-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="092ce-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="092ce-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="092ce-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="092ce-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="092ce-112">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="092ce-112">Example image</span></span>

<span data-ttu-id="092ce-113">En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de saturación con una saturación del 0%.</span><span class="sxs-lookup"><span data-stu-id="092ce-113">The example here shows the input and output images of the saturation effect with a saturation of 0%.</span></span>



| <span data-ttu-id="092ce-114">Antes</span><span class="sxs-lookup"><span data-stu-id="092ce-114">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)  |
| <span data-ttu-id="092ce-116">Después</span><span class="sxs-lookup"><span data-stu-id="092ce-116">After</span></span>                                                       |
| ![la imagen después de la transformación.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="092ce-118">El efecto calcula una matriz de colores basándose en el valor de saturación que se muestra *aquí (en* la ecuación) que se especifica con la propiedad de saturación D2D1 saturación de saturación \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="092ce-118">The effect calculates a color matrix based on the saturation value (*s* in the equation here) you specify with the D2D1\_SATURATION\_PROP\_SATURATION property.</span></span> <span data-ttu-id="092ce-119">La ecuación de la matriz se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="092ce-119">The matrix equation is shown here.</span></span>

![fórmula para calcular una matriz de saturación.](images/saturation-formula.png)

<span data-ttu-id="092ce-121">La matriz creada depende solo del valor de saturación.</span><span class="sxs-lookup"><span data-stu-id="092ce-121">The matrix created depends only on the saturation value.</span></span> <span data-ttu-id="092ce-122">Puede usar el efecto de la [matriz de colores](color-matrix.md) si necesita una matriz específica.</span><span class="sxs-lookup"><span data-stu-id="092ce-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

<span data-ttu-id="092ce-123">Este efecto consume y genera imágenes alfa premultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="092ce-123">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="092ce-124">El efecto no funcionará en imágenes alfa rectas a menos que sean totalmente opacas.</span><span class="sxs-lookup"><span data-stu-id="092ce-124">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="092ce-125">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="092ce-125">Effect properties</span></span>



| <span data-ttu-id="092ce-126">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="092ce-126">Display name and index enumeration</span></span>                                  | <span data-ttu-id="092ce-127">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="092ce-127">Type and default value</span></span>           | <span data-ttu-id="092ce-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="092ce-128">Description</span></span>                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="092ce-129">Saturación</span><span class="sxs-lookup"><span data-stu-id="092ce-129">Saturation</span></span><br/> <span data-ttu-id="092ce-130">Saturación de D2D1 \_ saturación de saturación \_ \_</span><span class="sxs-lookup"><span data-stu-id="092ce-130">D2D1\_SATURATION\_PROP\_SATURATION</span></span><br/> | <span data-ttu-id="092ce-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="092ce-131">FLOAT</span></span><br/> <span data-ttu-id="092ce-132">0.5 f</span><span class="sxs-lookup"><span data-stu-id="092ce-132">0.5f</span></span><br/> | <span data-ttu-id="092ce-133">Saturación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="092ce-133">The saturation of the image.</span></span> <span data-ttu-id="092ce-134">Puede establecer la saturación en un valor entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="092ce-134">You can set the saturation to a value between 0 and 1.</span></span> <span data-ttu-id="092ce-135">Si se establece en 1, la imagen de salida está completamente saturada.</span><span class="sxs-lookup"><span data-stu-id="092ce-135">If you set it to 1 the output image is fully saturated.</span></span> <span data-ttu-id="092ce-136">Si se establece en 0, la imagen de salida es monocroma.</span><span class="sxs-lookup"><span data-stu-id="092ce-136">If you set it to 0 the output image is monochrome.</span></span> <span data-ttu-id="092ce-137">El valor de saturación no es una unidad.</span><span class="sxs-lookup"><span data-stu-id="092ce-137">The saturation value is unitless.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="092ce-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="092ce-138">Requirements</span></span>



| <span data-ttu-id="092ce-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="092ce-139">Requirement</span></span> | <span data-ttu-id="092ce-140">Value</span><span class="sxs-lookup"><span data-stu-id="092ce-140">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="092ce-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="092ce-141">Minimum supported client</span></span> | <span data-ttu-id="092ce-142">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="092ce-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="092ce-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="092ce-143">Minimum supported server</span></span> | <span data-ttu-id="092ce-144">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="092ce-144">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="092ce-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="092ce-145">Header</span></span>                   | <span data-ttu-id="092ce-146">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="092ce-146">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="092ce-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="092ce-147">Library</span></span>                  | <span data-ttu-id="092ce-148">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="092ce-148">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="092ce-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="092ce-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="092ce-150">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="092ce-150">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

