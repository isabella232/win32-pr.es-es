---
title: Efecto de mapa de desplazamiento
description: Use el efecto de mapa de desplazamiento para desplazar los píxeles de la imagen de entrada por los valores de intensidad de una segunda imagen de entrada.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- efecto de mapa de desplazamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149929"
---
# <a name="displacement-map-effect"></a><span data-ttu-id="f672f-104">Efecto de mapa de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="f672f-104">Displacement map effect</span></span>

<span data-ttu-id="f672f-105">Use el efecto de mapa de desplazamiento para desplazar los píxeles de la imagen de entrada por los valores de intensidad de una segunda imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="f672f-105">Use the displacement map effect to displace the pixels of the input image by the intensity values of a second input image.</span></span>

<span data-ttu-id="f672f-106">El CLSID para este efecto es CLSID \_ D2D1DisplacementMap.</span><span class="sxs-lookup"><span data-stu-id="f672f-106">The CLSID for this effect is CLSID\_D2D1DisplacementMap.</span></span>

-   [<span data-ttu-id="f672f-107">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f672f-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="f672f-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="f672f-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="f672f-109">Canales de color</span><span class="sxs-lookup"><span data-stu-id="f672f-109">Color channels</span></span>](#color-channels)
-   [<span data-ttu-id="f672f-110">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="f672f-110">Output Bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="f672f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f672f-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f672f-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f672f-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="f672f-113">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f672f-113">Example image</span></span>



| <span data-ttu-id="f672f-114">Antes</span><span class="sxs-lookup"><span data-stu-id="f672f-114">Before</span></span>                                                           |
|------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)       |
| <span data-ttu-id="f672f-116">Después</span><span class="sxs-lookup"><span data-stu-id="f672f-116">After</span></span>                                                            |
| ![la imagen después de la transformación.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="f672f-118">Las ubicaciones de los píxeles de la salida se determinan mediante esta fórmula:</span><span class="sxs-lookup"><span data-stu-id="f672f-118">The locations of the pixels in the output are determined using this formula:</span></span>

<span data-ttu-id="f672f-119">C ' (x, y) = C (x + Scale \* (XChannelSelector (mapa de bits de desplazamiento (x, y))-0.5), y + Scale \* (YChannelSelector (mapa de bits de desplazamiento (x, y))-0,5))</span><span class="sxs-lookup"><span data-stu-id="f672f-119">C' (x,y)=C(x+ scale\*(XChannelSelector(Displacement Bitmap (x,y))-0.5),y+ scale\*(YChannelSelector(Displacement Bitmap (x,y))-0.5))</span></span>

<span data-ttu-id="f672f-120">Donde:</span><span class="sxs-lookup"><span data-stu-id="f672f-120">Where:</span></span><dl> <span data-ttu-id="f672f-121">*C (x, y)* es el píxel de salida en (x, y).</span><span class="sxs-lookup"><span data-stu-id="f672f-121">*C  (x, y)* is the output pixel at (x, y).</span></span>  
<span data-ttu-id="f672f-122">*C (x, y)* es el píxel de entrada en (x, y).</span><span class="sxs-lookup"><span data-stu-id="f672f-122">*C (x, y)* is the input pixel at (x, y).</span></span>  
<span data-ttu-id="f672f-123">El *mapa de bits de desplazamiento (x, y)* es la intensidad de píxeles de desplazamiento en las coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="f672f-123">*Displacement Bitmap (x, y)* is the displacement pixel intensity at the specified coordinates</span></span>  
<span data-ttu-id="f672f-124">*XChannelSelector* la intensidad del canal RGBA seleccionado del mapa de bits de desplazamiento que coloca la imagen de entrada en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="f672f-124">*XChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the X direction.</span></span>  
<span data-ttu-id="f672f-125">*YChannelSelector* la intensidad del canal RGBA seleccionado del mapa de bits de desplazamiento que desplace la imagen de entrada en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="f672f-125">*YChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the Y direction.</span></span>  
</dl>

<span data-ttu-id="f672f-126">El efecto remuestrea la imagen de entrada según la propiedad de escala y la intensidad de la imagen de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="f672f-126">The effect resamples the input image according to the scale property and the intensity of the displacement image.</span></span> <span data-ttu-id="f672f-127">Usa la interpolación bilineal si se muestrea desde los píxeles de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="f672f-127">It uses bilinear interpolation if sampling from between pixels in the input image.</span></span>

<span data-ttu-id="f672f-128">Este efecto funciona en imágenes alfa directas y premultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="f672f-128">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="f672f-129">El formato alfa de salida es el mismo que el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="f672f-129">The output alpha format is the same as the input format.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="f672f-130">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="f672f-130">Effect properties</span></span>



| <span data-ttu-id="f672f-131">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="f672f-131">Display name and index enumeration</span></span>                                                   | <span data-ttu-id="f672f-132">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f672f-132">Type and default value</span></span>                                                   | <span data-ttu-id="f672f-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="f672f-133">Description</span></span>                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f672f-134">Escala</span><span class="sxs-lookup"><span data-stu-id="f672f-134">Scale</span></span><br/> <span data-ttu-id="f672f-135">D2D1 \_ DISPLACEMENTMAP \_ prop \_ Scale</span><span class="sxs-lookup"><span data-stu-id="f672f-135">D2D1\_DISPLACEMENTMAP\_PROP\_SCALE</span></span><br/>                       | <span data-ttu-id="f672f-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f672f-136">FLOAT</span></span><br/> <span data-ttu-id="f672f-137">0,0F</span><span class="sxs-lookup"><span data-stu-id="f672f-137">0.0f</span></span><br/>                                         | <span data-ttu-id="f672f-138">Multiplica la intensidad del canal seleccionado de la imagen de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="f672f-138">Multiplies the intensity of the selected channel from the displacement image.</span></span> <span data-ttu-id="f672f-139">Cuanto más alto establezca esta propiedad, más el efecto desplazará los píxeles</span><span class="sxs-lookup"><span data-stu-id="f672f-139">The higher you set this property, the more the effect displaces the pixels</span></span><br/>                       |
| <span data-ttu-id="f672f-140">XChannelSelect</span><span class="sxs-lookup"><span data-stu-id="f672f-140">XChannelSelect</span></span><br/> <span data-ttu-id="f672f-141">D2D1 \_ DISPLACEMENTMAP \_ prop \_ X \_ canal \_ Select</span><span class="sxs-lookup"><span data-stu-id="f672f-141">D2D1\_DISPLACEMENTMAP\_PROP\_X\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="f672f-142">\_Selector de canal de D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="f672f-142">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="f672f-143">\_ \_ Selector de canal \_ de D2D1 A</span><span class="sxs-lookup"><span data-stu-id="f672f-143">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="f672f-144">El efecto extrae la intensidad de este canal de color y la usa para desplazar espacialmente la imagen en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="f672f-144">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.</span></span> <span data-ttu-id="f672f-145">Vea [canales de color](#color-channels) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f672f-145">See [Color channels](#color-channels) for more info.</span></span><br/> |
| <span data-ttu-id="f672f-146">YChannelSelect</span><span class="sxs-lookup"><span data-stu-id="f672f-146">YChannelSelect</span></span><br/> <span data-ttu-id="f672f-147">D2D1 \_ DISPLACEMENTMAP \_ prop \_ Y \_ canal \_ Select</span><span class="sxs-lookup"><span data-stu-id="f672f-147">D2D1\_DISPLACEMENTMAP\_PROP\_Y\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="f672f-148">\_Selector de canal de D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="f672f-148">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="f672f-149">\_ \_ Selector de canal \_ de D2D1 A</span><span class="sxs-lookup"><span data-stu-id="f672f-149">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="f672f-150">El efecto extrae la intensidad de este canal de color y la usa para desplazar espacialmente la imagen en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="f672f-150">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.</span></span> <span data-ttu-id="f672f-151">Vea [canales de color](#color-channels) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f672f-151">See [Color channels](#color-channels) for more info.</span></span><br/> |



 

## <a name="color-channels"></a><span data-ttu-id="f672f-152">Canales de color</span><span class="sxs-lookup"><span data-stu-id="f672f-152">Color channels</span></span>



| <span data-ttu-id="f672f-153">Enumeración</span><span class="sxs-lookup"><span data-stu-id="f672f-153">Enumeration</span></span>                | <span data-ttu-id="f672f-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="f672f-154">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f672f-155">Selector de canal de D2D1 \_ \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="f672f-155">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="f672f-156">El efecto extrae la salida de intensidad del canal rojo.</span><span class="sxs-lookup"><span data-stu-id="f672f-156">The effect extracts the intensity output from the red channel.</span></span>   |
| <span data-ttu-id="f672f-157">Selector de canal de D2D1 \_ \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="f672f-157">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="f672f-158">El efecto extrae la salida de intensidad del canal verde.</span><span class="sxs-lookup"><span data-stu-id="f672f-158">The effect extracts the intensity output from the green channel.</span></span> |
| <span data-ttu-id="f672f-159">Selector de canal de D2D1 \_ \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="f672f-159">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="f672f-160">El efecto extrae la salida de intensidad del canal azul.</span><span class="sxs-lookup"><span data-stu-id="f672f-160">The effect extracts the intensity output from the blue channel.</span></span>  |
| <span data-ttu-id="f672f-161">\_ \_ Selector de canal \_ de D2D1 A</span><span class="sxs-lookup"><span data-stu-id="f672f-161">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="f672f-162">El efecto extrae la salida de intensidad del canal alfa.</span><span class="sxs-lookup"><span data-stu-id="f672f-162">The effect extracts the intensity output from the alpha channel.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="f672f-163">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="f672f-163">Output Bitmap</span></span>

<span data-ttu-id="f672f-164">Puede determinar el tamaño máximo del mapa de bits de salida con estas ecuaciones:</span><span class="sxs-lookup"><span data-stu-id="f672f-164">You can determine the maximum size of the output bitmap with these equations:</span></span>

<span data-ttu-id="f672f-165">¿Mapa de bits de salida?</span><span class="sxs-lookup"><span data-stu-id="f672f-165">Output Bitmap?</span></span> <span data-ttu-id="f672f-166">Píxeles = (tamaño del mapa de bits de entrada? ( DIP) + escala \* (PPP de usuario/96)</span><span class="sxs-lookup"><span data-stu-id="f672f-166">Pixels=(Input Bitmap Size?(DIPs)+Scale)\*(User DPI/96)</span></span>

<span data-ttu-id="f672f-167">Mapa de bits<sub>y</sub> píxeles de salida = (tamaño del mapa de bits de entrada<sub>y</sub>(DIP) + escala) \* (PPP del usuario/96)</span><span class="sxs-lookup"><span data-stu-id="f672f-167">Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale)\*(User DPI/96)</span></span>

## <a name="requirements"></a><span data-ttu-id="f672f-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f672f-168">Requirements</span></span>



| <span data-ttu-id="f672f-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="f672f-169">Requirement</span></span> | <span data-ttu-id="f672f-170">Value</span><span class="sxs-lookup"><span data-stu-id="f672f-170">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f672f-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f672f-171">Minimum supported client</span></span> | <span data-ttu-id="f672f-172">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="f672f-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f672f-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f672f-173">Minimum supported server</span></span> | <span data-ttu-id="f672f-174">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="f672f-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f672f-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f672f-175">Header</span></span>                   | <span data-ttu-id="f672f-176">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="f672f-176">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="f672f-177">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f672f-177">Library</span></span>                  | <span data-ttu-id="f672f-178">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="f672f-178">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="f672f-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f672f-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f672f-180">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="f672f-180">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

