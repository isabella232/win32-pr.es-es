---
description: Notificaciones de fin de flujo
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: Notificaciones de fin de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fcdfef1225aa5b93b56aeaa0d8ae9d0a8550c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169993"
---
# <a name="end-of-stream-notifications"></a>Notificaciones de fin de flujo

Cuando un filtro de origen termina de enviar datos, llama al método [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el pin de entrada de bajada. El filtro de bajada propaga la llamada al siguiente filtro, y así sucesivamente. Cuando la **llamada a EndOfStream** llega al representador, el representador envía un evento [**EC \_ COMPLETE**](ec-complete.md) al Administrador de Graph Filtros. Si el representador tiene varios pines de entrada, entrega el evento EC COMPLETE después de que cada pin de entrada haya recibido la notificación de fin \_ de flujo.

Un filtro debe serializar [**las llamadas EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) con otras llamadas de streaming, como [**IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) (En otras palabras, el filtro de nivel inferior siempre debe recibir las llamadas en el orden correcto).

En algunos casos, un filtro de nivel inferior podría detectar el final de la secuencia antes de que lo haga el filtro de origen. (Por ejemplo, el filtro de nivel inferior podría estar analizando la secuencia). En ese caso, el filtro de bajada puede enviar la notificación de fin de flujo, en cuyo caso debe devolver S FALSE desde \_ [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) hasta que el gráfico se detenga o se vacíe. El valor \_ devuelto S FALSE informa al filtro de origen para que deje de enviar datos.

### <a name="default-handling-of-ec_complete"></a>Control predeterminado de EC \_ COMPLETE

De forma predeterminada, filter Graph Manager no reenvía todos los eventos EC \_ COMPLETE a la aplicación. En su lugar, espera hasta que todas las secuencias han señalado EC COMPLETE y, \_ a continuación, envía un único evento EC \_ COMPLETE. Por lo tanto, la aplicación recibe el evento después de que se haya completado cada secuencia.

Para determinar el número de secuencias, el Administrador de filtros Graph cuenta el número de filtros que admiten búsquedas (a través de [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition)**](/windows/desktop/api/Control/nn-control-imediaposition)y tiene un pin de entrada representado, que se define como un pin de entrada sin salidas correspondientes.  El Administrador Graph filtros determina si un pin se representa de una de estas dos maneras:

-   El método [**IPin::QueryInternalConnections del**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) pin devuelve cero en el *parámetro nPin.*
-   El filtro expone la interfaz [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) y devuelve la marca AM \_ FILTER \_ MISC \_ FLAGS \_ IS \_ RENDERER.

### <a name="end-of-stream-notifications-in-pull-mode"></a>Notificaciones de fin de flujo en modo de extracción

En una [**conexión IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) el filtro de origen no envía una notificación de fin de flujo. Lo hace el filtro de nivel inferior, que suele ser un filtro de analizador. El analizador envía la llamada [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) de bajada. No envía una dirección ascendente al filtro de origen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entrega del final de la secuencia](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



