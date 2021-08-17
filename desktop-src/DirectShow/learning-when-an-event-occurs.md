---
description: Learning Cuando se produce un evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Learning Cuando se produce un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58696055bdf1e3cbf3cf36c4db4ae2258bda334956fcaa14f33eda96db249773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397221"
---
# <a name="learning-when-an-event-occurs"></a>Learning Cuando se produce un evento

Para procesar DirectShow eventos, una aplicación necesita una manera de averiguar cuándo los eventos están esperando en la cola. El Administrador Graph filtros proporciona dos maneras de hacerlo:

-   **Notificación de ventana:** El Administrador Graph filtros envía un mensaje de Windows definido por el usuario a una ventana de aplicación cada vez que hay un nuevo evento.
-   **Señalización de eventos:** Filter Graph Manager indica un evento Windows si hay eventos DirectShow en la cola y restablece el evento si la cola está vacía.

Una aplicación puede usar cualquiera de estas técnicas. La notificación de ventana suele ser más sencilla.

**Notificación de ventana**

Para configurar la notificación de ventana, llame al [**método IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) y especifique un mensaje privado. Las aplicaciones pueden usar números de mensaje en el intervalo desde WM \_ APP hasta 0xBFFF como mensajes privados. Cada vez que el administrador Graph coloca una nueva notificación de eventos en la cola, envía este mensaje a la ventana designada. La aplicación responde al mensaje desde dentro del bucle de mensajes de la ventana.

En el ejemplo de código siguiente se muestra cómo establecer la ventana de notificación.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



El mensaje es un mensaje Windows y se publica por separado de la cola DirectShow de notificaciones de eventos. La ventaja de este enfoque es que la mayoría de las aplicaciones ya implementan un bucle de mensajes. Por lo tanto, puede incorporar DirectShow control de eventos sin mucho trabajo adicional.

En el ejemplo de código siguiente se muestra un esquema de cómo responder al mensaje de notificación. Para obtener un ejemplo completo, vea [Responder a eventos](responding-to-events.md).


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



Dado que la notificación de eventos y el bucle de mensajes son asincrónicos, la cola puede contener más de un evento en el momento en que la aplicación responde al mensaje. Además, los eventos a veces se pueden borrar de la cola si no son válidos. Por lo tanto, en el código de control de eventos, llame a [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) hasta que devuelva un código de error, lo que indica que la cola está vacía.

Antes de liberar el [**puntero IMediaEventEx,**](/windows/desktop/api/Control/nn-control-imediaeventex) cancele la notificación de eventos mediante una llamada a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un **puntero NULL.** En el código de procesamiento de eventos, compruebe si el **puntero IMediaEventEx** es válido antes de llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Estos pasos evitan un posible error, en el que la aplicación recibe la notificación de eventos después de que haya publicado el **puntero IMediaEventEx.**

**Señalización de eventos**

Filter Graph Manager mantiene un evento de restablecimiento manual que refleja el estado de la cola de eventos. Si la cola contiene notificaciones de eventos pendientes, filter Graph Manager indica el evento de restablecimiento manual. Si la cola está vacía, una llamada al método [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) restablece el evento. Una aplicación puede usar este evento para determinar el estado de la cola.

> [!Note]  
> La terminología puede resultar confusa aquí. El evento de restablecimiento manual es el tipo de evento creado por la Windows [**función CreateEvent;**](/windows/win32/api/synchapi/nf-synchapi-createeventa) no tiene nada que ver con los eventos definidos por DirectShow.

 

Llame al [**método IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) para obtener un identificador para el evento de restablecimiento manual. Espere a que se señale el evento mediante una llamada a una función como [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects). Una vez que se señala el evento, llame [**a IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obtener el DirectShow evento.

En el ejemplo de código siguiente se muestra este método. Obtiene el identificador del evento y, a continuación, espera en intervalos de 100 milisegundos a que se señale el evento. Si se señala el evento, llama a **GetEvent** e imprime el código de evento y los parámetros de evento en la ventana de consola. El bucle finaliza cuando se produce el evento [**\_ EC COMPLETE,**](ec-complete.md) lo que indica que se ha completado la reproducción.


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



Dado que el gráfico de filtros establece o restablece automáticamente el evento cuando sea necesario, la aplicación no debe hacerlo. Además, al liberar el gráfico de filtro, el gráfico de filtros cierra el identificador de eventos, por lo que no use el identificador de eventos después de ese punto.

 

 
