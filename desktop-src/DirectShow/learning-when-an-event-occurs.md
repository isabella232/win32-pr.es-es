---
description: Aprendizaje cuando se produce un evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Aprendizaje cuando se produce un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537702"
---
# <a name="learning-when-an-event-occurs"></a>Aprendizaje cuando se produce un evento

Para procesar los eventos de DirectShow, una aplicación necesita una manera de averiguar cuándo esperan los eventos en la cola. El administrador de gráficos de filtro proporciona dos maneras de hacerlo:

-   **Notificación de ventana:** El administrador de gráficos de filtros envía un mensaje de Windows definido por el usuario a una ventana de la aplicación cada vez que hay un nuevo evento.
-   **Señalización de eventos:** El administrador de gráficos de filtro indica un evento de Windows si hay eventos de DirectShow en la cola y restablece el evento si la cola está vacía.

Una aplicación puede utilizar cualquiera de las técnicas. La notificación de ventana suele ser más sencilla.

**Notificación de ventana**

Para configurar la notificación de ventana, llame al método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) y especifique un mensaje privado. Las aplicaciones pueden usar números de mensaje en el intervalo de la aplicación de WM \_ a través de 0xBFFF como mensajes privados. Siempre que el administrador de gráficos de filtro coloca una nueva notificación de eventos en la cola, envía este mensaje a la ventana designada. La aplicación responde al mensaje desde dentro del bucle de mensajes de la ventana.

En el ejemplo de código siguiente se muestra cómo establecer la ventana de notificación.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



El mensaje es un mensaje de Windows normal y se publica por separado de la cola de notificación de eventos de DirectShow. La ventaja de este enfoque es que la mayoría de las aplicaciones ya implementan un bucle de mensajes. Por lo tanto, puede incorporar el control de eventos de DirectShow sin mucho trabajo adicional.

En el ejemplo de código siguiente se muestra un esquema de cómo responder al mensaje de notificación. Para obtener un ejemplo completo, vea [responder a eventos](responding-to-events.md).


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



Dado que la notificación de eventos y el bucle de mensajes son asincrónicas, la cola podría contener más de un evento en el momento en que la aplicación responde al mensaje. Además, a veces se pueden borrar los eventos de la cola si dejan de ser válidos. Por lo tanto, en el código de control de eventos, llame a [**IAMMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) hasta que devuelva un código de error, que indica que la cola está vacía.

Antes de liberar el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele la notificación de eventos llamando a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un puntero **nulo** . En el código de procesamiento de eventos, compruebe si el puntero de **IMediaEventEx** es válido antes de llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Estos pasos impiden un posible error, en el que la aplicación recibe la notificación de eventos después de haber liberado el puntero **IMediaEventEx** .

**Señalización de eventos**

El administrador de gráficos de filtro mantiene un evento de restablecimiento manual que refleja el estado de la cola de eventos. Si la cola contiene notificaciones de eventos pendientes, el administrador de gráficos de filtros indica el evento de restablecimiento manual. Si la cola está vacía, una llamada al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) restablece el evento. Una aplicación puede utilizar este evento para determinar el estado de la cola.

> [!Note]  
> La terminología puede resultar confusa aquí. El evento de restablecimiento manual es el tipo de evento creado por la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) de Windows; no tiene nada que hacer con los eventos definidos por DirectShow.

 

Llame al método [**IMediaEvent:: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) para obtener un identificador para el evento de restablecimiento manual. Espere a que se Señalice el evento llamando a una función como [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects). Una vez señalado el evento, llame a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obtener el evento de DirectShow.

En el ejemplo de código siguiente se muestra este método. Obtiene el identificador de evento y, a continuación, espera en intervalos de 100 milisegundos para que se Señalice el evento. Si el evento se señala, llama a **GetEvent** e imprime el código de evento y los parámetros de evento en la ventana de la consola. El bucle finaliza cuando se produce el evento de [**\_ finalización de EC**](ec-complete.md) , lo que indica que se ha completado la reproducción.


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



Dado que el gráfico de filtros establece o restablece automáticamente el evento cuando sea necesario, la aplicación no debería hacerlo. Además, al liberar el gráfico de filtros, el gráfico de filtros cierra el controlador de eventos, por lo que no debe usar el identificador de eventos después de ese punto.

 

 
