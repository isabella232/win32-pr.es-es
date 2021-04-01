---
title: Efecto de recorte
description: Use el efecto de recorte para generar una región específica de una imagen.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- efecto de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905224"
---
# <a name="crop-effect"></a><span data-ttu-id="8dcbb-104">Efecto de recorte</span><span class="sxs-lookup"><span data-stu-id="8dcbb-104">Crop effect</span></span>

<span data-ttu-id="8dcbb-105">Use el efecto de recorte para generar una región específica de una imagen.</span><span class="sxs-lookup"><span data-stu-id="8dcbb-105">Use the crop effect to output a specified region of an image.</span></span>

<span data-ttu-id="8dcbb-106">El CLSID para este efecto es CLSID \_ D2D1Crop.</span><span class="sxs-lookup"><span data-stu-id="8dcbb-106">The CLSID for this effect is CLSID\_D2D1Crop.</span></span>

-   [<span data-ttu-id="8dcbb-107">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8dcbb-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="8dcbb-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8dcbb-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="8dcbb-109">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8dcbb-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="8dcbb-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dcbb-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8dcbb-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8dcbb-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="8dcbb-112">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8dcbb-112">Example image</span></span>



| <span data-ttu-id="8dcbb-113">Antes</span><span class="sxs-lookup"><span data-stu-id="8dcbb-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
| <span data-ttu-id="8dcbb-115">Después</span><span class="sxs-lookup"><span data-stu-id="8dcbb-115">After</span></span>                                                      |
| ![la imagen después de la transformación.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="8dcbb-117">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8dcbb-117">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8dcbb-118">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="8dcbb-118">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="8dcbb-119">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8dcbb-119">Type and default value</span></span></th>
<th><span data-ttu-id="8dcbb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dcbb-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8dcbb-121">Rect</span><span class="sxs-lookup"><span data-stu-id="8dcbb-121">Rect</span></span><br/></td>
<td><span data-ttu-id="8dcbb-122">D2D1_VECTOR_4F</span><span class="sxs-lookup"><span data-stu-id="8dcbb-122">D2D1_VECTOR_4F</span></span><br/></td>
<td><span data-ttu-id="8dcbb-123">Región que se va a recortar como vector en el formato (izquierda, superior, ancho y alto).</span><span class="sxs-lookup"><span data-stu-id="8dcbb-123">The region to be cropped specified as a vector in the form (left, top, width, height).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8dcbb-124">D2D1_CROP_PROP_RECT</span><span class="sxs-lookup"><span data-stu-id="8dcbb-124">D2D1_CROP_PROP_RECT</span></span><br/></td>
<td><span data-ttu-id="8dcbb-125">{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}</span><span class="sxs-lookup"><span data-stu-id="8dcbb-125">{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}</span></span><br/></td>
<td><span data-ttu-id="8dcbb-126">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="8dcbb-126">The units are in DIPs.</span></span> <br/>
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="8dcbb-127">El rectángulo se truncará si se superpone a los límites de borde de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="8dcbb-127">The Rect will be truncated if it overlaps the edge boundaries of the input image.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8dcbb-128">D2D1_CROP_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="8dcbb-128">D2D1_CROP_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="8dcbb-129">D2D1_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="8dcbb-129">D2D1_BORDER_MODE</span></span> <br/> <span data-ttu-id="8dcbb-130">D2D1_BORDER_MODE_SOFT</span><span class="sxs-lookup"><span data-stu-id="8dcbb-130">D2D1_BORDER_MODE_SOFT</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="8dcbb-131">D2D1_BORDER_MODE_SOFT: Si el rectángulo de recorte cae en coordenadas de píxeles fraccionarios, el efecto aplica el suavizado de contorno, lo que da como resultado un borde flexible.</span><span class="sxs-lookup"><span data-stu-id="8dcbb-131">D2D1_BORDER_MODE_SOFT : If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.</span></span></li>
<li><span data-ttu-id="8dcbb-132">D2D1_BORDER_MODE_HARD: Si el rectángulo de recorte cae en coordenadas de píxeles fraccionarios, el efecto se fija, lo que da como resultado un borde duro.</span><span class="sxs-lookup"><span data-stu-id="8dcbb-132">D2D1_BORDER_MODE_HARD : If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a><span data-ttu-id="8dcbb-133">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8dcbb-133">Output bitmap</span></span>

<span data-ttu-id="8dcbb-134">La salida de este efecto es el tamaño de la propiedad Rect.</span><span class="sxs-lookup"><span data-stu-id="8dcbb-134">The output of this effect is the size of the Rect property.</span></span> <span data-ttu-id="8dcbb-135">La longitud y el ancho son Calc</span><span class="sxs-lookup"><span data-stu-id="8dcbb-135">The length and width are calc</span></span>

<span data-ttu-id="8dcbb-136">ulated usar las ecuaciones aquí:</span><span class="sxs-lookup"><span data-stu-id="8dcbb-136">ulated using the equations here:</span></span> <dl> <span data-ttu-id="8dcbb-137">Longitud de salida en píxeles = (rect. Right-Rect. Left) \* (PPP del usuario/96)</span><span class="sxs-lookup"><span data-stu-id="8dcbb-137">Output length in Pixels=(Rect.Right-Rect.Left)\*(User's DPI/96)</span></span>  
<span data-ttu-id="8dcbb-138">Alto de salida en píxeles = (rect. Bottom-Rect.Top) \* (PPP del usuario/96)</span><span class="sxs-lookup"><span data-stu-id="8dcbb-138">Output height in pixels=(Rect.Bottom-Rect.Top)\*(User's DPI/96)</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="8dcbb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dcbb-139">Requirements</span></span>



| <span data-ttu-id="8dcbb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dcbb-140">Requirement</span></span> | <span data-ttu-id="8dcbb-141">Value</span><span class="sxs-lookup"><span data-stu-id="8dcbb-141">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8dcbb-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8dcbb-142">Minimum supported client</span></span> | <span data-ttu-id="8dcbb-143">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8dcbb-143">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8dcbb-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8dcbb-144">Minimum supported server</span></span> | <span data-ttu-id="8dcbb-145">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8dcbb-145">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8dcbb-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8dcbb-146">Header</span></span>                   | <span data-ttu-id="8dcbb-147">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8dcbb-147">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8dcbb-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8dcbb-148">Library</span></span>                  | <span data-ttu-id="8dcbb-149">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8dcbb-149">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8dcbb-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8dcbb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dcbb-151">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8dcbb-151">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

