---
description: Controlar un dispositivo externo
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Controlar un dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161572"
---
# <a name="controlling-an-external-device"></a>Controlar un dispositivo externo

Para controlar un dispositivo de grabadora de cinta de vídeo (VTR), use el [**método IAMExtTransport::p ut \_ Mode.**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) Especifique el nuevo estado mediante una de las constantes enumeradas en [Estado de transporte de dispositivos](device-transport-state.md). Por ejemplo, para detener el dispositivo, use lo siguiente:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Dado que VTR es un dispositivo físico, normalmente hay un retraso entre la emisión del comando y el momento en que se completa el comando. La aplicación debe crear un segundo subproceso de trabajo que espere a que finalice el comando. Cuando finaliza el comando, el subproceso puede actualizar la interfaz de usuario. Use una sección crítica para serializar el cambio de estado.

Algunas VTR pueden notificar a la aplicación cuándo ha cambiado el estado de transporte del dispositivo. Si el dispositivo admite esta característica, el subproceso de trabajo puede esperar la notificación. Según la especificación de la subunidad av/C tape recorder/player de la asociación comercial 1394, el comando de notificación de estado de transporte es opcional, lo que significa que los dispositivos no son necesarios para admitirlo. Si un dispositivo no admite notificaciones, debe sondear el dispositivo a intervalos periódicos para su estado actual.

En esta sección se describe primero el mecanismo de notificación y, a continuación, se describe el sondeo de dispositivos.

Uso de la notificación de estado de transporte

La notificación de estado de transporte funciona haciendo que el controlador señale un evento cuando el transporte cambia a un estado nuevo. En la aplicación, declare una sección crítica, un evento y un identificador de subproceso. La sección crítica se usa para sincronizar el estado del dispositivo. El evento se usa para detener el subproceso de trabajo cuando se cierra la aplicación:


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



Después de crear una instancia del filtro de captura, cree el subproceso de trabajo:


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



En el subproceso de trabajo, empiece por llamar al [**método IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) con el valor ED \_ NOTIFY \_ HESTATUS \_ GET. Esta llamada devuelve un identificador a un evento que se señalará cuando se complete una operación:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



A continuación, vuelva a llamar a **GetState** y pase el valor ED \_ MODE CHANGE \_ \_ NOTIFY:


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Si el dispositivo admite notificaciones, el método devuelve el valor E \_ PENDING. (De lo contrario, debe sondear el dispositivo, como se describe en la sección siguiente). Suponiendo que el dispositivo admita la notificación, el evento se señalará cada vez que cambie el estado del transporte de VTR. En este momento, puede actualizar la interfaz de usuario para reflejar el nuevo estado. Para obtener la siguiente notificación, restablezca el identificador de eventos y vuelva a llamar a **GetStatus** con ED \_ MODE CHANGE \_ \_ NOTIFY.

Antes de que se cierre el subproceso de trabajo, libere el identificador de eventos mediante una llamada a **GetStatus** con la marca ED NOTIFY HESTATUS RELEASE y \_ la dirección del \_ \_ identificador:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



El código siguiente muestra el procedimiento de subproceso completo. Se supone que la función UpdateTransportState es una función de aplicación que actualiza la interfaz de usuario. Tenga en cuenta que el subproceso espera dos eventos: el evento de notificación (*hNotify*) y el evento de terminación del subproceso (*hThreadEnd*). Tenga en cuenta también dónde se usa la sección crítica para proteger la variable de estado del dispositivo.


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



Use también la sección crítica cuando emita comandos al dispositivo, como se muestra a continuación:


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Antes de que se cierre la aplicación, detenga el subproceso secundario estableciendo el evento thread-end:


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



Sondear el estado de transporte

Si llama a **IAMExtTransport::GetStatus** con la marca ED MODE CHANGE NOTIFY y el valor devuelto no es E PENDING, significa que el dispositivo no \_ admite la \_ \_ \_ notificación. En ese caso, debe sondear el dispositivo para determinar su estado. *Sondear* simplemente significa llamar **al \_ modo get** a intervalos regulares para comprobar el estado de transporte. Debe seguir utilizando un subproceso secundario y una sección crítica, como se describió anteriormente. El subproceso consulta el estado del dispositivo en un intervalo regular. En el ejemplo siguiente se muestra una manera de implementar el subproceso:


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una cámara dv](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



