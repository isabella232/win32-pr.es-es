---
description: En este artículo se describe cómo responder a eventos que se producen en un gráfico de filtros.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Respuesta a eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb0325af2e216a3679d3e15a293aa6bfe1c100f2271d089e982b295df791130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050565"
---
# <a name="responding-to-events"></a>Respuesta a eventos

En este artículo se describe cómo responder a eventos que se producen en un gráfico de filtros.

## <a name="how-event-notification-works"></a>Funcionamiento de la notificación de eventos

Mientras se ejecuta DirectShow aplicación, pueden producirse eventos dentro del gráfico de filtros. Por ejemplo, un filtro podría encontrar un error de streaming. Los filtros alertan al Administrador de Graph mediante el envío de eventos, que constan de un código de evento y dos parámetros de evento. El código de evento indica el tipo de evento y los parámetros de evento suministran información adicional. El significado de los parámetros depende del código de evento. Para obtener una lista completa de códigos de evento, vea [Códigos de notificación de eventos](event-notification-codes.md).

Algunos eventos se controlan de forma silenciosa mediante el Administrador de Graph, sin que se notifique a la aplicación. Otros eventos se colocan en una cola para la aplicación. En función de la aplicación, hay varios eventos que es posible que tenga que controlar. Este artículo se centra en tres eventos que son muy comunes:

-   El [**evento \_ EC COMPLETE**](ec-complete.md) indica que la reproducción se ha completado con normalidad.
-   El [**evento \_ USERABORT de EC**](ec-userabort.md) indica que el usuario ha interrumpido la reproducción. Los representadores de vídeo envían este evento si el usuario cierra la ventana de vídeo.
-   El [**evento \_ EC ERRORABORT**](ec-errorabort.md) indica que un error ha provocado la detención de la reproducción.

## <a name="using-event-notification"></a>Uso de la notificación de eventos

Una aplicación puede indicar al Administrador de Graph que envíe un mensaje Windows a una ventana designada cada vez que se produzca un nuevo evento. Esto permite que la aplicación responda dentro del bucle de mensajes de la ventana. En primer lugar, defina el mensaje que se enviará a la ventana de la aplicación. Las aplicaciones pueden usar números de mensaje en el intervalo desde WM \_ APP hasta 0xBFFF como mensajes privados:


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



A continuación, consulte filter Graph Manager para la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) y llame al [**método IMediaEventEx::SetNotifyWindow:**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Este método designa la ventana especificada (g \_ hwnd) como destinatario del mensaje. Llame al método después de crear el gráfico de filtro, pero antes de ejecutar el gráfico.

WM \_ GRAPHNOTIFY es un mensaje Windows normal. Cada vez que el Administrador Graph coloca un nuevo evento en la cola de eventos, envía un mensaje GRAPHNOTIFY de WM a la \_ ventana de aplicación designada. El parámetro *lParam del* mensaje es igual al tercer parámetro de [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Este parámetro le permite enviar datos de instancia con el mensaje. El parámetro *wParam* del mensaje de ventana siempre es cero.

En la función **WindowProc** de la aplicación, agregue una instrucción case para el mensaje \_ GRAPHNOTIFY de WM:


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



En la función de controlador de eventos, llame [**al método IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para recuperar eventos de la cola:


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



El [**método GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) recupera el código de evento y los dos parámetros de evento. El cuarto **parámetro GetEvent** especifica el tiempo de espera de un evento, en milisegundos. Dado que la aplicación llama a este método en respuesta a un mensaje DE WM \_ GRAPHNOTIFY, el evento ya está en cola. Por lo tanto, establecemos el valor de tiempo de espera en cero.

La notificación de eventos y el bucle de mensajes son asincrónicos, por lo que la cola podría contener más de un evento en el momento en que la aplicación responde al mensaje. Además, el Administrador de Graph puede quitar determinados eventos de la cola, si no son válidos. Por lo tanto, debe llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) hasta que devuelva un código de error, lo que indica que la cola está vacía.

En este ejemplo, la aplicación responde a [**EC \_ COMPLETE,**](ec-complete.md)EC USERABORT y [**EC \_ ERRORABORT**](ec-errorabort.md) invocando la función CleanUp definida por la aplicación, lo que hace que la aplicación se cierre correctamente. [**\_**](ec-userabort.md) En el ejemplo se omiten los dos parámetros de evento. Después de recuperar un evento, llame a [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) en los recursos gratuitos asociados a los parámetros del evento.

Tenga en cuenta que [**un evento \_ EC COMPLETE**](ec-complete.md) no hace que el gráfico de filtro se detenga. La aplicación puede detener o pausar el gráfico. Si detiene el gráfico, los filtros liberan los recursos que están manteniendo. Si pausa el gráfico, los filtros seguirán reteniendo los recursos. Además, cuando un representador de vídeo se detiene, muestra una imagen estática del fotograma más reciente.

Antes de liberar el [**puntero IMediaEventEx,**](/windows/desktop/api/Control/nn-control-imediaeventex) cancele la notificación de eventos mediante una llamada a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un **identificador de ventana** NULL:


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



En el controlador \_ de mensajes WM GRAPHNOTIFY, compruebe el [**puntero IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) antes de llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):


```C++
if (g_pEvent == NULL) return;
```



Esto evita un posible error que puede producirse si la aplicación recibe la notificación de eventos después de liberar el puntero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas DirectShow básicas](basic-directshow-tasks.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



