---
description: La mezcla alfa del búfer de fotogramas es un poco diferente que el vértice alfa, el alfa del material y la textura alfa.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Búfer de trama alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152115"
---
# <a name="frame-buffer-alpha-direct3d-9"></a><span data-ttu-id="427ce-103">Búfer de trama alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="427ce-103">Frame Buffer Alpha (Direct3D 9)</span></span>

<span data-ttu-id="427ce-104">La mezcla alfa del búfer de fotogramas es un poco diferente que el vértice alfa, el alfa del material y la textura alfa.</span><span class="sxs-lookup"><span data-stu-id="427ce-104">Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.</span></span> <span data-ttu-id="427ce-105">Los valores de transparencia de vértices, materiales y texturas que se usan solo para el primitivo actual y no tienen ningún efecto en otros tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="427ce-105">Vertex, material, and texture alpha set transparency values that are used only for the current primitive, and by themselves have no effect on other primitives.</span></span> <span data-ttu-id="427ce-106">La mezcla alfa de búfer de fotogramas controla cómo se combina el primitivo actual con los píxeles existentes en el búfer de fotogramas para producir un color de píxel final.</span><span class="sxs-lookup"><span data-stu-id="427ce-106">Frame buffer alpha-blending controls how the current primitive is combined with existing pixels in the frame buffer to yield a final pixel color.</span></span>

<span data-ttu-id="427ce-107">Al realizar la combinación alfa, se combinan dos colores: un color de origen y un color de destino.</span><span class="sxs-lookup"><span data-stu-id="427ce-107">When performing alpha blending, two colors are being combined: a source color and a destination color.</span></span> <span data-ttu-id="427ce-108">El color de origen es del objeto transparente, el color de destino es el color que ya está en la ubicación de píxeles.</span><span class="sxs-lookup"><span data-stu-id="427ce-108">The source color is from the transparent object, the destination color is the color already at the pixel location.</span></span> <span data-ttu-id="427ce-109">El color de destino es el resultado de representar algún otro objeto situado detrás del objeto transparente, es decir, el objeto que será visible a través del objeto transparente.</span><span class="sxs-lookup"><span data-stu-id="427ce-109">The destination color is the result of rendering some other object that is behind the transparent object, that is, the object that will be visible through the transparent object.</span></span> <span data-ttu-id="427ce-110">La combinación alfa utiliza una fórmula para controlar la relación entre los objetos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="427ce-110">Alpha blending uses a formula to control the ratio between the source and destination objects.</span></span>


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



<span data-ttu-id="427ce-111">ObjectColor es la contribución de la primitiva que se representa en la ubicación de píxeles actual.</span><span class="sxs-lookup"><span data-stu-id="427ce-111">ObjectColor is the contribution from the primitive being rendered at the current pixel location.</span></span> <span data-ttu-id="427ce-112">PixelColor es la contribución del búfer de fotogramas en la ubicación de píxeles actual.</span><span class="sxs-lookup"><span data-stu-id="427ce-112">PixelColor is the contribution from the frame buffer at the current pixel location.</span></span>

<span data-ttu-id="427ce-113">A continuación se enumera el conjunto de factores de mezcla alfa que se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="427ce-113">The set of alpha blend factors that can be used are listed below.</span></span>



| <span data-ttu-id="427ce-114">Factor de modo de mezcla</span><span class="sxs-lookup"><span data-stu-id="427ce-114">Blend mode factor</span></span>         | <span data-ttu-id="427ce-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="427ce-115">Description</span></span>                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="427ce-116">D3DBLEND \_ cero</span><span class="sxs-lookup"><span data-stu-id="427ce-116">D3DBLEND\_ZERO</span></span>            | <span data-ttu-id="427ce-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="427ce-117">(0, 0, 0, 0)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="427ce-118">D3DBLEND \_ uno</span><span class="sxs-lookup"><span data-stu-id="427ce-118">D3DBLEND\_ONE</span></span>             | <span data-ttu-id="427ce-119">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="427ce-119">(1, 1, 1, 1)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="427ce-120">D3DBLEND \_ SRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="427ce-120">D3DBLEND\_SRCCOLOR</span></span>        | <span data-ttu-id="427ce-121">(RS, GS, BS, as)</span><span class="sxs-lookup"><span data-stu-id="427ce-121">(Rs, Gs, Bs, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="427ce-122">D3DBLEND \_ INVSRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="427ce-122">D3DBLEND\_INVSRCCOLOR</span></span>     | <span data-ttu-id="427ce-123">(1-RS, 1-GS, 1-BS, 1-as)</span><span class="sxs-lookup"><span data-stu-id="427ce-123">(1-Rs, 1-Gs, 1-Bs, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="427ce-124">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="427ce-124">D3DBLEND\_SRCALPHA</span></span>        | <span data-ttu-id="427ce-125">(Como, como, como)</span><span class="sxs-lookup"><span data-stu-id="427ce-125">(As, As, As, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="427ce-126">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="427ce-126">D3DBLEND\_INVSRCALPHA</span></span>     | <span data-ttu-id="427ce-127">(1-as, 1-as, 1-as, 1-as)</span><span class="sxs-lookup"><span data-stu-id="427ce-127">(1-As, 1-As, 1-As, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="427ce-128">D3DBLEND \_ DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="427ce-128">D3DBLEND\_DESTALPHA</span></span>       | <span data-ttu-id="427ce-129">(Ad, ad, ad, ad)</span><span class="sxs-lookup"><span data-stu-id="427ce-129">(Ad, Ad, Ad, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="427ce-130">D3DBLEND \_ INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="427ce-130">D3DBLEND\_INVDESTALPHA</span></span>    | <span data-ttu-id="427ce-131">(1: AD, 1: AD, 1: AD, 1-ad)</span><span class="sxs-lookup"><span data-stu-id="427ce-131">(1-Ad, 1-Ad, 1-Ad, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="427ce-132">D3DBLEND \_ DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="427ce-132">D3DBLEND\_DESTCOLOR</span></span>       | <span data-ttu-id="427ce-133">(Rd, GD, BD, ad)</span><span class="sxs-lookup"><span data-stu-id="427ce-133">(Rd, Gd, Bd, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="427ce-134">D3DBLEND \_ INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="427ce-134">D3DBLEND\_INVDESTCOLOR</span></span>    | <span data-ttu-id="427ce-135">(1-Rd, 1-GD, 1-BD, 1-ad)</span><span class="sxs-lookup"><span data-stu-id="427ce-135">(1-Rd, 1-Gd, 1-Bd, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="427ce-136">D3DBLEND \_ SRCALPHASAT</span><span class="sxs-lookup"><span data-stu-id="427ce-136">D3DBLEND\_SRCALPHASAT</span></span>     | <span data-ttu-id="427ce-137">(f, f, f, 1); f = min (as, 1-ad)</span><span class="sxs-lookup"><span data-stu-id="427ce-137">(f, f, f, 1); f = min(As, 1-Ad)</span></span>                                                                                                                                                          |
| <span data-ttu-id="427ce-138">D3DBLEND \_ BOTHSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="427ce-138">D3DBLEND\_BOTHSRCALPHA</span></span>    | <span data-ttu-id="427ce-139">Obsoleto para DirectX 6 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="427ce-139">Obsolete for DirectX 6 and later.</span></span> <span data-ttu-id="427ce-140">Puede lograr el mismo efecto si establece los factores de mezcla de origen y destino en D3DBLEND \_ SRCALPHA y D3DBLEND \_ INVSRCALPHA en llamadas independientes.</span><span class="sxs-lookup"><span data-stu-id="427ce-140">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span> |
| <span data-ttu-id="427ce-141">D3DBLEND \_ BOTHINVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="427ce-141">D3DBLEND\_BOTHINVSRCALPHA</span></span> | <span data-ttu-id="427ce-142">Obsoleto para DirectX 6.</span><span class="sxs-lookup"><span data-stu-id="427ce-142">Obsolete for DirectX 6.</span></span> <span data-ttu-id="427ce-143">Puede lograr el mismo efecto si establece los factores de mezcla de origen y destino en D3DBLEND \_ INVSRCALPHA y D3DBLEND \_ SRCALPHA en llamadas independientes.</span><span class="sxs-lookup"><span data-stu-id="427ce-143">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_INVSRCALPHA and D3DBLEND\_SRCALPHA in separate calls.</span></span>           |
| <span data-ttu-id="427ce-144">D3DBLEND \_ BLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="427ce-144">D3DBLEND\_BLENDFACTOR</span></span>     | <span data-ttu-id="427ce-145">Use color. r, color. g, color. b y color. Obtenido de la configuración de BLENDFACTOR de D3DRS \_ .</span><span class="sxs-lookup"><span data-stu-id="427ce-145">Use color.r, color.g, color.b, and color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                                 |
| <span data-ttu-id="427ce-146">D3DBLEND \_ INVBLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="427ce-146">D3DBLEND\_INVBLENDFACTOR</span></span>  | <span data-ttu-id="427ce-147">Use 1-color. r, 1-color. g, 1-color. b y 1-color. obtenido del valor BLENDFACTOR de D3DRS \_ .</span><span class="sxs-lookup"><span data-stu-id="427ce-147">Use 1-color.r, 1-color.g, 1-color.b, and 1-color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                         |



 

<span data-ttu-id="427ce-148">Direct3D usa el \_ Estado de representación de ALPHABLENDENABLE de D3DRS para habilitar la combinación de transparencia alfa.</span><span class="sxs-lookup"><span data-stu-id="427ce-148">Direct3D uses the D3DRS\_ALPHABLENDENABLE render state to enable alpha transparency blending.</span></span> <span data-ttu-id="427ce-149">El tipo de combinación alfa que se realiza depende de los Estados de \_ representación D3DRS SRCBLEND y D3DRS \_ DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="427ce-149">The type of alpha blending that is done depends on the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span> <span data-ttu-id="427ce-150">Los Estados de mezcla de origen y destino se usan en pares.</span><span class="sxs-lookup"><span data-stu-id="427ce-150">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="427ce-151">El siguiente fragmento de código establece el estado de Blend de origen en D3DBLEND \_ SRCCOLOR y el estado de Blend de destino en D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="427ce-151">The following code fragment sets the source blend state to D3DBLEND\_SRCCOLOR and the destination blend state to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="427ce-152">Este código realiza una mezcla lineal entre el color de origen (el color de la primitiva que se representa en la ubicación actual) y el color de destino (el color de la ubicación actual en el búfer de marco).</span><span class="sxs-lookup"><span data-stu-id="427ce-152">This code performs a linear blend between the source color (the color of the primitive being rendered at the current location) and the destination color (the color at the current location in the frame buffer).</span></span> <span data-ttu-id="427ce-153">La apariencia resultante es similar a la del matiz con matices en el hecho de que parte del color del objeto de destino parezca transmitirse a través del objeto de origen. el resto de ellos parece ser absorbido.</span><span class="sxs-lookup"><span data-stu-id="427ce-153">The resulting appearance is similar to tinted glass in that some of the color of the destination object seems to be transmitted through the source object; the rest of it appears to be absorbed.</span></span>

<span data-ttu-id="427ce-154">Muchos de estos factores de mezcla requieren valores alfa en la textura para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="427ce-154">Many of these blend factors require alpha values in the texture to operate correctly.</span></span> <span data-ttu-id="427ce-155">Por lo tanto, cuando se usa el vértice o el alfa del material, la aplicación se restringe en qué modos se producirán resultados interesantes.</span><span class="sxs-lookup"><span data-stu-id="427ce-155">Thus, when using vertex or material alpha, the application is restricted as to which modes will produce interesting results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="427ce-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="427ce-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="427ce-157">Combinación alfa</span><span class="sxs-lookup"><span data-stu-id="427ce-157">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



