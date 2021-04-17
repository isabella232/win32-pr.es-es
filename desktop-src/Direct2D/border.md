---
title: Efecto de borde
description: Use el efecto de borde para extender una imagen de los bordes.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- efecto de borde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104547243"
---
# <a name="border-effect"></a><span data-ttu-id="2332f-104">Efecto de borde</span><span class="sxs-lookup"><span data-stu-id="2332f-104">Border effect</span></span>

<span data-ttu-id="2332f-105">Use el efecto de borde para extender una imagen de los bordes.</span><span class="sxs-lookup"><span data-stu-id="2332f-105">Use the border effect to extend an image from the edges.</span></span> <span data-ttu-id="2332f-106">Puede usar este efecto para repetir los píxeles desde los bordes de la imagen, ajustar los píxeles desde el extremo opuesto de la imagen o reflejar los píxeles en el borde del mapa de bits para extender la región del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2332f-106">You can use this effect to repeat the pixels from the edges of the image, wrap the pixels from the opposite end of the image, or mirror the pixels across the bitmap border to extend the bitmap region.</span></span>

<span data-ttu-id="2332f-107">El CLSID para este efecto es CLSID \_ D2D1Border.</span><span class="sxs-lookup"><span data-stu-id="2332f-107">The CLSID for this effect is CLSID\_D2D1Border.</span></span>

## <a name="example-images"></a><span data-ttu-id="2332f-108">Imágenes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2332f-108">Example images</span></span>

<span data-ttu-id="2332f-109">En los ejemplos siguientes se muestra el resultado del efecto de borde con cada modo.</span><span class="sxs-lookup"><span data-stu-id="2332f-109">The examples here show the output of the border effect using each mode.</span></span> <span data-ttu-id="2332f-110">El tamaño de salida es infinito, pero estas imágenes de ejemplo se recortan dos veces el tamaño.</span><span class="sxs-lookup"><span data-stu-id="2332f-110">The output size is infinite, but these example images are cropped to twice the size.</span></span>

### <a name="mirror"></a><span data-ttu-id="2332f-111">Reflejo</span><span class="sxs-lookup"><span data-stu-id="2332f-111">Mirror</span></span>



| <span data-ttu-id="2332f-112">Antes</span><span class="sxs-lookup"><span data-stu-id="2332f-112">Before</span></span>                                                    |
|-----------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto.](images/border-before.jpg) |
| <span data-ttu-id="2332f-114">Después</span><span class="sxs-lookup"><span data-stu-id="2332f-114">After</span></span>                                                     |
| ![Captura de pantalla que muestra la imagen después de la transformación.](images/10-border.png)   |



 

### <a name="clamp"></a><span data-ttu-id="2332f-116">Clamp</span><span class="sxs-lookup"><span data-stu-id="2332f-116">Clamp</span></span>



| <span data-ttu-id="2332f-117">Antes</span><span class="sxs-lookup"><span data-stu-id="2332f-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto de una abrazadera.](images/border-before.jpg)     |
| <span data-ttu-id="2332f-119">Después</span><span class="sxs-lookup"><span data-stu-id="2332f-119">After</span></span>                                                         |
| ![Captura de pantalla que muestra la imagen después de la transformación de una abrazadera.](images/10-border-clamp.png) |



 

### <a name="wrap"></a><span data-ttu-id="2332f-121">Encapsulado</span><span class="sxs-lookup"><span data-stu-id="2332f-121">Wrap</span></span>



| <span data-ttu-id="2332f-122">Antes</span><span class="sxs-lookup"><span data-stu-id="2332f-122">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto para un ajuste.](images/border-before.jpg)    |
| <span data-ttu-id="2332f-124">Después</span><span class="sxs-lookup"><span data-stu-id="2332f-124">After</span></span>                                                        |
| ![Captura de pantalla que muestra la imagen después de la transformación de un ajuste.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="2332f-126">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="2332f-126">Effect properties</span></span>



| <span data-ttu-id="2332f-127">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="2332f-127">Display name and index enumeration</span></span>                                  | <span data-ttu-id="2332f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2332f-128">Description</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2332f-129">Modo de borde X</span><span class="sxs-lookup"><span data-stu-id="2332f-129">Edge Mode X</span></span><br/> <span data-ttu-id="2332f-130">D2D1 \_ Border \_ props \_ modo de borde \_ \_ X</span><span class="sxs-lookup"><span data-stu-id="2332f-130">D2D1\_BORDER\_PROP\_EDGE\_MODE\_X</span></span><br/> | <span data-ttu-id="2332f-131">Modo de borde en la dirección X del efecto.</span><span class="sxs-lookup"><span data-stu-id="2332f-131">The edge mode in the X direction for the effect.</span></span> <span data-ttu-id="2332f-132">Puede establecerlo en Clamp, Wrap o Mirror.</span><span class="sxs-lookup"><span data-stu-id="2332f-132">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="2332f-133">Vea [modos perimetrales](#edge-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2332f-133">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="2332f-134">El tipo es el modo de borde de borde de D2D1 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2332f-134">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="2332f-135">El valor predeterminado es la abrazadera del modo de borde de \_ borde D2D1 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2332f-135">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |
| <span data-ttu-id="2332f-136">Modo de borde Y</span><span class="sxs-lookup"><span data-stu-id="2332f-136">Edge Mode Y</span></span><br/> <span data-ttu-id="2332f-137">Modo de borde de propiedades de borde de D2D1 \_ \_ \_ \_ \_ Y</span><span class="sxs-lookup"><span data-stu-id="2332f-137">D2D1\_BORDER\_PROP\_EDGE\_MODE\_Y</span></span><br/> | <span data-ttu-id="2332f-138">Modo de borde en la dirección Y del efecto.</span><span class="sxs-lookup"><span data-stu-id="2332f-138">The edge mode in the Y direction for the effect.</span></span> <span data-ttu-id="2332f-139">Puede establecerlo en Clamp, Wrap o Mirror.</span><span class="sxs-lookup"><span data-stu-id="2332f-139">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="2332f-140">Vea [modos perimetrales](#edge-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2332f-140">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="2332f-141">El tipo es el modo de borde de borde de D2D1 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2332f-141">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="2332f-142">El valor predeterminado es la abrazadera del modo de borde de \_ borde D2D1 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2332f-142">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |



 

## <a name="edge-modes"></a><span data-ttu-id="2332f-143">Modos perimetrales</span><span class="sxs-lookup"><span data-stu-id="2332f-143">Edge modes</span></span>



| <span data-ttu-id="2332f-144">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="2332f-144">Display name and index enumeration</span></span>                            | <span data-ttu-id="2332f-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="2332f-145">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2332f-146">Clamp</span><span class="sxs-lookup"><span data-stu-id="2332f-146">Clamp</span></span><br/> <span data-ttu-id="2332f-147">\_Abrazadera del \_ \_ modo \_ de borde de borde de D2D1</span><span class="sxs-lookup"><span data-stu-id="2332f-147">D2D1\_BORDER\_EDGE\_MODE\_CLAMP</span></span><br/>   | <span data-ttu-id="2332f-148">Repite los píxeles de los bordes de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2332f-148">Repeats the pixels from the edges of the image.</span></span>      |
| <span data-ttu-id="2332f-149">Encapsulado</span><span class="sxs-lookup"><span data-stu-id="2332f-149">Wrap</span></span><br/> <span data-ttu-id="2332f-150">\_Ajuste del \_ \_ modo \_ de borde de borde de D2D1</span><span class="sxs-lookup"><span data-stu-id="2332f-150">D2D1\_BORDER\_EDGE\_MODE\_WRAP</span></span><br/>     | <span data-ttu-id="2332f-151">Usa píxeles desde el borde final opuesto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2332f-151">Uses pixels from the opposite end edge of the image.</span></span> |
| <span data-ttu-id="2332f-152">Reflejo</span><span class="sxs-lookup"><span data-stu-id="2332f-152">Mirror</span></span><br/> <span data-ttu-id="2332f-153">\_Reflejo del \_ \_ modo \_ de borde de D2D1 Border</span><span class="sxs-lookup"><span data-stu-id="2332f-153">D2D1\_BORDER\_EDGE\_MODE\_MIRROR</span></span><br/> | <span data-ttu-id="2332f-154">Refleja los píxeles sobre el borde de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2332f-154">Reflects pixels about the edge of the image.</span></span>         |



 

## <a name="output-bitmap"></a><span data-ttu-id="2332f-155">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="2332f-155">Output bitmap</span></span>

<span data-ttu-id="2332f-156">El tamaño del mapa de bits de salida es infinito para todas las entradas, excepto una imagen de entrada de tamaño 0.</span><span class="sxs-lookup"><span data-stu-id="2332f-156">The output bitmap size is infinite for all inputs, except a 0 sized input image.</span></span> <span data-ttu-id="2332f-157">Si el alto o el ancho de una imagen de entrada es 0, el tamaño de salida es 0.</span><span class="sxs-lookup"><span data-stu-id="2332f-157">If the height or the width of an input image is 0, the output size is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="2332f-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2332f-158">Requirements</span></span>



| <span data-ttu-id="2332f-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="2332f-159">Requirement</span></span> | <span data-ttu-id="2332f-160">Value</span><span class="sxs-lookup"><span data-stu-id="2332f-160">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2332f-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2332f-161">Minimum supported client</span></span> | <span data-ttu-id="2332f-162">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="2332f-162">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2332f-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2332f-163">Minimum supported server</span></span> | <span data-ttu-id="2332f-164">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="2332f-164">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2332f-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2332f-165">Header</span></span>                   | <span data-ttu-id="2332f-166">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="2332f-166">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="2332f-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2332f-167">Library</span></span>                  | <span data-ttu-id="2332f-168">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2332f-168">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2332f-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2332f-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2332f-170">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="2332f-170">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

