---
title: Multiple-Pass representación
description: La representación de varias pasadas es un proceso en el que una aplicación atraviesa su gráfico de escenas varias veces para producir una salida que se represente en la pantalla.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fcf7f3f04bd641fdf82c9cf317e8a2ec99e85c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357304"
---
# <a name="multiple-pass-rendering"></a><span data-ttu-id="ea78d-103">Multiple-Pass representación</span><span class="sxs-lookup"><span data-stu-id="ea78d-103">Multiple-Pass Rendering</span></span>

<span data-ttu-id="ea78d-104">La representación de varias pasadas es un proceso en el que una aplicación atraviesa su gráfico de escenas varias veces para producir una salida que se represente en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ea78d-104">Multiple-pass rendering is a process in which an application traverses its scene graph multiple times in order to produce an output to render to the display.</span></span> <span data-ttu-id="ea78d-105">La representación de varias pasadas mejora el rendimiento porque divide escenas complejas en tareas que se pueden ejecutar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="ea78d-105">Multiple-pass rendering improves performance because it breaks up complex scenes into tasks that can run concurrently.</span></span>

<span data-ttu-id="ea78d-106">Para realizar una representación de varias pasadas, se crea un contexto y una lista de comandos aplazados para cada paso adicional.</span><span class="sxs-lookup"><span data-stu-id="ea78d-106">To perform multiple-pass rendering, you create a deferred context and command list for each additional pass.</span></span> <span data-ttu-id="ea78d-107">Mientras la aplicación atraviesa el gráfico de escenas, registra comandos (por ejemplo, comandos de representación como [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) en un contexto diferido.</span><span class="sxs-lookup"><span data-stu-id="ea78d-107">While the application traverses the scene graph, it records commands (for example, rendering commands such as [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) into a deferred context.</span></span> <span data-ttu-id="ea78d-108">Una vez que la aplicación finaliza el recorrido, llama al método [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) en el contexto diferido.</span><span class="sxs-lookup"><span data-stu-id="ea78d-108">After the application finishes the traversal, it calls the [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) method on the deferred context.</span></span> <span data-ttu-id="ea78d-109">Por último, la aplicación llama al método [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) en el contexto inmediato para ejecutar los comandos en cada lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="ea78d-109">Finally, the application calls the [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) method on the immediate context to execute the commands in each command list.</span></span>

<span data-ttu-id="ea78d-110">En el siguiente pseudocódigo se muestra cómo realizar la representación de varias pasadas:</span><span class="sxs-lookup"><span data-stu-id="ea78d-110">The following pseudocode shows how to perform multiple-pass rendering:</span></span>

``` syntax
{
 ImmCtx->SetRenderTarget( pRTViewOfResourceX );
 DefCtx1->SetTexture( pSRView1OfResourceX );
 DefCtx2->SetTexture( pSRView2OfResourceX );

 for () // Traverse the scene graph.
  {
    ImmCtx->Draw(); // Pass 0: immediate context renders primitives into resource X.

    // The following texturing by the deferred contexts occurs after the 
    // immediate context makes calls to ExecuteCommandList. 
    // Resource X is then comletely updated by the immediate context. 
    DefCtx1->Draw(); // Pass 1: deferred context 1 performs texturing from resource X.
    DefCtx2->Draw(); // Pass 2: deferred context 2 performs texturing from resource X.
      }

  // Create command lists and record commands into them.
  DefCtx1->FinishCommandList( &pCL1 ); 
  DefCtx2->FinishCommandList( &pCL2 );

  ImmCtx->ExecuteCommandList( pCL1 ); // Execute pass 1.
  ImmCtx->ExecuteCommandList( pCL2 ); // Exeucte pass 2.
}
```

> [!Note]  
> <span data-ttu-id="ea78d-111">El contexto inmediato modifica un recurso, que está enlazado al contexto inmediato como una vista de destino de representación (RTV); por el contrario, cada contexto diferido simplemente usa el recurso, que está enlazado al contexto diferido como vista de recursos del sombreador (SRV).</span><span class="sxs-lookup"><span data-stu-id="ea78d-111">The immediate context modifies a resource, which is bound to the immediate context as a render target view (RTV); in contrast, each deferred context simply uses the resource, which is bound to the deferred context as a shader resource view (SRV).</span></span> <span data-ttu-id="ea78d-112">Para obtener más información sobre los contextos inmediatos y aplazados, consulte [representación inmediata y diferida](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="ea78d-112">For more information about immediate and deferred contexts, see [Immediate and Deferred Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ea78d-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea78d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea78d-114">Representación</span><span class="sxs-lookup"><span data-stu-id="ea78d-114">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




