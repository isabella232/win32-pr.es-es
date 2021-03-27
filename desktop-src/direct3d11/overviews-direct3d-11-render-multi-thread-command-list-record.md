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
# <a name="how-to-record-a-command-list"></a>Cómo: grabar una lista de comandos

Una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) es una lista grabada de comandos de representación. En este tema se muestra cómo crear y grabar una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md). Use una lista de comandos para grabar comandos de representación y volver a reproducirlos más adelante. Una lista de comandos es conveniente para dividir las tareas de representación entre subprocesos.

**Para grabar una lista de comandos**

1.  Se debe crear una lista de comandos a partir de un contexto diferido, que contiene las acciones de representación y estado del dispositivo. Dado un dispositivo, cree un contexto diferido llamando a [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

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

    

    En este sencillo ejemplo se borra un destino de representación, pero se pueden agregar comandos de representación adicionales.

3.  Cree o grabe una lista de comandos mediante una llamada a [**ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) y pasando un puntero a una interfaz [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) no inicializada.

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    Cuando el método devuelve un resultado, se crea una lista de comandos que contiene todos los comandos de representación y se devuelve una interfaz a la aplicación.

    El parámetro Boolean indica al tiempo de ejecución qué hacer con el estado de la canalización en el contexto diferido. **True** significa que se restaura el estado del contexto del dispositivo a su condición de lista de comandos previos cuando la grabación se completa, por lo que **false** significa que no se cambia el estado después de la grabación. Esto significa que el contexto de dispositivo reflejará los cambios de estado contenidos en la lista de comandos.

Para ver un ejemplo de reproducción de una lista de comandos, consulte [Cómo: reproducir una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




