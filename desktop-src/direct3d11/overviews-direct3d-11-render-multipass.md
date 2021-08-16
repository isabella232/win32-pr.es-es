---
title: Multiple-Pass Rendering
description: La representación de varios pasos es un proceso en el que una aplicación recorre su gráfico de escena varias veces con el fin de generar una salida para representarla en la pantalla.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242573dea2982f3525082187aad536a407e446c4ce59f116f53b8fa0d40fc582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124213"
---
# <a name="multiple-pass-rendering"></a>Multiple-Pass Rendering

La representación de varios pasos es un proceso en el que una aplicación recorre su gráfico de escena varias veces con el fin de generar una salida para representarla en la pantalla. La representación de varios pases mejora el rendimiento porque divide escenas complejas en tareas que se pueden ejecutar simultáneamente.

Para realizar la representación de varios pases, cree un contexto aplazado y una lista de comandos para cada paso adicional. Mientras la aplicación recorre el gráfico de escena, registra comandos (por ejemplo, comandos de representación como [**Draw)**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)en un contexto aplazado. Una vez que la aplicación finaliza el recorrido, llama al [**método FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) en el contexto diferido. Por último, la aplicación llama al [**método ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) en el contexto inmediato para ejecutar los comandos en cada lista de comandos.

El pseudocódigo siguiente muestra cómo realizar la representación de varios pasos:

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
> El contexto inmediato modifica un recurso, que está enlazado al contexto inmediato como una vista de destino de representación (RTV); En cambio, cada contexto aplazado simplemente usa el recurso , que está enlazado al contexto diferido como una vista de recursos de sombreador (SRV). Para obtener más información sobre los contextos inmediatos y diferidos, vea [Representación inmediata y diferida.](overviews-direct3d-11-render-multi-thread-render.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




