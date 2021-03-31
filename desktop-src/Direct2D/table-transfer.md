---
title: Efecto de transferencia de tabla
description: Utilice el efecto transferencia de tabla para asignar las intensidades de color de una imagen mediante una función de transferencia creada a partir de la interpolación de una lista de valores que proporcione.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- efecto de transferencia de tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490643"
---
# <a name="table-transfer-effect"></a><span data-ttu-id="a8388-104">Efecto de transferencia de tabla</span><span class="sxs-lookup"><span data-stu-id="a8388-104">Table transfer effect</span></span>

<span data-ttu-id="a8388-105">Utilice el efecto transferencia de tabla para asignar las intensidades de color de una imagen mediante una función de transferencia creada a partir de la interpolación de una lista de valores que proporcione.</span><span class="sxs-lookup"><span data-stu-id="a8388-105">Use the table transfer effect to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.</span></span>

<span data-ttu-id="a8388-106">El CLSID para este efecto es CLSID \_ D2D1TableTransfer.</span><span class="sxs-lookup"><span data-stu-id="a8388-106">The CLSID for this effect is CLSID\_D2D1TableTransfer.</span></span>

-   [<span data-ttu-id="a8388-107">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8388-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="a8388-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="a8388-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="a8388-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8388-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a8388-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8388-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="a8388-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8388-111">Example image</span></span>

<span data-ttu-id="a8388-112">La imagen siguiente muestra la entrada y la salida del efecto de transferencia de tabla.</span><span class="sxs-lookup"><span data-stu-id="a8388-112">The image here shows the input and output of the table transfer effect.</span></span>



| <span data-ttu-id="a8388-113">Antes</span><span class="sxs-lookup"><span data-stu-id="a8388-113">Before</span></span>                                                         |
|----------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)     |
| <span data-ttu-id="a8388-115">Después</span><span class="sxs-lookup"><span data-stu-id="a8388-115">After</span></span>                                                          |
| ![la imagen después de la transformación.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="a8388-117">La función de transferencia se basa en una lista de entradas V = (V0, V1, V2, V3, V?</span><span class="sxs-lookup"><span data-stu-id="a8388-117">The transfer function is based on a list of inputs V=(V0,V1,V2,V3, V?</span></span> <span data-ttu-id="a8388-118">, V<sub>n</sub>), donde N es el número de elementos-1.</span><span class="sxs-lookup"><span data-stu-id="a8388-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="a8388-119">La intensidad del píxel de entrada se representa como C. La intensidad de los píxeles de salida, C se puede calcular con la ecuación.</span><span class="sxs-lookup"><span data-stu-id="a8388-119">The input pixel intensity is represented as C. The output pixel intensity, C  can be calculated with the equation.</span></span>

<span data-ttu-id="a8388-120">Para un valor C, elija un valor k, de modo que: k/N = C < (k + 1)/N</span><span class="sxs-lookup"><span data-stu-id="a8388-120">For a value C, pick a value k, such that: k/N = C < (k+1)/N</span></span>

<span data-ttu-id="a8388-121">La salida C se calcula con la siguiente ecuación: C ' = V?</span><span class="sxs-lookup"><span data-stu-id="a8388-121">The output C  is calculated using the following equation: C' = V?</span></span> <span data-ttu-id="a8388-122">+ (C-k/N) \* N \* (V??? dimensional?</span><span class="sxs-lookup"><span data-stu-id="a8388-122">+ (C -  k/N) \* N \* (V???1?</span></span> <span data-ttu-id="a8388-123">-V?)</span><span class="sxs-lookup"><span data-stu-id="a8388-123">- V?)</span></span>

<span data-ttu-id="a8388-124">Este efecto funciona en imágenes alfa directas y premultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="a8388-124">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="a8388-125">El efecto genera mapas de bits alfa premultiplicados.</span><span class="sxs-lookup"><span data-stu-id="a8388-125">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="a8388-126">Este es el aspecto del gráfico de la función de transferencia de tabla si la propiedad de tabla está establecida en `[0.0, 0.25, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="a8388-126">Here is what the graph of table transfer function looks like if the table property is set to `[0.0, 0.25, 1.0]`.</span></span>

![gráfico de intensidad de píxeles para la función de transferencia de tabla.](images/table-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="a8388-128">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="a8388-128">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="a8388-129">Los valores de todos los canales de las propiedades de transferencia de tabla son no reunitarios y tienen un mínimo de 0,0 y un máximo de 1,0.</span><span class="sxs-lookup"><span data-stu-id="a8388-129">The values of all channels of the table transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="a8388-130">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="a8388-130">Display name and index enumeration</span></span>                                           | <span data-ttu-id="a8388-131">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a8388-131">Type and default value</span></span>                       | <span data-ttu-id="a8388-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8388-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8388-133">RedTable</span><span class="sxs-lookup"><span data-stu-id="a8388-133">RedTable</span></span><br/> <span data-ttu-id="a8388-134">D2D1 \_ TABLETRANSFER \_ prop \_ roja, \_ tabla</span><span class="sxs-lookup"><span data-stu-id="a8388-134">D2D1\_TABLETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="a8388-135">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="a8388-135">FLOAT\[\]</span></span><br/> <span data-ttu-id="a8388-136">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="a8388-136">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="a8388-137">Lista de valores que se usan para definir la función de transferencia para el canal rojo.</span><span class="sxs-lookup"><span data-stu-id="a8388-137">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a8388-138">RedDisable</span><span class="sxs-lookup"><span data-stu-id="a8388-138">RedDisable</span></span><br/> <span data-ttu-id="a8388-139">D2D1 \_ TABLETRANSFER \_ prop \_ rojo \_ deshabilitado</span><span class="sxs-lookup"><span data-stu-id="a8388-139">D2D1\_TABLETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="a8388-140">BOOL</span><span class="sxs-lookup"><span data-stu-id="a8388-140">BOOL</span></span><br/> <span data-ttu-id="a8388-141">false</span><span class="sxs-lookup"><span data-stu-id="a8388-141">FALSE</span></span><br/>             | <span data-ttu-id="a8388-142">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal rojo.</span><span class="sxs-lookup"><span data-stu-id="a8388-142">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="a8388-143">Si se establece en FALSE, se aplica la función RedTableTransfer al canal rojo.</span><span class="sxs-lookup"><span data-stu-id="a8388-143">If you set this to FALSE it applies the RedTableTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a8388-144">GreenTable</span><span class="sxs-lookup"><span data-stu-id="a8388-144">GreenTable</span></span><br/> <span data-ttu-id="a8388-145">D2D1 \_ TABLETRANSFER \_ prop \_ verde \_ tabla</span><span class="sxs-lookup"><span data-stu-id="a8388-145">D2D1\_TABLETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="a8388-146">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="a8388-146">FLOAT\[\]</span></span><br/> <span data-ttu-id="a8388-147">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="a8388-147">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="a8388-148">Lista de valores que se usan para definir la función de transferencia para el canal verde.</span><span class="sxs-lookup"><span data-stu-id="a8388-148">The list of values used to define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a8388-149">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="a8388-149">GreenDisable</span></span><br/> <span data-ttu-id="a8388-150">D2D1 \_ TABLETRANSFER \_ prop \_ verde \_ deshabilitada</span><span class="sxs-lookup"><span data-stu-id="a8388-150">D2D1\_TABLETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="a8388-151">BOOL</span><span class="sxs-lookup"><span data-stu-id="a8388-151">BOOL</span></span><br/> <span data-ttu-id="a8388-152">false</span><span class="sxs-lookup"><span data-stu-id="a8388-152">FALSE</span></span><br/>             | <span data-ttu-id="a8388-153">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal verde.</span><span class="sxs-lookup"><span data-stu-id="a8388-153">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="a8388-154">Si se establece en FALSE, se aplica la función GreenTableTransfer al canal verde.</span><span class="sxs-lookup"><span data-stu-id="a8388-154">If you set this to FALSE it applies the GreenTableTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a8388-155">BlueTable</span><span class="sxs-lookup"><span data-stu-id="a8388-155">BlueTable</span></span><br/> <span data-ttu-id="a8388-156">D2D1 \_ TABLETRANSFER \_ prop \_ \_ tabla azul</span><span class="sxs-lookup"><span data-stu-id="a8388-156">D2D1\_TABLETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="a8388-157">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="a8388-157">FLOAT\[\]</span></span><br/> <span data-ttu-id="a8388-158">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="a8388-158">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="a8388-159">Lista de valores que se usan para definir la función de transferencia del canal azul.</span><span class="sxs-lookup"><span data-stu-id="a8388-159">The list of values used to define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a8388-160">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="a8388-160">BlueDisable</span></span><br/> <span data-ttu-id="a8388-161">Deshabilitar D2D1 de TABLETRANSFER de la \_ \_ prop \_ azul \_</span><span class="sxs-lookup"><span data-stu-id="a8388-161">D2D1\_TABLETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="a8388-162">BOOL</span><span class="sxs-lookup"><span data-stu-id="a8388-162">BOOL</span></span><br/> <span data-ttu-id="a8388-163">false</span><span class="sxs-lookup"><span data-stu-id="a8388-163">FALSE</span></span><br/>             | <span data-ttu-id="a8388-164">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal azul.</span><span class="sxs-lookup"><span data-stu-id="a8388-164">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="a8388-165">Si se establece en FALSE, se aplica la función BlueTableTransfer al canal azul.</span><span class="sxs-lookup"><span data-stu-id="a8388-165">If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a8388-166">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="a8388-166">AlphaTable</span></span><br/> <span data-ttu-id="a8388-167">D2D1 \_ TABLE \_ Transfer \_ tabla \_ alfa \_</span><span class="sxs-lookup"><span data-stu-id="a8388-167">D2D1\_TABLE\_TRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>   | <span data-ttu-id="a8388-168">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="a8388-168">FLOAT\[\]</span></span><br/> <span data-ttu-id="a8388-169">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="a8388-169">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="a8388-170">Lista de valores utilizados para definir la función de transferencia para el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="a8388-170">The list of values used to define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a8388-171">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="a8388-171">AlphaDisable</span></span><br/> <span data-ttu-id="a8388-172">D2D1 \_ TABLETRANSFER \_ prop \_ alpha \_ deshabilitada</span><span class="sxs-lookup"><span data-stu-id="a8388-172">D2D1\_TABLETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="a8388-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="a8388-173">BOOL</span></span><br/> <span data-ttu-id="a8388-174">false</span><span class="sxs-lookup"><span data-stu-id="a8388-174">FALSE</span></span><br/>             | <span data-ttu-id="a8388-175">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal alfa.</span><span class="sxs-lookup"><span data-stu-id="a8388-175">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="a8388-176">Si se establece en FALSE, se aplica la función AlphaTableTransfer al canal alfa.</span><span class="sxs-lookup"><span data-stu-id="a8388-176">If you set this to FALSE it applies the AlphaTableTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a8388-177">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="a8388-177">ClampOutput</span></span><br/> <span data-ttu-id="a8388-178">Salida de la abrazadera de D2D1 \_ TABLETRANSFER \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8388-178">D2D1\_TABLETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="a8388-179">BOOL</span><span class="sxs-lookup"><span data-stu-id="a8388-179">BOOL</span></span><br/> <span data-ttu-id="a8388-180">false</span><span class="sxs-lookup"><span data-stu-id="a8388-180">FALSE</span></span><br/>             | <span data-ttu-id="a8388-181">Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a8388-181">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="a8388-182">El efecto fija los valores antes de que premultiplique el alfa.</span><span class="sxs-lookup"><span data-stu-id="a8388-182">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="a8388-183">Si establece este valor en TRUE, el efecto fijará los valores.</span><span class="sxs-lookup"><span data-stu-id="a8388-183">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="a8388-184">Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.</span><span class="sxs-lookup"><span data-stu-id="a8388-184">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a8388-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8388-185">Requirements</span></span>



| <span data-ttu-id="a8388-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8388-186">Requirement</span></span> | <span data-ttu-id="a8388-187">Value</span><span class="sxs-lookup"><span data-stu-id="a8388-187">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8388-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8388-188">Minimum supported client</span></span> | <span data-ttu-id="a8388-189">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="a8388-189">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a8388-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8388-190">Minimum supported server</span></span> | <span data-ttu-id="a8388-191">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="a8388-191">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a8388-192">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8388-192">Header</span></span>                   | <span data-ttu-id="a8388-193">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="a8388-193">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="a8388-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8388-194">Library</span></span>                  | <span data-ttu-id="a8388-195">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="a8388-195">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="a8388-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8388-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8388-197">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="a8388-197">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

