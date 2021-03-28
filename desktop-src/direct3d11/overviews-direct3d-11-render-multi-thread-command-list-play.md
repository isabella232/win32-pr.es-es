---
title: Cómo reproducir una lista de comandos
description: En este tema se muestra cómo reproducir una lista de comandos.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996768"
---
# <a name="how-to-play-back-a-command-list"></a><span data-ttu-id="19d4b-103">Cómo: reproducir una lista de comandos</span><span class="sxs-lookup"><span data-stu-id="19d4b-103">How to: Play Back a Command List</span></span>

<span data-ttu-id="19d4b-104">Una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) es una lista grabada de comandos de representación.</span><span class="sxs-lookup"><span data-stu-id="19d4b-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="19d4b-105">Use una lista de comandos para grabar previamente los comandos de dibujo y volver a reproducirlos más adelante.</span><span class="sxs-lookup"><span data-stu-id="19d4b-105">Use a command list to pre-record drawing commands and play them back later.</span></span> <span data-ttu-id="19d4b-106">En este tema se muestra cómo reproducir una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="19d4b-106">This topic shows how to play back a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="19d4b-107">Una lista de comandos se puede usar para dividir las tareas de representación entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="19d4b-107">A command list can be used to split rendering tasks between threads.</span></span>

<span data-ttu-id="19d4b-108">En esta sección se describe cómo reproducir una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="19d4b-108">This section describes how to play back a command list.</span></span> <span data-ttu-id="19d4b-109">Para grabar una lista de comandos, consulte [Cómo: grabar una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span><span class="sxs-lookup"><span data-stu-id="19d4b-109">For recording a command list, see [How to: Record a Command List](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span></span>

<span data-ttu-id="19d4b-110">**Para reproducir una lista de comandos**</span><span class="sxs-lookup"><span data-stu-id="19d4b-110">**To play back a command list**</span></span>

-   <span data-ttu-id="19d4b-111">Llame a [**ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) y pase un objeto [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) válido.</span><span class="sxs-lookup"><span data-stu-id="19d4b-111">Call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) and pass a valid [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) object.</span></span>
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

<span data-ttu-id="19d4b-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) se debe ejecutar en el [contexto inmediato](overviews-direct3d-11-devices-intro.md) para que se ejecuten los comandos grabados en la unidad de procesamiento de gráficos (GPU).</span><span class="sxs-lookup"><span data-stu-id="19d4b-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) must be executed on the [immediate context](overviews-direct3d-11-devices-intro.md) for recorded commands to be run on the graphics processing unit (GPU).</span></span> <span data-ttu-id="19d4b-113">Use el contexto inmediato para alimentar comandos a la GPU para su ejecución, use un contexto diferido para grabar comandos para la reproducción en otra lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="19d4b-113">Use the immediate context to feed commands to the GPU for execution, use a deferred context to record commands for playback onto another command list.</span></span> <span data-ttu-id="19d4b-114">Cuando se llama a **ExecuteCommandList** en otro contexto diferido, se crea una lista de comandos diferidos ' combinados '.</span><span class="sxs-lookup"><span data-stu-id="19d4b-114">When you call **ExecuteCommandList** onto another deferred context, you create a ‘merged’ deferred command list.</span></span> <span data-ttu-id="19d4b-115">Para ejecutar los comandos en la lista de comandos diferidos combinados, debe ejecutarlos en el contexto inmediato.</span><span class="sxs-lookup"><span data-stu-id="19d4b-115">To run the commands on the merged deferred command list, you need to execute them on the immediate context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19d4b-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19d4b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d4b-117">Lista de comandos</span><span class="sxs-lookup"><span data-stu-id="19d4b-117">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="19d4b-118">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="19d4b-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




