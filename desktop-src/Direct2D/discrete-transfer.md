---
title: Efecto de transferencia discreto
description: Use el efecto de transferencia discreta para asignar las intensidades de color de una imagen mediante una función de transferencia por pasos creada a partir de una lista de valores que proporcione.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- efecto de transferencia discreto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562953"
---
# <a name="discrete-transfer-effect"></a><span data-ttu-id="cafaa-104">Efecto de transferencia discreto</span><span class="sxs-lookup"><span data-stu-id="cafaa-104">Discrete transfer effect</span></span>

<span data-ttu-id="cafaa-105">Use el efecto de transferencia discreta para asignar las intensidades de color de una imagen mediante una función de transferencia por pasos creada a partir de una lista de valores que proporcione.</span><span class="sxs-lookup"><span data-stu-id="cafaa-105">Use the discrete transfer effect to map the color intensities of an image using a step transfer function created from a list of values you provide.</span></span>

<span data-ttu-id="cafaa-106">El CLSID para este efecto es CLSID \_ D2D1DiscreteTransfer.</span><span class="sxs-lookup"><span data-stu-id="cafaa-106">The CLSID for this effect is CLSID\_D2D1DiscreteTransfer.</span></span>

-   [<span data-ttu-id="cafaa-107">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="cafaa-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="cafaa-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="cafaa-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="cafaa-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cafaa-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cafaa-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cafaa-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="cafaa-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="cafaa-111">Example image</span></span>

<span data-ttu-id="cafaa-112">La imagen siguiente muestra la entrada y la salida del efecto de la transferencia discreta.</span><span class="sxs-lookup"><span data-stu-id="cafaa-112">The image here shows the input and output of the discrete transfer effect.</span></span>



| <span data-ttu-id="cafaa-113">Antes</span><span class="sxs-lookup"><span data-stu-id="cafaa-113">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)        |
| <span data-ttu-id="cafaa-115">Después</span><span class="sxs-lookup"><span data-stu-id="cafaa-115">After</span></span>                                                             |
| ![la imagen después de la transformación.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="cafaa-117">La función de transferencia se basa en la lista de entradas: V = (V0, V1, V2, V3, V?</span><span class="sxs-lookup"><span data-stu-id="cafaa-117">The transfer function is based on the list of inputs: V=(V0,V1,V2,V3,V?</span></span> <span data-ttu-id="cafaa-118">, V<sub>n</sub>), donde N es el número de elementos-1.</span><span class="sxs-lookup"><span data-stu-id="cafaa-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="cafaa-119">La intensidad del píxel de entrada se representa como C. La intensidad de los píxeles de salida, C se calcula con la ecuación:</span><span class="sxs-lookup"><span data-stu-id="cafaa-119">The input pixel intensity is represented as C. The output pixel intensity, C  is calculated with the equation:</span></span>

<span data-ttu-id="cafaa-120">Para un valor C, elija un valor k, de modo que:</span><span class="sxs-lookup"><span data-stu-id="cafaa-120">For a value C, pick a value k, such that:</span></span>

![fórmula para el proceso.](images/discrete-transfer1.png)

<span data-ttu-id="cafaa-122">La salida C se puede calcular mediante la ecuación: C ' = V?</span><span class="sxs-lookup"><span data-stu-id="cafaa-122">The output C  can be calculated using the equation: C' = V?</span></span>

<span data-ttu-id="cafaa-123">Este efecto funciona en imágenes alfa directas y premultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="cafaa-123">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="cafaa-124">El efecto genera mapas de bits alfa premultiplicados.</span><span class="sxs-lookup"><span data-stu-id="cafaa-124">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="cafaa-125">Este es el aspecto del gráfico de la función de transferencia discreta si las entradas son `[0.25, 0.5, 0.75, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="cafaa-125">Here is what the graph of discrete transfer function looks like if the inputs are `[0.25, 0.5, 0.75, 1.0]`.</span></span>

![gráfico de intensidad de píxeles para la función de transferencia discreta.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="cafaa-127">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="cafaa-127">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="cafaa-128">Los valores de todos los canales de las propiedades de transferencia discreta son independientes y tienen un mínimo de 0,0 y un máximo de 1,0.</span><span class="sxs-lookup"><span data-stu-id="cafaa-128">The values of all channels of the discrete transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="cafaa-129">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="cafaa-129">Display name and index enumeration</span></span>                                              | <span data-ttu-id="cafaa-130">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="cafaa-130">Type and default value</span></span>                       | <span data-ttu-id="cafaa-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="cafaa-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cafaa-132">RedTable</span><span class="sxs-lookup"><span data-stu-id="cafaa-132">RedTable</span></span><br/> <span data-ttu-id="cafaa-133">D2D1 \_ DISCRETETRANSFER \_ prop \_ roja, \_ tabla</span><span class="sxs-lookup"><span data-stu-id="cafaa-133">D2D1\_DISCRETETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="cafaa-134">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="cafaa-134">FLOAT\[\]</span></span><br/> <span data-ttu-id="cafaa-135">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cafaa-135">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cafaa-136">Lista de valores que se usan para definir la función de transferencia para el canal rojo.</span><span class="sxs-lookup"><span data-stu-id="cafaa-136">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cafaa-137">RedDisable</span><span class="sxs-lookup"><span data-stu-id="cafaa-137">RedDisable</span></span><br/> <span data-ttu-id="cafaa-138">D2D1 \_ DISCRETETRANSFER \_ prop \_ rojo \_ deshabilitado</span><span class="sxs-lookup"><span data-stu-id="cafaa-138">D2D1\_DISCRETETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="cafaa-139">BOOL</span><span class="sxs-lookup"><span data-stu-id="cafaa-139">BOOL</span></span><br/> <span data-ttu-id="cafaa-140">false</span><span class="sxs-lookup"><span data-stu-id="cafaa-140">FALSE</span></span><br/>             | <span data-ttu-id="cafaa-141">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal rojo.</span><span class="sxs-lookup"><span data-stu-id="cafaa-141">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="cafaa-142">Si se establece en FALSE, el efecto aplica la función RedDiscreteTransfer al canal rojo.</span><span class="sxs-lookup"><span data-stu-id="cafaa-142">If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cafaa-143">GreenTable</span><span class="sxs-lookup"><span data-stu-id="cafaa-143">GreenTable</span></span><br/> <span data-ttu-id="cafaa-144">D2D1 \_ DISCRETETRANSFER \_ prop \_ verde \_ tabla</span><span class="sxs-lookup"><span data-stu-id="cafaa-144">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="cafaa-145">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="cafaa-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="cafaa-146">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cafaa-146">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cafaa-147">Lista de valores que definen la función de transferencia para el canal verde.</span><span class="sxs-lookup"><span data-stu-id="cafaa-147">The list of values that define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cafaa-148">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="cafaa-148">GreenDisable</span></span><br/> <span data-ttu-id="cafaa-149">D2D1 \_ DISCRETETRANSFER \_ prop \_ verde \_ deshabilitada</span><span class="sxs-lookup"><span data-stu-id="cafaa-149">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="cafaa-150">BOOL</span><span class="sxs-lookup"><span data-stu-id="cafaa-150">BOOL</span></span><br/> <span data-ttu-id="cafaa-151">false</span><span class="sxs-lookup"><span data-stu-id="cafaa-151">FALSE</span></span><br/>             | <span data-ttu-id="cafaa-152">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal verde.</span><span class="sxs-lookup"><span data-stu-id="cafaa-152">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="cafaa-153">Si se establece en FALSE, el efecto aplica la función GreenDiscreteTransfer al canal verde.</span><span class="sxs-lookup"><span data-stu-id="cafaa-153">If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cafaa-154">BlueTable</span><span class="sxs-lookup"><span data-stu-id="cafaa-154">BlueTable</span></span><br/> <span data-ttu-id="cafaa-155">D2D1 \_ DISCRETETRANSFER \_ prop \_ \_ tabla azul</span><span class="sxs-lookup"><span data-stu-id="cafaa-155">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="cafaa-156">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="cafaa-156">FLOAT\[\]</span></span><br/> <span data-ttu-id="cafaa-157">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cafaa-157">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cafaa-158">Lista de valores que definen la función de transferencia para el canal azul.</span><span class="sxs-lookup"><span data-stu-id="cafaa-158">The list of values that define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cafaa-159">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="cafaa-159">BlueDisable</span></span><br/> <span data-ttu-id="cafaa-160">Deshabilitar D2D1 de DISCRETETRANSFER de la \_ \_ prop \_ azul \_</span><span class="sxs-lookup"><span data-stu-id="cafaa-160">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="cafaa-161">BOOL</span><span class="sxs-lookup"><span data-stu-id="cafaa-161">BOOL</span></span><br/> <span data-ttu-id="cafaa-162">false</span><span class="sxs-lookup"><span data-stu-id="cafaa-162">FALSE</span></span><br/>             | <span data-ttu-id="cafaa-163">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal azul.</span><span class="sxs-lookup"><span data-stu-id="cafaa-163">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="cafaa-164">Si se establece en FALSE, el efecto aplica la función BlueDiscreteTransfer al canal azul.</span><span class="sxs-lookup"><span data-stu-id="cafaa-164">If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cafaa-165">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="cafaa-165">AlphaTable</span></span><br/> <span data-ttu-id="cafaa-166">D2D1 \_ DISCRETETRANSFER \_ prop \_ \_ tabla alfa</span><span class="sxs-lookup"><span data-stu-id="cafaa-166">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>     | <span data-ttu-id="cafaa-167">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="cafaa-167">FLOAT\[\]</span></span><br/> <span data-ttu-id="cafaa-168">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cafaa-168">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cafaa-169">Lista de valores que definen la función de transferencia para el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="cafaa-169">The list of values that define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cafaa-170">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="cafaa-170">AlphaDisable</span></span><br/> <span data-ttu-id="cafaa-171">D2D1 \_ DISCRETETRANSFER \_ prop \_ alpha \_ deshabilitada</span><span class="sxs-lookup"><span data-stu-id="cafaa-171">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="cafaa-172">BOOL</span><span class="sxs-lookup"><span data-stu-id="cafaa-172">BOOL</span></span><br/> <span data-ttu-id="cafaa-173">false</span><span class="sxs-lookup"><span data-stu-id="cafaa-173">FALSE</span></span><br/>             | <span data-ttu-id="cafaa-174">Si se establece en TRUE, el efecto no aplica la función de transferencia al canal alfa.</span><span class="sxs-lookup"><span data-stu-id="cafaa-174">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="cafaa-175">Si se establece en FALSE, el efecto aplica la función AlphaDiscreteTransfer al canal alfa.</span><span class="sxs-lookup"><span data-stu-id="cafaa-175">If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cafaa-176">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="cafaa-176">ClampOutput</span></span><br/> <span data-ttu-id="cafaa-177">Salida de la abrazadera de D2D1 \_ DISCRETETRANSFER \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="cafaa-177">D2D1\_DISCRETETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="cafaa-178">BOOL</span><span class="sxs-lookup"><span data-stu-id="cafaa-178">BOOL</span></span><br/> <span data-ttu-id="cafaa-179">false</span><span class="sxs-lookup"><span data-stu-id="cafaa-179">FALSE</span></span><br/>             | <span data-ttu-id="cafaa-180">Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="cafaa-180">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="cafaa-181">El efecto fija los valores antes de que premultiplique el alfa.</span><span class="sxs-lookup"><span data-stu-id="cafaa-181">The effect clamps the values before it premultiplies the alpha.</span></span><br/> <span data-ttu-id="cafaa-182">Si establece este valor en TRUE, el efecto fijará los valores.</span><span class="sxs-lookup"><span data-stu-id="cafaa-182">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="cafaa-183">Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.</span><span class="sxs-lookup"><span data-stu-id="cafaa-183">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cafaa-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cafaa-184">Requirements</span></span>



| <span data-ttu-id="cafaa-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="cafaa-185">Requirement</span></span> | <span data-ttu-id="cafaa-186">Value</span><span class="sxs-lookup"><span data-stu-id="cafaa-186">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cafaa-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cafaa-187">Minimum supported client</span></span> | <span data-ttu-id="cafaa-188">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="cafaa-188">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cafaa-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cafaa-189">Minimum supported server</span></span> | <span data-ttu-id="cafaa-190">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="cafaa-190">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cafaa-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cafaa-191">Header</span></span>                   | <span data-ttu-id="cafaa-192">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="cafaa-192">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="cafaa-193">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cafaa-193">Library</span></span>                  | <span data-ttu-id="cafaa-194">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="cafaa-194">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="cafaa-195">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cafaa-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cafaa-196">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="cafaa-196">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

