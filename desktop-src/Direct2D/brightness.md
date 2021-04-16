---
title: Efecto de brillo
description: Use el efecto brillo para controlar el brillo de la imagen.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- efecto de brillo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104551727"
---
# <a name="brightness-effect"></a><span data-ttu-id="8012a-104">Efecto de brillo</span><span class="sxs-lookup"><span data-stu-id="8012a-104">Brightness effect</span></span>

<span data-ttu-id="8012a-105">Use el efecto brillo para controlar el brillo de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8012a-105">Use the brightness effect to control the brightness of the image.</span></span>

<span data-ttu-id="8012a-106">El CLSID para este efecto es CLSID \_ D2D1Brightness.</span><span class="sxs-lookup"><span data-stu-id="8012a-106">The CLSID for this effect is CLSID\_D2D1Brightness.</span></span>

-   [<span data-ttu-id="8012a-107">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8012a-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="8012a-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8012a-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="8012a-109">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8012a-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="8012a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8012a-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8012a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8012a-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="8012a-112">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8012a-112">Example image</span></span>



| <span data-ttu-id="8012a-113">Antes</span><span class="sxs-lookup"><span data-stu-id="8012a-113">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)  |
| <span data-ttu-id="8012a-115">Después</span><span class="sxs-lookup"><span data-stu-id="8012a-115">After</span></span>                                                       |
| ![la imagen después de la transformación.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="8012a-117">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8012a-117">Effect properties</span></span>



| <span data-ttu-id="8012a-118">Nombre para mostrar de la propiedad</span><span class="sxs-lookup"><span data-stu-id="8012a-118">Property Display Name</span></span>                                                 | <span data-ttu-id="8012a-119">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8012a-119">Type and default value</span></span>                              | <span data-ttu-id="8012a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8012a-120">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8012a-121">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="8012a-121">WhitePoint</span></span><br/> <span data-ttu-id="8012a-122">\_ \_ \_ Punto blanco de la luminosidad de D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="8012a-122">D2D1\_BRIGHTNESS\_PROP\_WHITE\_POINT</span></span><br/> | <span data-ttu-id="8012a-123">\_Vector D2D1 \_ 2F</span><span class="sxs-lookup"><span data-stu-id="8012a-123">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="8012a-124">{1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="8012a-124">{1.0f, 1.0f}</span></span><br/> | <span data-ttu-id="8012a-125">Parte superior de la curva de transferencia de brillo.</span><span class="sxs-lookup"><span data-stu-id="8012a-125">The upper portion of the brightness transfer curve.</span></span> <span data-ttu-id="8012a-126">El punto blanco ajusta la apariencia de las partes más brillantes de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8012a-126">The white point adjusts the appearance of the brighter portions of the image.</span></span> <span data-ttu-id="8012a-127">Esta propiedad es para el valor x y el valor y, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="8012a-127">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="8012a-128">Cada uno de los valores de esta propiedad está entre 0 y 1, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="8012a-128">Each of the values of this property are between 0 and 1, inclusive.</span></span> |
| <span data-ttu-id="8012a-129">BlackPoint</span><span class="sxs-lookup"><span data-stu-id="8012a-129">BlackPoint</span></span><br/> <span data-ttu-id="8012a-130">\_ \_ \_ Punto negro de la luminosidad de D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="8012a-130">D2D1\_BRIGHTNESS\_PROP\_BLACK\_POINT</span></span><br/> | <span data-ttu-id="8012a-131">\_Vector D2D1 \_ 2F</span><span class="sxs-lookup"><span data-stu-id="8012a-131">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="8012a-132">{0.0 f, 0.0 f}</span><span class="sxs-lookup"><span data-stu-id="8012a-132">{0.0f, 0.0f}</span></span><br/> | <span data-ttu-id="8012a-133">Parte inferior de la curva de transferencia de brillo.</span><span class="sxs-lookup"><span data-stu-id="8012a-133">The lower portion of the brightness transfer curve.</span></span> <span data-ttu-id="8012a-134">El punto negro ajusta la apariencia de las partes más oscuras de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8012a-134">The black point adjusts the appearance of the darker portions of the image.</span></span> <span data-ttu-id="8012a-135">Esta propiedad es para el valor x y el valor y, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="8012a-135">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="8012a-136">Cada uno de los valores de esta propiedad está entre 0 y 1, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="8012a-136">Each of the values of this property are between 0 and 1, inclusive.</span></span>   |



 

<span data-ttu-id="8012a-137">Este efecto usa los puntos blanco y negro especificados para generar una función de transferencia que se usa para ajustar el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8012a-137">This effect uses the specified white and black points to generate a transfer function used to adjust the bitmap.</span></span> <span data-ttu-id="8012a-138">La siguiente ecuación describe la función de transferencia.</span><span class="sxs-lookup"><span data-stu-id="8012a-138">The next equation describes the transfer function.</span></span> <span data-ttu-id="8012a-139">Las intensidades de entrada se definen entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="8012a-139">The input intensities are defined between 0 and 1.</span></span>

![algoritmo de brillo](images/brightness-formula1.png)

<span data-ttu-id="8012a-141">El algoritmo de efecto implementa una ecuación que crea la función de transferencia.</span><span class="sxs-lookup"><span data-stu-id="8012a-141">The effect algorithm implements an equation that creates the transfer function.</span></span> <span data-ttu-id="8012a-142">Usamos esta función para ajustar los píxeles de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8012a-142">We use this function to adjust the image pixels.</span></span> <span data-ttu-id="8012a-143">Los valores x e y del punto negro y el punto blanco son las coordenadas de dos dimensiones que están conectadas para formar la transformación.</span><span class="sxs-lookup"><span data-stu-id="8012a-143">The x and y values of the black point and the white point are the coordinates in two dimensions that are connected to form the transform.</span></span> <span data-ttu-id="8012a-144">Cada una de las partes de la ecuación de salida final:</span><span class="sxs-lookup"><span data-stu-id="8012a-144">Each part of the final output equation:</span></span>

1.  <span data-ttu-id="8012a-145">Convierte los datos de imagen del espacio lineal al espacio no lineal usando esta ecuación:</span><span class="sxs-lookup"><span data-stu-id="8012a-145">Converts the image data from linear space to non-linear space using this equation:</span></span>![función auxiliar 1](images/brightness-formula2.png)

2.  <span data-ttu-id="8012a-147">Ajusta la imagen según estos valores:</span><span class="sxs-lookup"><span data-stu-id="8012a-147">Adjusts the image according to these values:</span></span>
    -   <span data-ttu-id="8012a-148">la *entrada* es los valores de intensidad de píxeles de la imagen de entrada de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="8012a-148">*input* is the input image pixel intensity values from 0 to 1.</span></span>

    -   <span data-ttu-id="8012a-149">*PT blanco (x, y)* ubicación de la curva de transformación para intensidades de píxeles más brillantes.</span><span class="sxs-lookup"><span data-stu-id="8012a-149">*White Pt. (x, y)* the location of the transform curve for brighter pixel intensities.</span></span>

    -   <span data-ttu-id="8012a-150">El punto *negro (x, y)* es la ubicación de la curva de transformación para la intensidad de los píxeles atenuados.</span><span class="sxs-lookup"><span data-stu-id="8012a-150">*Black Pt. (x, y)* is the location of the transform curve for dimmer pixel intensities.</span></span>

3.  <span data-ttu-id="8012a-151">Vuelve a convertir los datos de la imagen en el espacio lineal mediante esta ecuación:</span><span class="sxs-lookup"><span data-stu-id="8012a-151">Converts the image data back to linear space using this equation:</span></span> ![función auxiliar 2](images/brightness-formula3.png)

<span data-ttu-id="8012a-153">La ecuación de salida final y las partes del componente se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="8012a-153">The final output equation and the component parts are shown here.</span></span>

![los cálculos completos para el ajuste de brillo](images/brightness-formula4.png)

## <a name="output-bitmap"></a><span data-ttu-id="8012a-155">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8012a-155">Output bitmap</span></span>

<span data-ttu-id="8012a-156">El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="8012a-156">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="8012a-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8012a-157">Requirements</span></span>



| <span data-ttu-id="8012a-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="8012a-158">Requirement</span></span> | <span data-ttu-id="8012a-159">Value</span><span class="sxs-lookup"><span data-stu-id="8012a-159">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8012a-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8012a-160">Minimum supported client</span></span> | <span data-ttu-id="8012a-161">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8012a-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8012a-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8012a-162">Minimum supported server</span></span> | <span data-ttu-id="8012a-163">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8012a-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8012a-164">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8012a-164">Header</span></span>                   | <span data-ttu-id="8012a-165">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8012a-165">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8012a-166">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8012a-166">Library</span></span>                  | <span data-ttu-id="8012a-167">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8012a-167">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8012a-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8012a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8012a-169">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8012a-169">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

