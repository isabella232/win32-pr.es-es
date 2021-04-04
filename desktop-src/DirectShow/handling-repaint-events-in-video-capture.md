---
description: Control de eventos Repaint en la captura de vídeo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Control de eventos Repaint en la captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997990"
---
# <a name="handling-repaint-events-in-video-capture"></a>Control de eventos Repaint en la captura de vídeo

Si crea un gráfico de captura de vídeo sin usar la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) y obtiene una vista previa del vídeo con el filtro de representador de vídeo anterior, debe invalidar el control predeterminado de los eventos de [**\_ Repaint de EC**](ec-repaint.md) . Consulte el administrador de gráficos de filtro para la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) y llame al método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con el valor EC \_ Repaint:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Esto evita un posible error que puede dañar el archivo de captura. Si el usuario cubre y detecta la ventana de vista previa, el filtro de representador de vídeo recibe un mensaje de dibujo de WM \_ . De forma predeterminada, el representador de vídeo solicita un nuevo fotograma y Filter Graph Manager pausa el gráfico para señalar otro fotograma de vídeo. Si esto sucede mientras el gráfico está escribiendo un archivo, se dañará el archivo. Invalidar el comportamiento predeterminado de \_ REpaint de EC evita que el representador solicite un nuevo marco.

No es necesario que realice este paso si está utilizando la interfaz **ICaptureGraphBuilder2** , porque el generador de gráficos de captura lo hace automáticamente. Además, no es necesario si usa el representador de mezcla de vídeo (VMR) para la versión preliminar. La VMR siempre tiene el fotograma más reciente disponible, por lo que no envía \_ eventos de Repaint de EC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



