---
description: Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Aplicar una técnica (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496013"
---
# <a name="apply-a-technique-direct3d-10"></a><span data-ttu-id="aaf19-103">Aplicar una técnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="aaf19-103">Apply a Technique (Direct3D 10)</span></span>

<span data-ttu-id="aaf19-104">Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaf19-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="aaf19-105">Establecer el estado de no sombreador en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="aaf19-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="aaf19-106">Algunos Estados de canalización no se establecen con un efecto.</span><span class="sxs-lookup"><span data-stu-id="aaf19-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="aaf19-107">Por ejemplo, el borrado de un destino de representación prepara el destino de representación para los datos.</span><span class="sxs-lookup"><span data-stu-id="aaf19-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="aaf19-108">Antes de establecer el estado del efecto en el dispositivo, este es un ejemplo de Cómo borrar los búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="aaf19-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="aaf19-109">Establecer el estado del efecto en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="aaf19-109">Set Effect State in the Device</span></span>

<span data-ttu-id="aaf19-110">El establecimiento del estado del efecto se realiza aplicando el estado del efecto en el bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="aaf19-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="aaf19-111">Esto se realiza desde fuera de.</span><span class="sxs-lookup"><span data-stu-id="aaf19-111">This is done from the outside in.</span></span> <span data-ttu-id="aaf19-112">Es decir, seleccione una técnica y, a continuación, establezca el estado de cada una de las pasadas (dependiendo del resultado deseado).</span><span class="sxs-lookup"><span data-stu-id="aaf19-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



<span data-ttu-id="aaf19-113">Un efecto no representa nada, simplemente establece el estado del efecto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaf19-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="aaf19-114">El código de representación se llama después de que el estado del efecto actualice el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaf19-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="aaf19-115">En este ejemplo, la llamada a DrawIndexed realiza la representación.</span><span class="sxs-lookup"><span data-stu-id="aaf19-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaf19-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aaf19-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaf19-117">Representar un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="aaf19-117">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



