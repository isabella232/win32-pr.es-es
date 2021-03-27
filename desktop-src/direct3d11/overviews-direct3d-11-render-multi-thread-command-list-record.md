---
title: Cómo grabar una lista de comandos
description: En este tema se muestra cómo crear y grabar una lista de comandos.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777082"
---
# <a name="how-to-record-a-command-list"></a><span data-ttu-id="fe1c4-103">Cómo: grabar una lista de comandos</span><span class="sxs-lookup"><span data-stu-id="fe1c4-103">How to: Record a Command List</span></span>

<span data-ttu-id="fe1c4-104">Una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) es una lista grabada de comandos de representación.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="fe1c4-105">En este tema se muestra cómo crear y grabar una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="fe1c4-105">This topic shows how to create and record a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="fe1c4-106">Use una lista de comandos para grabar comandos de representación y volver a reproducirlos más adelante.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-106">Use a command list to record render commands and play them back later.</span></span> <span data-ttu-id="fe1c4-107">Una lista de comandos es conveniente para dividir las tareas de representación entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-107">A command list is convenient for splitting rendering tasks between threads.</span></span>

<span data-ttu-id="fe1c4-108">**Para grabar una lista de comandos**</span><span class="sxs-lookup"><span data-stu-id="fe1c4-108">**To record a command list**</span></span>

1.  <span data-ttu-id="fe1c4-109">Se debe crear una lista de comandos a partir de un contexto diferido, que contiene las acciones de representación y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-109">A command list must be created from a deferred context, which contains device state and rendering actions.</span></span> <span data-ttu-id="fe1c4-110">Dado un dispositivo, cree un contexto diferido llamando a [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="fe1c4-110">Given a device, create a deferred context by calling [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  <span data-ttu-id="fe1c4-111">Use el contexto diferido para representarlo.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-111">Use the deferred context to render.</span></span>

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    <span data-ttu-id="fe1c4-112">En este sencillo ejemplo se borra un destino de representación, pero se pueden agregar comandos de representación adicionales.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-112">This simple example clears a render target, but you could add additional render commands.</span></span>

3.  <span data-ttu-id="fe1c4-113">Cree o grabe una lista de comandos mediante una llamada a [**ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) y pasando un puntero a una interfaz [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) no inicializada.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-113">Create/record a command list by calling [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) and passing a pointer to an uninitialized [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) interface.</span></span>

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    <span data-ttu-id="fe1c4-114">Cuando el método devuelve un resultado, se crea una lista de comandos que contiene todos los comandos de representación y se devuelve una interfaz a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-114">When the method returns, a command list is created containing all the render commands and an interface is returned to the application.</span></span>

    <span data-ttu-id="fe1c4-115">El parámetro Boolean indica al tiempo de ejecución qué hacer con el estado de la canalización en el contexto diferido.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-115">The boolean parameter tells the runtime what to do with the pipeline state in the deferred context.</span></span> <span data-ttu-id="fe1c4-116">**True** significa que se restaura el estado del contexto del dispositivo a su condición de lista de comandos previos cuando la grabación se completa, por lo que **false** significa que no se cambia el estado después de la grabación.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-116">**TRUE** means restore the state of the device context to its pre-command list condition when recording is completed, **FALSE** means do not change the state after recording.</span></span> <span data-ttu-id="fe1c4-117">Esto significa que el contexto de dispositivo reflejará los cambios de estado contenidos en la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="fe1c4-117">This means that the device context will reflect the state changes contained in the command list.</span></span>

<span data-ttu-id="fe1c4-118">Para ver un ejemplo de reproducción de una lista de comandos, consulte [Cómo: reproducir una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span><span class="sxs-lookup"><span data-stu-id="fe1c4-118">To see an example for playing back a command list, see [How to: Play Back a Command List](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe1c4-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe1c4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe1c4-120">Lista de comandos</span><span class="sxs-lookup"><span data-stu-id="fe1c4-120">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="fe1c4-121">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="fe1c4-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




