---
description: Control de un dispositivo externo
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Control de un dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536694"
---
# <a name="controlling-an-external-device"></a>Control de un dispositivo externo

Para controlar un dispositivo de grabadora de cintas de vídeo (VTR), use el método [**IAMExtTransport::p UT \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) . Especifique el nuevo estado mediante una de las constantes que aparecen en el [Estado de transporte del dispositivo](device-transport-state.md). Por ejemplo, para detener el dispositivo, use lo siguiente:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Dado que el VTR es un dispositivo físico, normalmente se produce un retraso entre la emisión del comando y la finalización del comando. La aplicación debe crear un segundo subproceso de trabajo que espera a que finalice el comando. Cuando el comando finaliza, el subproceso puede actualizar la interfaz de usuario. Use una sección crítica para serializar el cambio de estado.

Algunos VTRs pueden notificar a la aplicación cuando el estado de transporte del dispositivo ha cambiado. Si el dispositivo es compatible con esta característica, el subproceso de trabajo puede esperar la notificación. Sin embargo, según la "Especificación de subunidad de grabadora de cintas AV/C" de la asociación comercial de 1394, el comando de notificación de estado de transporte es opcional, lo que significa que no es necesario que los dispositivos lo admitan. Si un dispositivo no admite notificaciones, debe sondear el dispositivo a intervalos periódicos para su estado actual.

En esta sección se describe primero el mecanismo de notificación y, a continuación, se describe el sondeo del dispositivo.

Uso de la notificación de estado de transporte

La notificación de estado de transporte funciona haciendo que el controlador señale un evento cuando el transporte cambia a un nuevo estado. En la aplicación, declare una sección crítica, un evento y un identificador de subproceso. La sección crítica se usa para sincronizar el estado del dispositivo. El evento se usa para detener el subproceso de trabajo cuando se cierra la aplicación:


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



En el subproceso de trabajo, empiece por llamar al método [**IAMExtTransport:: getStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) con el valor Ed \_ Notify \_ HEVENT \_ get. Esta llamada devuelve un identificador a un evento que se señalará cuando se complete una operación:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



A continuación, vuelva a llamar a **GetState** y pase el valor de la notificación de cambio de modo de Ed \_ \_ \_ :


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Si el dispositivo admite la notificación, el método devuelve el valor E \_ pendiente. (De lo contrario, debe sondear el dispositivo, como se describe en la sección siguiente). Suponiendo que el dispositivo admite la notificación, el evento se señalará cada vez que cambie el estado del transporte del VTR. En este momento, puede actualizar la interfaz de usuario para que refleje el nuevo estado. Para obtener la notificación siguiente, restablezca el identificador de evento y **llame de nuevo a la** notificación de cambio de modo de la actualización del modo Ed \_ \_ \_ .

Antes de que se cierre el subproceso de trabajo, libere el identificador de evento llamando a **getStatus** con la marca Ed \_ Notify \_ HEVENT \_ release y la dirección del identificador:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



En el código siguiente se muestra el procedimiento de subproceso completo. Se supone que la función UpdateTransportState es una función de aplicación que actualiza la interfaz de usuario. Tenga en cuenta que el subproceso espera dos eventos: el evento de notificación (*hNotify*) y el evento de terminación del subproceso (*hThreadEnd*). Tenga en cuenta también dónde se usa la sección crítica para proteger la variable de estado del dispositivo.


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



Use también la sección crítica cuando emita comandos para el dispositivo, como se indica a continuación:


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Antes de que se cierre la aplicación, detenga el subproceso secundario estableciendo el evento de fin de subproceso:


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

Si llama a **IAMExtTransport:: getStatus** con la \_ marca de notificación de cambio de modo Ed \_ \_ y el valor devuelto no es E \_ pendiente, significa que el dispositivo no admite la notificación. En ese caso, debe sondear el dispositivo para determinar su estado. El *sondeo* simplemente significa llamar al **\_ modo Get** a intervalos regulares para comprobar el estado de transporte. Todavía debería usar un subproceso secundario y una sección crítica, como se describió anteriormente. El subproceso consulta el estado del dispositivo en un intervalo normal. En el ejemplo siguiente se muestra una manera de implementar el subproceso:


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

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



