---
description: Las aplicaciones usan el búfer de estarcido para enmascarar los píxeles de una imagen. La máscara controla si el píxel se dibuja o no. A continuación se muestran algunos de los efectos más comunes.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Técnicas de búfer de estarcido (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423151"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a><span data-ttu-id="393e7-105">Técnicas de búfer de estarcido (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="393e7-105">Stencil Buffer Techniques (Direct3D 9)</span></span>

<span data-ttu-id="393e7-106">Las aplicaciones usan el búfer de estarcido para enmascarar los píxeles de una imagen.</span><span class="sxs-lookup"><span data-stu-id="393e7-106">Applications use the stencil buffer to mask pixels in an image.</span></span> <span data-ttu-id="393e7-107">La máscara controla si el píxel se dibuja o no.</span><span class="sxs-lookup"><span data-stu-id="393e7-107">The mask controls whether the pixel is drawn or not.</span></span> <span data-ttu-id="393e7-108">A continuación se muestran algunos de los efectos más comunes.</span><span class="sxs-lookup"><span data-stu-id="393e7-108">Some of the more common effects are shown below.</span></span>

-   [<span data-ttu-id="393e7-109">Composición</span><span class="sxs-lookup"><span data-stu-id="393e7-109">Compositing</span></span>](compositing.md)
-   [<span data-ttu-id="393e7-110">Marcas</span><span class="sxs-lookup"><span data-stu-id="393e7-110">Decaling</span></span>](decaling.md)
-   [<span data-ttu-id="393e7-111">Resuelve, atenúa y deslizar rápidamente</span><span class="sxs-lookup"><span data-stu-id="393e7-111">Dissolves, Fades, and Swipes</span></span>](dissolves--fades--and-swipes.md)
-   [<span data-ttu-id="393e7-112">Contornos y siluetas</span><span class="sxs-lookup"><span data-stu-id="393e7-112">Outlines and Silhouettes</span></span>](outlines-and-silhouettes.md)
-   [<span data-ttu-id="393e7-113">Galería de símbolos de dos caras</span><span class="sxs-lookup"><span data-stu-id="393e7-113">Two-Sided Stencil</span></span>](two-sided-stencil.md)

<span data-ttu-id="393e7-114">El búfer de estarcido habilita o deshabilita el dibujo en la superficie de destino de representación en píxel por píxel.</span><span class="sxs-lookup"><span data-stu-id="393e7-114">The stencil buffer enables or disables drawing to the rendering target surface on a pixel-by-pixel basis.</span></span> <span data-ttu-id="393e7-115">En su nivel más básico, permite a las aplicaciones enmascarar las secciones de la imagen representada para que no se muestren.</span><span class="sxs-lookup"><span data-stu-id="393e7-115">At its most fundamental level, it enables applications to mask sections of the rendered image so that they are not displayed.</span></span> <span data-ttu-id="393e7-116">A menudo, las aplicaciones utilizan búferes de estarcido para efectos especiales como la resolución, la alineación y la esquematización.</span><span class="sxs-lookup"><span data-stu-id="393e7-116">Applications often use stencil buffers for special effects such as dissolves, decaling, and outlining.</span></span>

<span data-ttu-id="393e7-117">La información del búfer de estarcido se incrusta en los datos del búfer z.</span><span class="sxs-lookup"><span data-stu-id="393e7-117">Stencil buffer information is embedded in the z-buffer data.</span></span> <span data-ttu-id="393e7-118">La aplicación puede usar el método [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) para comprobar la compatibilidad con la galería de símbolos de hardware, tal como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="393e7-118">Your application can use the [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) method to check for hardware stencil support, as shown in the following code example.</span></span>


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



<span data-ttu-id="393e7-119">[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) permite elegir un dispositivo para crearlo en función de las capacidades de dicho dispositivo.</span><span class="sxs-lookup"><span data-stu-id="393e7-119">[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="393e7-120">En este caso, se rechazan los dispositivos que no admiten búferes de estarcido de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="393e7-120">In this case, devices that do not support 8-bit stencil buffers are rejected.</span></span> <span data-ttu-id="393e7-121">Tenga en cuenta que este es solo un uso posible para **IDirect3D9:: CheckDeviceFormat**; para obtener más información [, vea determinar la compatibilidad de hardware (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="393e7-121">Note that this is only one possible use for **IDirect3D9::CheckDeviceFormat**; for details see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>

## <a name="how-the-stencil-buffer-works"></a><span data-ttu-id="393e7-122">Cómo funciona el búfer de estarcido</span><span class="sxs-lookup"><span data-stu-id="393e7-122">How the Stencil Buffer Works</span></span>

<span data-ttu-id="393e7-123">Direct3D realiza una prueba en el contenido del búfer de estarcido píxel a píxel.</span><span class="sxs-lookup"><span data-stu-id="393e7-123">Direct3D performs a test on the contents of the stencil buffer on a pixel-by-pixel basis.</span></span> <span data-ttu-id="393e7-124">Para cada píxel de la superficie de destino, realiza una prueba usando el valor correspondiente en el búfer de la galería de símbolos, un valor de referencia de la galería de símbolos y un valor de máscara de estarcido.</span><span class="sxs-lookup"><span data-stu-id="393e7-124">For each pixel in the target surface, it performs a test using the corresponding value in the stencil buffer, a stencil reference value, and a stencil mask value.</span></span> <span data-ttu-id="393e7-125">Si se supera la prueba, Direct3D realiza una acción.</span><span class="sxs-lookup"><span data-stu-id="393e7-125">If the test passes, Direct3D performs an action.</span></span> <span data-ttu-id="393e7-126">La prueba se realiza mediante los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="393e7-126">The test is performed using the following steps.</span></span>

1.  <span data-ttu-id="393e7-127">Realiza una operación and bit a bit del valor de referencia de la galería de símbolos con la máscara de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="393e7-127">Perform a bitwise AND operation of the stencil reference value with the stencil mask.</span></span>
2.  <span data-ttu-id="393e7-128">Realiza una operación and bit a bit del valor del búfer de estarcido del píxel actual con la máscara de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="393e7-128">Perform a bitwise AND operation of the stencil buffer value for the current pixel with the stencil mask.</span></span>
3.  <span data-ttu-id="393e7-129">Compare el resultado del paso 1 con el resultado del paso 2, mediante la función de comparación.</span><span class="sxs-lookup"><span data-stu-id="393e7-129">Compare the result of step 1 to the result of step 2, using the comparison function.</span></span>

<span data-ttu-id="393e7-130">Estos pasos se muestran en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="393e7-130">These steps are shown in the following code example.</span></span>


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



<span data-ttu-id="393e7-131">es el contenido del búfer de estarcido del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="393e7-131">is the contents of the stencil buffer for the current pixel.</span></span> <span data-ttu-id="393e7-132">En este ejemplo de código se usa el símbolo de y comercial (&) para representar la operación and bit a bit.</span><span class="sxs-lookup"><span data-stu-id="393e7-132">This code example uses the ampersand (&) symbol to represent the bitwise AND operation.</span></span>


```
StencilMask
```



<span data-ttu-id="393e7-133">representa el valor de la máscara de la galería de símbolos y</span><span class="sxs-lookup"><span data-stu-id="393e7-133">represents the value of the stencil mask, and</span></span>


```
StencilRef
```



<span data-ttu-id="393e7-134">representa el valor de referencia de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="393e7-134">represents the stencil reference value.</span></span>


```
CompFunc
```



<span data-ttu-id="393e7-135">es la función de comparación.</span><span class="sxs-lookup"><span data-stu-id="393e7-135">is the comparison function.</span></span>

<span data-ttu-id="393e7-136">El píxel actual se escribe en la superficie de destino si se supera la prueba del estarcido y se omite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="393e7-136">The current pixel is written to the target surface if the stencil test passes, and is ignored otherwise.</span></span> <span data-ttu-id="393e7-137">El comportamiento de comparación predeterminado es escribir el píxel, independientemente de cómo se desactive cada operación bit a bit (D3DCMP \_ siempre).</span><span class="sxs-lookup"><span data-stu-id="393e7-137">The default comparison behavior is to write the pixel, no matter how each bitwise operation turns out (D3DCMP\_ALWAYS).</span></span> <span data-ttu-id="393e7-138">Puede cambiar este comportamiento cambiando el valor de D3DRS \_ STENCILFUNC Render State, pasando un miembro del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) para identificar la función de comparación deseada.</span><span class="sxs-lookup"><span data-stu-id="393e7-138">You can change this behavior by changing the value of the D3DRS\_STENCILFUNC render state, passing a member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type to identify the desired comparison function.</span></span>

<span data-ttu-id="393e7-139">La aplicación puede personalizar el funcionamiento del búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="393e7-139">Your application can customize the operation of the stencil buffer.</span></span> <span data-ttu-id="393e7-140">Puede establecer la función de comparación, la máscara de la galería de símbolos y el valor de referencia de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="393e7-140">It can set the comparison function, the stencil mask, and the stencil reference value.</span></span> <span data-ttu-id="393e7-141">También puede controlar la acción que Direct3D realiza cuando la prueba de estarcido supera o produce un error.</span><span class="sxs-lookup"><span data-stu-id="393e7-141">It can also control the action that Direct3D takes when the stencil test passes or fails.</span></span> <span data-ttu-id="393e7-142">Para obtener más información, vea [cliché buffer State (Direct3D 9)](stencil-buffer-state.md).</span><span class="sxs-lookup"><span data-stu-id="393e7-142">For more information, see [Stencil Buffer State (Direct3D 9)](stencil-buffer-state.md).</span></span>

## <a name="examples"></a><span data-ttu-id="393e7-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="393e7-143">Examples</span></span>

<span data-ttu-id="393e7-144">En los siguientes ejemplos de código se muestra cómo configurar el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="393e7-144">The following code examples demonstrate setting up the stencil buffer.</span></span>


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



<span data-ttu-id="393e7-145">De forma predeterminada, el valor de referencia de la galería de símbolos es cero.</span><span class="sxs-lookup"><span data-stu-id="393e7-145">By default, the stencil reference value is zero.</span></span> <span data-ttu-id="393e7-146">Cualquier valor entero es válido.</span><span class="sxs-lookup"><span data-stu-id="393e7-146">Any integer value is valid.</span></span> <span data-ttu-id="393e7-147">Direct3D realiza una operación and bit a bit del valor de referencia de la galería de símbolos y un valor de máscara de galería de símbolos antes de la prueba.</span><span class="sxs-lookup"><span data-stu-id="393e7-147">Direct3D performs a bitwise AND of the stencil reference value and a stencil mask value before the stencil test.</span></span>

<span data-ttu-id="393e7-148">Puede controlar qué información de píxeles se escribe en función de la comparación de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="393e7-148">You can control what pixel information is written out depending on the stencil comparison.</span></span>


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



<span data-ttu-id="393e7-149">Puede escribir su propia fórmula para el valor que desea escribir en el búfer de estarcido, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="393e7-149">You can write your own formula for the value you want written into the stencil buffer as shown in the following example.</span></span>


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a><span data-ttu-id="393e7-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="393e7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="393e7-151">Canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="393e7-151">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
