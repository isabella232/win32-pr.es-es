---
title: Cómo registrar una lista de comandos
description: En este tema se muestra cómo crear y registrar una lista de comandos.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570921"
---
# <a name="how-to-record-a-command-list"></a>Cómo: Registrar una lista de comandos

Una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) es una lista registrada de comandos de representación. En este tema se muestra cómo crear y registrar una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md). Use una lista de comandos para registrar comandos de representación y reproducirlos más adelante. Una lista de comandos es conveniente para dividir las tareas de representación entre subprocesos.

**Para registrar una lista de comandos**

1.  Se debe crear una lista de comandos a partir de un contexto diferido, que contiene el estado del dispositivo y las acciones de representación. Dado un dispositivo, cree un contexto aplazado mediante una llamada a [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  Use el contexto diferido para representarlo.

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    Este sencillo ejemplo borra un destino de representación, pero podría agregar comandos de representación adicionales.

3.  Cree o registre una lista de comandos llamando a [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) y pasando un puntero a una interfaz [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) sin inicializar.

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    Cuando el método devuelve un resultado, se crea una lista de comandos que contiene todos los comandos de representación y se devuelve una interfaz a la aplicación.

    El parámetro booleano indica al tiempo de ejecución qué hacer con el estado de canalización en el contexto diferido. **TRUE** significa restaurar el estado del contexto del dispositivo a su condición de lista de comandos previos cuando se completa la grabación, **FALSE** significa que no cambia el estado después de la grabación. Esto significa que el contexto del dispositivo reflejará los cambios de estado contenidos en la lista de comandos.

Para ver un ejemplo para reproducir una lista de comandos, vea Cómo: Reproducir [una lista de comandos.](overviews-direct3d-11-render-multi-thread-command-list-play.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




