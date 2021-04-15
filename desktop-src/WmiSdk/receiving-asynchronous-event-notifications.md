---
description: La notificación de eventos asincrónicos es una técnica que permite a una aplicación supervisar constantemente eventos sin monopolizar los recursos del sistema.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Recibir notificaciones de eventos asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648498"
---
# <a name="receiving-asynchronous-event-notifications"></a>Recibir notificaciones de eventos asincrónicas

La notificación de eventos asincrónicos es una técnica que permite a una aplicación supervisar constantemente eventos sin monopolizar los recursos del sistema. Las notificaciones de eventos asincrónicos tienen las mismas limitaciones de seguridad que otras llamadas asincrónicas. En su lugar, puede realizar llamadas semisincrónicas. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

La cola de eventos asincrónicos enrutados a un cliente tiene la posibilidad de crecer excepcionalmente grande. Por lo tanto, WMI implementa una directiva de todo el sistema para evitar quedarse sin memoria. WMI ralentiza eventos o comienza a quitar eventos de la cola cuando la cola crece más allá de un tamaño determinado.

WMI utiliza las propiedades [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) y [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) de la clase [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para establecer límites en la prevención de memoria insuficiente. El valor mínimo indica cuándo WMI debería empezar a ralentizar la notificación de eventos y el valor máximo indica cuándo se debe iniciar la eliminación de eventos. Los valores predeterminados para los umbrales inferior y superior son 1 millón (10 MB) y 2 millones (20 MB). Además, puede establecer la propiedad [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para describir la cantidad de tiempo que WMI debe esperar antes de quitar los eventos. El valor predeterminado de **MaxWaitOnEvents** es 2000 o 2 segundos.

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a>Recibir notificaciones de eventos asincrónicas en VBScript

Las llamadas de scripting para recibir notificaciones de eventos son esencialmente las mismas que todas las llamadas asincrónicas con los mismos problemas de seguridad. Para obtener más información, vea [crear una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md).

**Para recibir notificaciones de eventos asincrónicos en VBScript**

1.  Cree un objeto de receptor llamando a [Wscript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) y especificando el ProgID de "WbemScripting" y el tipo de objeto de [**SWbemSink**](swbemsink.md). El objeto receptor recibe las notificaciones.
2.  Escriba una subrutina para cada evento que desee controlar. En la tabla siguiente se enumeran los eventos de [**SWbemSink**](swbemsink.md) .

    

    | Evento                                            | Significado                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [**OnObjectReady**](swbemsink-onobjectready.md) | Notifica las devoluciones de un objeto al receptor. El uso de esta llamada devuelve un objeto cada vez hasta que se completa la operación.     |
    | [**OnCompleted**](swbemsink-oncompleted.md)     | Informa cuando se completa una llamada asincrónica. Este evento nunca se produce si la operación es indefinida.                          |
    | [**OnObjectPut**](swbemsink-onobjectput.md)     | Informa de la finalización de una operación PUT asincrónica. Este evento devuelve la ruta de acceso del objeto de la instancia o la clase guardada. |
    | [**OnProgress**](swbemsink-onprogress.md)       | Informa del estado de una llamada asincrónica que está en curso. No todos los proveedores admiten informes de progreso provisional.             |
    | [**Cancelar**](swbemsink-cancel.md)               | Cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.                                        |

    

     

En el siguiente ejemplo de código de VBScript se notifica la eliminación de procesos con un intervalo de sondeo de 10 segundos. En este script, el receptor de subrutinas \_ OnObjectReady controla la repetición del evento. En el ejemplo, el objeto receptor se denomina "Sink"; sin embargo, puede asignar un nombre a este objeto como elija.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a>Recibir notificaciones de eventos asincrónicas en C++

Para realizar una notificación asincrónica, se crea un subproceso independiente únicamente para supervisar y recibir eventos de Instrumental de administración de Windows (WMI). Cuando ese subproceso recibe un mensaje, el subproceso notifica a la aplicación principal.

Al dedicar un subproceso independiente, permite que el proceso principal realice otras actividades mientras espera que llegue un evento. La entrega asincrónica de notificaciones mejora el rendimiento, pero puede proporcionar menos seguridad de lo que se desee. En C++, tiene la opción de usar la interfaz [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) o realizar comprobaciones de acceso en descriptores de seguridad. Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

**Para configurar notificaciones de eventos asincrónicos**

1.  Antes de inicializar las notificaciones asincrónicas, asegúrese de que los parámetros de prevención de memoria insuficiente están configurados correctamente en [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).

2.  Determine qué tipo de eventos desea recibir.

    WMI admite eventos intrínsecos y extrínsecos. Un evento intrínseco es un evento predefinido por WMI, mientras que un evento extrínseco es un evento definido por un proveedor de terceros. Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).

En el procedimiento siguiente se describe cómo recibir notificaciones de eventos asincrónicas en C++.

**Para recibir notificaciones de eventos asincrónicos en C++**

1.  Configure la aplicación con llamadas a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    La llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) inicializa com, mientras que [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) concede a WMI el permiso para llamar al proceso del consumidor. La función **CoInitializeEx** también le concede la capacidad de programar una aplicación multiproceso, que es necesaria para la notificación asincrónica. Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).

    El código de este tema requiere las siguientes referencias e \# incluir instrucciones para compilar correctamente.

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    En el ejemplo de código siguiente se describe cómo configurar el consumidor de eventos temporal con llamadas a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  Cree un objeto de receptor a través de la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .

    WMI usa [**IWbemObjectSink**](iwbemobjectsink.md) para enviar notificaciones de eventos y para notificar el estado de una operación asincrónica o una notificación de eventos.

3.  Registre el consumidor de eventos con una llamada al método [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .

    Asegúrese de que el parámetro *pResponseHandler* apunta al objeto receptor creado en el paso anterior.

    El propósito del registro es recibir solo las notificaciones necesarias. Recibir notificaciones superfluas desperdicia el procesamiento y el tiempo de entrega; y no utiliza la capacidad de filtrado de WMI para obtener el máximo potencial.

    Sin embargo, un consumidor temporal puede recibir más de un tipo de evento. En este caso, un consumidor temporal debe realizar llamadas independientes a [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) para cada tipo de evento. Por ejemplo, un consumidor podría requerir una notificación cuando se creen nuevos procesos (un evento de creación de instancia o [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) y para los cambios en ciertas claves del registro (un evento del registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)). Por consiguiente, el consumidor realiza una llamada a [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) para registrar los eventos de creación de instancia y otra llamada a **ExecNotificationQueryAsync** para registrar los eventos del registro.

    Si decide crear un consumidor de eventos que se registre para varios eventos, debe evitar el registro de varias clases con el mismo receptor. En su lugar, utilice un receptor independiente para cada clase de evento registrado. Tener un receptor dedicado simplifica el procesamiento y la ayuda en el mantenimiento, lo que le permite cancelar un registro sin que afecte a los demás.

4.  Realice las actividades necesarias en el consumidor de eventos.

    Este paso debe contener la mayor parte del código e incluir actividades como la visualización de eventos en una interfaz de usuario.

5.  Cuando termine, anule el registro del consumidor de eventos temporal con una llamada al evento [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    Independientemente de si la llamada a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) se realiza correctamente o se produce un error, no elimine el objeto de receptor hasta que el recuento de referencias de objeto llegue a cero. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

 
