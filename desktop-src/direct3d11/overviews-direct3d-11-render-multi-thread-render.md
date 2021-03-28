---
title: Representación inmediata y diferida
description: Direct3D 11 admite dos tipos de representación inmediata y diferida. Ambos se implementan mediante la interfaz ID3D11DeviceContext.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef954a8e794755e1405c8e1e07505a5f39189b03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996777"
---
# <a name="immediate-and-deferred-rendering"></a>Representación inmediata y diferida

Direct3D 11 admite dos tipos de representación: inmediato y aplazado. Ambos se implementan mediante la interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

## <a name="immediate-rendering"></a>Representación inmediata

La representación inmediata hace referencia a la llamada de API o comandos de representación desde un dispositivo, que pone en cola los comandos de un búfer para su ejecución en la GPU. Usar un contexto inmediato para representar, establecer el estado de la canalización y reproducir una lista de comandos.

Cree un contexto inmediato mediante [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="deferred-rendering"></a>Representación diferida

La representación aplazada registra los comandos de gráficos en un búfer de comandos para que se puedan reproducir en otro momento. Use un contexto diferido para registrar comandos (representación y configuración de estado) en una lista de comandos. La representación diferida es un nuevo concepto en Direct3D 11; la representación diferida está diseñada para admitir la representación en un subproceso mientras se graban comandos para la representación en subprocesos adicionales. Esta estrategia paralela y multiproceso permite dividir escenas complejas en tareas simultáneas. Para obtener más información sobre la representación de escenas complejas, consulte [representación de varias pasadas](overviews-direct3d-11-render-multipass.md).

Cree un contexto diferido mediante [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Direct3D genera una sobrecarga de representación cuando pone en cola comandos en el búfer de comandos. En cambio, una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) se ejecuta mucho más eficazmente durante la reproducción. Para usar una lista de comandos, grabe los comandos de representación con un contexto diferido y vuelva a reproducirlos mediante un contexto inmediato.

Solo puede generar una lista de comandos única en un modo de un solo subproceso. Sin embargo, puede crear y usar varios contextos aplazados simultáneamente, cada uno en un subproceso independiente. Después, puede usar esos contextos diferidos para crear simultáneamente varias listas de comandos.

No se pueden reproducir dos o más listas de comandos simultáneamente en el contexto inmediato.

Para determinar si un contexto de dispositivo es un contexto inmediato o diferido, llame a [**ID3D11DeviceContext:: GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype).

El método [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) solo se admite en un contexto diferido para recursos dinámicos ([**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)), donde la primera llamada dentro de la lista de comandos es D3D11 el [**\_ \_ \_ descarte de escritura de asignación**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). **D3D11 \_ NO se admite la escritura de asignación \_ \_ sin \_** sobrescritura en las llamadas subsiguientes si están disponibles para el tipo de recurso especificado.

Las consultas en un contexto diferido se limitan a la generación de datos y al dibujo de predicado. No se puede llamar a [**ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) en un contexto diferido para obtener datos sobre una consulta; solo se puede llamar a **GetData** en el contexto inmediato para obtener datos sobre una consulta. Puede establecer un predicado de representación (un tipo de consulta) llamando a [**D3D11DeviceContext:: SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) para usar los resultados de la consulta en la GPU. Puede generar datos de consulta mediante llamadas a [**ID3D11DeviceContext:: Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) y [**ID3D11DeviceContext:: end**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end). Sin embargo, los datos de consulta no estarán disponibles hasta que llame a [**ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) en el contexto inmediato para enviar la lista de comandos de contexto aplazado. A continuación, la GPU procesa los datos de la consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




