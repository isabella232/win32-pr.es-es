---
description: Control de eventos de repintado en la captura de vídeo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Control de eventos de repintado en la captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169945"
---
# <a name="handling-repaint-events-in-video-capture"></a>Control de eventos de repintado en la captura de vídeo

Si crea un gráfico de captura de vídeo sin usar la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) y muestra una vista previa del vídeo mediante el filtro De representador de vídeo anterior, debe invalidar el control predeterminado para los eventos [**\_ EC REPAINT.**](ec-repaint.md) Consulte el Administrador de Graph filtros para la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) y llame al método [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con el valor EC \_ REPAINT:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Esto evita un posible error que puede dañar el archivo de captura. Si el usuario cubre y descubre la ventana de vista previa, el filtro Representador de vídeo recibe un mensaje WM \_ PAINT. De forma predeterminada, el representador de vídeo solicita un nuevo fotograma y el Administrador de filtros Graph pausa el gráfico para que señale otro fotograma de vídeo. Si esto sucede mientras el gráfico escribe un archivo, el archivo se dañará. La invalidación del comportamiento predeterminado de EC REPAINT impide que el representador \_ solicite un fotograma nuevo.

No tiene que realizar este paso si usa la interfaz **ICaptureGraphBuilder2,** ya que Capture Graph Builder lo hace automáticamente. Además, no es necesario si usa el representador de mezcla de vídeo (VMR) para la versión preliminar. VmR siempre tiene disponible el fotograma más reciente, por lo que no envía eventos \_ EC REPAINT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



