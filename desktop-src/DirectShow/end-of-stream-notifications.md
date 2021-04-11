---
description: Notificaciones de final de secuencia
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: Notificaciones de final de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fcdfef1225aa5b93b56aeaa0d8ae9d0a8550c9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274778"
---
# <a name="end-of-stream-notifications"></a>Notificaciones de final de secuencia

Cuando un filtro de origen ha terminado de enviar datos, llama al método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada de nivel inferior. El filtro de nivel inferior propaga la llamada al filtro siguiente, y así sucesivamente. Cuando la llamada a **EndOfStream** llega al representador, el representador envía un evento [**EC \_ Complete**](ec-complete.md) al administrador de gráficos de filtro. Si el representador tiene varios PIN de entrada, entrega el \_ evento de finalización de EC una vez que cada pin de entrada ha recibido la notificación de fin de secuencia.

Un filtro debe serializar las llamadas a [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) con otras llamadas de streaming, como [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive). (Es decir, el filtro de nivel inferior debe recibir siempre las llamadas en el orden correcto).

En algunos casos, un filtro de nivel inferior podría detectar el final de la secuencia antes que el filtro de origen. (Por ejemplo, el filtro de nivel inferior podría estar analizando la secuencia). En ese caso, el filtro de nivel inferior puede enviar la notificación de final de secuencia, en cuyo caso debe devolver S \_ false desde [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) hasta que el gráfico se detenga o se vacíe. El \_ valor devuelto de S false informa al filtro de origen para que deje de enviar datos.

### <a name="default-handling-of-ec_complete"></a>Control predeterminado de EC \_ completado

De forma predeterminada, el administrador de gráficos de filtro no reenvía \_ a la aplicación todos los eventos de finalización de EC. En su lugar, espera hasta que todas las secuencias hayan \_ concluido la EC y, a continuación, envíe un solo \_ evento de finalización de EC. Por lo tanto, la aplicación recibe el evento después de que se haya completado cada flujo.

Para determinar el número de secuencias, el administrador de gráficos de filtro cuenta el número de filtros que admiten la búsqueda (a través de [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)) y tienen un PIN de entrada *representado* , que se define como un PIN de entrada sin salidas correspondientes. El administrador de gráficos de filtro determina si un PIN se representa de una de las dos maneras siguientes:

-   El método [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) del PIN devuelve cero en el parámetro *nPin* .
-   El filtro expone la interfaz [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) y devuelve la marca AM \_ Filter \_ Misc \_ Flags \_ is \_ representator.

### <a name="end-of-stream-notifications-in-pull-mode"></a>Notificaciones de final de secuencia en el modo de extracción

En una conexión [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) , el filtro de origen no envía una notificación de final de secuencia. Instread, esto se realiza mediante el filtro de nivel inferior, que suele ser un filtro de analizador. El analizador envía la llamada [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) downstream. No envía un flujo ascendente al filtro de origen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entrega del final de la secuencia](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



