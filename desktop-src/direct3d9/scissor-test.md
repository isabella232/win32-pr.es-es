---
description: La prueba de tijera selecciona los píxeles que están fuera del rectángulo de tijeras, una subsección rectangular definida por el usuario del destino de representación.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Prueba de tijeras (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696092"
---
# <a name="scissor-test-direct3d-9"></a><span data-ttu-id="caaeb-103">Prueba de tijeras (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="caaeb-103">Scissor Test (Direct3D 9)</span></span>

<span data-ttu-id="caaeb-104">La prueba de tijera selecciona los píxeles que están fuera del rectángulo de tijeras, una subsección rectangular definida por el usuario del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="caaeb-104">The scissor test culls pixels that are outside of the scissor rectangle, a user-defined rectangular sub-section of the render target.</span></span>

<span data-ttu-id="caaeb-105">El rectángulo en tijeras puede usarse para indicar el área del destino de representación en la que se dibuja el mundo del juego.</span><span class="sxs-lookup"><span data-stu-id="caaeb-105">The scissor rectangle could be used to indicate the area of the render target where the game world is drawn.</span></span> <span data-ttu-id="caaeb-106">El área fuera del rectángulo se selecciona y podría estar dedicada a la GUI de un juego.</span><span class="sxs-lookup"><span data-stu-id="caaeb-106">The area outside the rectangle is culled and could be devoted to a game's GUI.</span></span> <span data-ttu-id="caaeb-107">La prueba de tijera no puede desactivar áreas no rectangulares.</span><span class="sxs-lookup"><span data-stu-id="caaeb-107">The scissor test cannot cull non-rectangular areas.</span></span>

<span data-ttu-id="caaeb-108">Los rectángulos con tijeras no se pueden establecer en un valor mayor que el destino de representación, pero se pueden establecer en un valor mayor que el de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="caaeb-108">Scissor rectangles cannot be set larger than the render target, but they can be set larger than the viewport.</span></span>

<span data-ttu-id="caaeb-109">El rectángulo en tijera se administra mediante un estado de representación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="caaeb-109">The scissor rectangle is managed by a device render state.</span></span> <span data-ttu-id="caaeb-110">Una prueba de tijera está habilitada o deshabilitada estableciendo renderstate en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="caaeb-110">A scissor test is enabled or disabled by setting the renderstate to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="caaeb-111">Esta prueba se realiza después de calcular el color del fragmento, pero antes de la prueba alfa.</span><span class="sxs-lookup"><span data-stu-id="caaeb-111">This test is performed after the fragment color is computed but before alpha testing.</span></span> <span data-ttu-id="caaeb-112">[**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) restablece el rectángulo de tijeras en el destino de representación completo, análogo al restablecimiento de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="caaeb-112">[**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) resets the scissor rectangle to the full render target, analogous to the viewport reset.</span></span> <span data-ttu-id="caaeb-113">[**IDirect3DDevice9:: SetScissorRect**](/windows/desktop/api) se registra con Stateblocks y [**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) con la configuración de todos los Estados (D3DSBT \_ todos los valores en [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span><span class="sxs-lookup"><span data-stu-id="caaeb-113">[**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) is recorded by stateblocks, and [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) with the all state setting (D3DSBT\_ALL value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span></span> <span data-ttu-id="caaeb-114">La prueba de tijeras también afecta a la operación Device [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) .</span><span class="sxs-lookup"><span data-stu-id="caaeb-114">The scissor test also affects the device [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) operation.</span></span>


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



<span data-ttu-id="caaeb-115">El rectángulo entre tijeras predeterminado es la ventanilla completa.</span><span class="sxs-lookup"><span data-stu-id="caaeb-115">The default scissor rectangle is the full viewport.</span></span>

<span data-ttu-id="caaeb-116">La prueba de tijeras se realiza justo después de que un sombreador de píxeles o la canalización de función fija complete el procesamiento de píxeles, tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="caaeb-116">Scissor testing is done just after pixel processing is completed by a pixel shader or the fixed function pipeline, as shown in the following diagram.</span></span>

![diagrama de Cuándo se realiza la prueba de tijeras en relación con otros pasos](images/scissor-test.png)

## <a name="related-topics"></a><span data-ttu-id="caaeb-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="caaeb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caaeb-119">Canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="caaeb-119">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
