---
title: Cómo reproducir una lista de comandos
description: En este tema se muestra cómo reproducir una lista de comandos.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566673"
---
# <a name="how-to-play-back-a-command-list"></a>Cómo: Reproducir una lista de comandos

Una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) es una lista registrada de comandos de representación. Use una lista de comandos para grabar previamente los comandos de dibujo y reproducirlos más adelante. En este tema se muestra cómo reproducir una lista [de comandos](overviews-direct3d-11-render-multi-thread-command-list.md). Se puede usar una lista de comandos para dividir las tareas de representación entre subprocesos.

En esta sección se describe cómo reproducir una lista de comandos. Para grabar una lista de comandos, [vea Cómo: Grabar una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md).

**Para reproducir una lista de comandos**

-   Llame [**a ID3D11DeviceContext::ExecuteCommandList y**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) pase un objeto [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) válido.
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

[**ExecuteCommandList debe**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) ejecutarse en el [contexto](overviews-direct3d-11-devices-intro.md) inmediato para que los comandos registrados se ejecuten en la unidad de procesamiento de gráficos (GPU). Use el contexto inmediato para alimentar comandos a la GPU para su ejecución, use un contexto aplazado para registrar comandos para su reproducción en otra lista de comandos. Cuando se llama **a ExecuteCommandList** en otro contexto diferido, se crea una lista de comandos aplazados "combinados". Para ejecutar los comandos en la lista de comandos aplazados combinados, debe ejecutarlos en el contexto inmediato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




