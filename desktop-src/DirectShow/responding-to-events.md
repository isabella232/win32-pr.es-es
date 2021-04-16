---
description: En este artículo se describe cómo responder a los eventos que se producen en un gráfico de filtro.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Respuesta a eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537203"
---
# <a name="responding-to-events"></a>Respuesta a eventos

En este artículo se describe cómo responder a los eventos que se producen en un gráfico de filtro.

## <a name="how-event-notification-works"></a>Cómo funciona la notificación de eventos

Mientras se ejecuta una aplicación de DirectShow, se pueden producir eventos dentro del gráfico de filtros. Por ejemplo, un filtro podría encontrar un error de streaming. Los filtros alertan al administrador de gráficos de filtro mediante el envío de eventos, que constan de un código de evento y dos parámetros de evento. El código de evento indica el tipo de evento y los parámetros de evento proporcionan información adicional. El significado de los parámetros depende del código de evento. Para obtener una lista completa de los códigos de evento, consulte [códigos de notificación de eventos](event-notification-codes.md).

Algunos eventos se controlan de forma silenciosa por el administrador de gráficos de filtro, sin que se notifique a la aplicación. Otros eventos se colocan en una cola para la aplicación. Dependiendo de la aplicación, hay varios eventos que es posible que deba controlar. Este artículo se centra en tres eventos que son muy comunes:

-   El evento de [**\_ finalización de EC**](ec-complete.md) indica que la reproducción se ha completado con normalidad.
-   El [**evento \_ USERABORT de EC**](ec-userabort.md) indica que el usuario ha interrumpido la reproducción. Los representadores de vídeo envían este evento si el usuario cierra la ventana de vídeo.
-   El [**evento \_ ERRORABORT de EC**](ec-errorabort.md) indica que un error ha provocado que se detenga la reproducción.

## <a name="using-event-notification"></a>Usar la notificación de eventos

Una aplicación puede indicar al administrador de gráficos de filtro que envíe un mensaje de Windows a una ventana designada cada vez que se produzca un nuevo evento. Esto permite que la aplicación responda dentro del bucle de mensajes de la ventana. En primer lugar, defina el mensaje que se enviará a la ventana de la aplicación. Las aplicaciones pueden usar números de mensaje en el intervalo de la aplicación de WM \_ a través de 0xBFFF como mensajes privados:


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



A continuación, consulte el administrador de gráficos de filtro para la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) y llame al método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Este método designa la ventana especificada (g \_ hWnd) como destinatario del mensaje. Llame al método después de crear el gráfico de filtros, pero antes de ejecutar el gráfico.

WM \_ GRAPHNOTIFY es un mensaje de Windows normal. Siempre que el administrador de gráficos de filtro coloca un nuevo evento en la cola de eventos, envía un mensaje de WM \_ GRAPHNOTIFY a la ventana de la aplicación designada. El parámetro *lParam* del mensaje es igual que el tercer parámetro de [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Este parámetro permite enviar datos de instancia con el mensaje. El parámetro *wParam* del mensaje de ventana siempre es cero.

En la función **WindowProc** de la aplicación, agregue una instrucción Case para el \_ mensaje de GRAPHNOTIFY de WM:


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



En la función de controlador de eventos, llame al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para recuperar los eventos de la cola:


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



El método [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) recupera el código de evento y los dos parámetros de evento. El cuarto parámetro **GetEvent** especifica la cantidad de tiempo de espera para un evento, en milisegundos. Dado que la aplicación llama a este método en respuesta a un mensaje de GRAPHNOTIFY de WM \_ , el evento ya está en cola. Por lo tanto, el valor de tiempo de espera se establece en cero.

La notificación de eventos y el bucle de mensajes son asincrónicas, por lo que la cola podría contener más de un evento en el momento en que la aplicación responde al mensaje. Además, el administrador de gráficos de filtro puede quitar determinados eventos de la cola, si no son válidos. Por lo tanto, debe llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) hasta que devuelva un código de error, lo que indica que la cola está vacía.

En este ejemplo, la aplicación responde a [**EC \_ Complete**](ec-complete.md), [**EC \_ USERABORT**](ec-userabort.md)y [**EC \_ ERRORABORT**](ec-errorabort.md) mediante la invocación de la función de limpieza definida por la aplicación, que hace que la aplicación se cierre correctamente. En el ejemplo se omiten los dos parámetros de evento. Después de recuperar un evento, llame a [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) a todos los recursos libres asociados a los parámetros de evento.

Tenga en cuenta que un evento de [**\_ finalización de EC**](ec-complete.md) no hace que el gráfico de filtros se detenga. La aplicación puede detener o pausar el gráfico. Si detiene el gráfico, los filtros liberan los recursos que contienen. Si pausa el gráfico, los filtros continúan manteniendo los recursos. Además, cuando una pausa en el representador de vídeo, muestra una imagen estática del fotograma más reciente.

Antes de liberar el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele la notificación de eventos llamando a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un identificador de ventana **nulo** :


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



En el controlador de mensajes de WM \_ GRAPHNOTIFY, compruebe el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) antes de llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):


```C++
if (g_pEvent == NULL) return;
```



Esto evita un posible error que se puede producir si la aplicación recibe la notificación de eventos después de liberar el puntero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas básicas de DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



