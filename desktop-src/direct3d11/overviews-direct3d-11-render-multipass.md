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
# <a name="multiple-pass-rendering"></a>Multiple-Pass representación

La representación de varias pasadas es un proceso en el que una aplicación atraviesa su gráfico de escenas varias veces para producir una salida que se represente en la pantalla. La representación de varias pasadas mejora el rendimiento porque divide escenas complejas en tareas que se pueden ejecutar simultáneamente.

Para realizar una representación de varias pasadas, se crea un contexto y una lista de comandos aplazados para cada paso adicional. Mientras la aplicación atraviesa el gráfico de escenas, registra comandos (por ejemplo, comandos de representación como [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) en un contexto diferido. Una vez que la aplicación finaliza el recorrido, llama al método [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) en el contexto diferido. Por último, la aplicación llama al método [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) en el contexto inmediato para ejecutar los comandos en cada lista de comandos.

En el siguiente pseudocódigo se muestra cómo realizar la representación de varias pasadas:

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
> El contexto inmediato modifica un recurso, que está enlazado al contexto inmediato como una vista de destino de representación (RTV); por el contrario, cada contexto diferido simplemente usa el recurso, que está enlazado al contexto diferido como vista de recursos del sombreador (SRV). Para obtener más información sobre los contextos inmediatos y aplazados, consulte [representación inmediata y diferida](overviews-direct3d-11-render-multi-thread-render.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




