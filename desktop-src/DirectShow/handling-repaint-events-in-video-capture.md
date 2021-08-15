---
description: Control de eventos de repintado en la captura de vídeo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Control de eventos de repintado en la captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433a9897c7c69119eb54d088aff2d22536e20ae43760cc6b4c9430f9a44f6814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999764"
---
# <a name="handling-repaint-events-in-video-capture"></a>Control de eventos de repintado en la captura de vídeo

Si crea un gráfico de captura de vídeo sin usar la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) y muestra una vista previa del vídeo mediante el filtro Video Renderer anterior, debe invalidar el control predeterminado para los eventos [**\_ EC REPAINT.**](ec-repaint.md) Consulte el Administrador de Graph filtro para la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) y llame al método [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con el valor EC \_ REPAINT:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Esto evita un posible error que puede dañar el archivo de captura. Si el usuario cubre y descubre la ventana de vista previa, el filtro Representador de vídeo recibe un mensaje \_ WM PAINT. De forma predeterminada, el representador de vídeo solicita un nuevo fotograma y el Administrador de filtros Graph pausa el gráfico para que se señale otro fotograma de vídeo. Si esto sucede mientras el gráfico escribe un archivo, el archivo se dañará. Invalidar el comportamiento predeterminado de EC REPAINT impide que el representador \_ solicite un nuevo fotograma.

No es necesario realizar este paso si usa la interfaz **ICaptureGraphBuilder2,** ya que Capture Graph Builder lo hace automáticamente. Además, no es necesario si usa el representador de mezcla de vídeo (VMR) para la versión preliminar. VmR siempre tiene disponible el fotograma más reciente, por lo que no envía eventos \_ EC REPAINT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



