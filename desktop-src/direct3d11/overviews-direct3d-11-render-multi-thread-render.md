---
title: Representación inmediata y diferida
description: Direct3D 11 admite dos tipos de representación inmediata y diferida. Ambos se implementan mediante la interfaz ID3D11DeviceContext.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740a957ec4b7f2edacb4b753c7f68230494b10cf33721ef6c2d869de334517b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912937"
---
# <a name="immediate-and-deferred-rendering"></a>Representación inmediata y diferida

Direct3D 11 admite dos tipos de representación: inmediato y diferido. Ambos se implementan mediante la interfaz [**ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

## <a name="immediate-rendering"></a>Representación inmediata

La representación inmediata hace referencia a la llamada a las API o comandos de representación desde un dispositivo, que pone en cola los comandos en un búfer para su ejecución en la GPU. Use un contexto inmediato para representar, establecer el estado de la canalización y reproducir una lista de comandos.

Cree un contexto inmediato mediante [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="deferred-rendering"></a>Representación diferida

La representación diferida registra comandos gráficos en un búfer de comandos para que se puedan reproducir en otro momento. Use un contexto diferido para registrar comandos (representación y configuración de estado) en una lista de comandos. La representación aplazada es un nuevo concepto de Direct3D 11; la representación diferida está diseñada para admitir la representación en un subproceso mientras se graban comandos para la representación en subprocesos adicionales. Esta estrategia paralela multiproceso permite dividir escenas complejas en tareas simultáneas. Para obtener más información sobre la representación de escenas complejas, [vea Multiple-Pass Rendering](overviews-direct3d-11-render-multipass.md).

Cree un contexto diferido [**mediante ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Direct3D genera una sobrecarga de representación cuando pone en cola comandos en el búfer de comandos. Por el contrario, una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) se ejecuta mucho más eficazmente durante la reproducción. Para usar una lista de comandos, registre los comandos de representación con un contexto diferido y reprodúslos con un contexto inmediato.

Solo puede generar una lista de comandos única de un solo subproceso. Sin embargo, puede crear y usar varios contextos diferidos simultáneamente, cada uno en un subproceso independiente. A continuación, puede usar esos varios contextos diferidos para crear simultáneamente varias listas de comandos.

No se pueden reproducir dos o más listas de comandos simultáneamente en el contexto inmediato.

Para determinar si un contexto de dispositivo es inmediato o diferido, llame a [**ID3D11DeviceContext::GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype).

El [**método ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) solo se admite en un contexto diferido para recursos dinámicos [**(D3D11 \_ USAGE \_ DYNAMIC),**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)donde la primera llamada dentro de la lista de comandos es [**D3D11 \_ MAP WRITE \_ \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). **D3D11 \_ MAP \_ WRITE \_ NO \_ OVERWRITE** se admite en llamadas posteriores si están disponibles para el tipo de recurso especificado.

Las consultas en un contexto diferido se limitan a la generación de datos y al dibujo predicado. No se puede llamar a [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) en un contexto diferido para obtener datos sobre una consulta; Solo puede llamar a **GetData en** el contexto inmediato para obtener datos sobre una consulta. Puede establecer un predicado de representación (un tipo de consulta) llamando a [**D3D11DeviceContext::SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) para usar los resultados de la consulta en la GPU. Puede generar datos de consulta mediante llamadas a [**ID3D11DeviceContext::Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) e [**ID3D11DeviceContext::End**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end). Sin embargo, los datos de consulta no estarán disponibles hasta que llame a [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) en el contexto inmediato para enviar la lista de comandos de contexto diferido. A continuación, la GPU procesa los datos de consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




