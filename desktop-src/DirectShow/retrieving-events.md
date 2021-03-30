---
description: Recuperar eventos
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Recuperar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422736"
---
# <a name="retrieving-events"></a>Recuperar eventos

El administrador de gráficos de filtro expone tres interfaces que admiten la notificación de eventos.

-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contiene el método para los filtros para publicar eventos.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contiene métodos para que las aplicaciones recuperen eventos.
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) hereda de y extiende la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .

Los filtros envían notificaciones de eventos mediante una llamada al método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) en el administrador de gráficos de filtro. Una notificación de eventos consta de un código de evento, que define el tipo de evento y dos parámetros que proporcionan información adicional. Dependiendo del código de evento, los parámetros pueden contener punteros, códigos de retorno, tiempos de referencia u otra información. Para obtener una lista completa de los códigos de evento y los parámetros, vea [códigos de notificación de eventos](event-notification-codes.md).

Para recuperar un evento de la cola, la aplicación llama al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) en el administrador de gráficos de filtro. Este método se bloquea hasta que hay un evento que se va a devolver o hasta que transcurre un tiempo especificado. Suponiendo que haya un evento en cola, el método devuelve con el código de evento y los dos parámetros de evento. Después de llamar a **GetEvent**, una aplicación siempre debe llamar al método [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar los recursos asociados a los parámetros de evento. Por ejemplo, un parámetro puede ser un valor **BSTR** asignado por el gráfico de filtros.

En el ejemplo de código siguiente se proporciona un esquema de cómo recuperar eventos de la cola.


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



Para invalidar el control predeterminado del administrador de gráficos de filtro para un evento, llame al método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con el código de evento como parámetro. Puede restablecer el control predeterminado llamando al método [**IMediaEvent:: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) . Si el gráfico de filtros no realiza ningún control predeterminado para el código de evento especificado, la llamada a estos métodos no tiene ningún efecto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



