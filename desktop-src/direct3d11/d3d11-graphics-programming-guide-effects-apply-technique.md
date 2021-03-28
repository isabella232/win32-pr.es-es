---
title: Aplicar una técnica (Direct3D 11)
description: Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e67668b27c1f0271974f20edc62619a7b1ae8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075811"
---
# <a name="apply-a-technique-direct3d-11"></a><span data-ttu-id="7e7ba-103">Aplicar una técnica (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="7e7ba-103">Apply a Technique (Direct3D 11)</span></span>

<span data-ttu-id="7e7ba-104">Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="7e7ba-105">Establecer el estado de no sombreador en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="7e7ba-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="7e7ba-106">Algunos Estados de canalización no se establecen con un efecto.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="7e7ba-107">Por ejemplo, el borrado de un destino de representación prepara el destino de representación para los datos.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="7e7ba-108">Antes de establecer el estado del efecto en el dispositivo, este es un ejemplo de Cómo borrar los búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="7e7ba-109">Establecer el estado del efecto en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="7e7ba-109">Set Effect State in the Device</span></span>

<span data-ttu-id="7e7ba-110">El establecimiento del estado del efecto se realiza aplicando el estado del efecto en el bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="7e7ba-111">Esto se realiza desde fuera de.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-111">This is done from the outside in.</span></span> <span data-ttu-id="7e7ba-112">Es decir, seleccione una técnica y, a continuación, establezca el estado de cada una de las pasadas (dependiendo del resultado deseado).</span><span class="sxs-lookup"><span data-stu-id="7e7ba-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D11_TECHNIQUE_DESC techDesc;
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



<span data-ttu-id="7e7ba-113">Un efecto no representa nada, simplemente establece el estado del efecto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="7e7ba-114">El código de representación se llama después de que el estado del efecto actualice el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="7e7ba-115">En este ejemplo, la llamada a DrawIndexed realiza la representación.</span><span class="sxs-lookup"><span data-stu-id="7e7ba-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e7ba-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e7ba-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e7ba-117">Representar un efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="7e7ba-117">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




