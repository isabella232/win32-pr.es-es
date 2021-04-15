---
description: Varios destinos de representación (MRT) hacen referencia a la capacidad de representar en varias superficies (vea IDirect3D9Surface) con una única llamada a Draw.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Varios destinos de representación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495287"
---
# <a name="multiple-render-targets-direct3d-9"></a><span data-ttu-id="22361-103">Varios destinos de representación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="22361-103">Multiple Render Targets (Direct3D 9)</span></span>

<span data-ttu-id="22361-104">Varios destinos de representación (MRT) hacen referencia a la capacidad de representar en varias superficies (vea [**IDirect3D9Surface**](/windows/desktop/api)) con una única llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="22361-104">Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/desktop/api)) with a single draw call.</span></span> <span data-ttu-id="22361-105">Estas superficies pueden crearse de forma independiente entre sí.</span><span class="sxs-lookup"><span data-stu-id="22361-105">These surfaces can be created independently of each other.</span></span> <span data-ttu-id="22361-106">Los destinos de representación se pueden establecer mediante [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span><span class="sxs-lookup"><span data-stu-id="22361-106">Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span></span>

<span data-ttu-id="22361-107">Varios destinos de representación tienen las siguientes restricciones:</span><span class="sxs-lookup"><span data-stu-id="22361-107">Multiple render targets have the following restrictions:</span></span>

-   <span data-ttu-id="22361-108">Todas las superficies de destino de representación que se usan juntas deben tener la misma profundidad de bits, pero pueden tener distintos formatos, a menos que \_ se establezca el límite de MRTINDEPENDENTBITDEPTHS de D3DPMISCCAPS.</span><span class="sxs-lookup"><span data-stu-id="22361-108">All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.</span></span>
-   <span data-ttu-id="22361-109">Todas las superficies de un destino de representación múltiple deben tener el mismo ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="22361-109">All surfaces of a multiple render target should have the same width and height.</span></span>
-   <span data-ttu-id="22361-110">Algunas implementaciones no pueden realizar operaciones de sombreador de postpíxel en varios destinos de representación, entre los que se incluyen: sin interpolación, prueba alfa, sin vaho, sin fusión o enmascaramiento, excepto la prueba de la z y el estarcido.</span><span class="sxs-lookup"><span data-stu-id="22361-110">Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test.</span></span> <span data-ttu-id="22361-111">Los dispositivos que admiten operaciones de sombreador de postpíxel establecen el bit Cap en D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.</span><span class="sxs-lookup"><span data-stu-id="22361-111">Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.</span></span>

    <span data-ttu-id="22361-112">Cuando \_ se establece el límite de MRTPOSTPIXELSHADERBLENDING de D3DPMISCCAPS, primero debe consultar a [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con el \_ \_ \_ resultado de combinación de POSTPIXELSHADER de consulta de uso para el formato de superficie específico.</span><span class="sxs-lookup"><span data-stu-id="22361-112">When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format.</span></span> <span data-ttu-id="22361-113">Si es false, no habrá ninguna operación de fusión de sombreador de postpíxel disponible para ese formato de superficie específico.</span><span class="sxs-lookup"><span data-stu-id="22361-113">If false, no post-pixel shader blending operations will be available for that specific surface format.</span></span> <span data-ttu-id="22361-114">Si es true, se espera que el dispositivo aplique el mismo estado a todos los destinos de representación simultáneos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="22361-114">If true, the device is expected to apply the same state to all simultaneous render targets as follows:</span></span>

    -   <span data-ttu-id="22361-115">Alpha Blend: el valor de color de oCi se combina con el destino de representación iésimo.</span><span class="sxs-lookup"><span data-stu-id="22361-115">Alpha blend: The color value in oCi is blended with the ith render target.</span></span>
    -   <span data-ttu-id="22361-116">Prueba alfa: la comparación se realizará con oC0.</span><span class="sxs-lookup"><span data-stu-id="22361-116">Alpha test: Comparison will happen with oC0.</span></span> <span data-ttu-id="22361-117">Si se produce un error en la comparación, se finaliza la prueba de píxeles para todos los destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="22361-117">If the comparison fails, the pixel test is terminated for all render targets.</span></span>
    -   <span data-ttu-id="22361-118">Niebla: el destino de representación 0 se mostrará en la luneta trasera.</span><span class="sxs-lookup"><span data-stu-id="22361-118">Fog: Render target 0 will get fogged.</span></span> <span data-ttu-id="22361-119">Otros destinos de representación no están definidos.</span><span class="sxs-lookup"><span data-stu-id="22361-119">Other render targets are undefined.</span></span> <span data-ttu-id="22361-120">Las implementaciones pueden optar por la niebla de todos con el mismo estado.</span><span class="sxs-lookup"><span data-stu-id="22361-120">Implementations can choose to fog them all using the same state.</span></span>
    -   <span data-ttu-id="22361-121">Interpolación: sin definir.</span><span class="sxs-lookup"><span data-stu-id="22361-121">Dithering: Undefined.</span></span>

-   <span data-ttu-id="22361-122">No se admite el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="22361-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="22361-123">Algunas de las implementaciones no aplican la máscara de escritura de salida (D3DRS \_ COLORWRITEENABLE).</span><span class="sxs-lookup"><span data-stu-id="22361-123">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="22361-124">Las que pueden tener máscaras de escritura de color independientes.</span><span class="sxs-lookup"><span data-stu-id="22361-124">Those that can, have independent color write masks.</span></span> <span data-ttu-id="22361-125">Esto se expresa mediante un nuevo bit de capacidad.</span><span class="sxs-lookup"><span data-stu-id="22361-125">This is expressed using a new capability bit.</span></span> <span data-ttu-id="22361-126">El número de máscaras de escritura de color independientes disponibles será igual al número máximo de elementos que admite el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22361-126">The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.</span></span>

<span data-ttu-id="22361-127">Nuevas Cap de hardware:</span><span class="sxs-lookup"><span data-stu-id="22361-127">New hardware caps:</span></span>


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a><span data-ttu-id="22361-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22361-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22361-129">Canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="22361-129">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
