---
description: La notificación asincrónica de eventos es una técnica que permite a una aplicación supervisar constantemente los eventos sin tener que tener que controlar los recursos del sistema.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Recepción de notificaciones de eventos asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c84f6c441fc5c468b0ce7d39477d52911c6ae3becb1c4c15b5130ffb041040c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130897"
---
# <a name="receiving-asynchronous-event-notifications"></a>Recepción de notificaciones de eventos asincrónicas

La notificación asincrónica de eventos es una técnica que permite a una aplicación supervisar constantemente los eventos sin tener que tener que controlar los recursos del sistema. Las notificaciones de eventos asincrónicos tienen las mismas limitaciones de seguridad que otras llamadas asincrónicas. En su lugar, puede realizar llamadas semisincronosas. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

La cola de eventos asincrónicos enrutados a un cliente tiene el potencial de crecer excepcionalmente. Por lo tanto, WMI implementa una directiva para todo el sistema para evitar que se quedándose sin memoria. WMI ralentiza los eventos o empieza a quitar eventos de la cola cuando la cola crece más allá de un tamaño determinado.

WMI usa [**las propiedades LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) y [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) de la clase [**\_ WMISetting de Win32**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para establecer límites en la prevención de memoria fuera de memoria. El valor mínimo indica cuándo WMI debe empezar a ralentizar la notificación de eventos y el valor máximo indica cuándo empezar a quitar eventos. Los valores predeterminados para los umbrales bajo y alto son 100 0000 (10 MB) y 200 0000 (20 MB). Además, puede establecer la propiedad [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para describir la cantidad de tiempo que WMI debe esperar antes de quitar eventos. El valor predeterminado de **MaxWaitOnEvents** es 2000 o 2 segundos.

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a>Recepción de notificaciones asincrónicas de eventos en VBScript

Las llamadas de scripting para recibir notificaciones de eventos son básicamente las mismas que todas las llamadas asincrónicas con los mismos problemas de seguridad. Para obtener más información, vea [Realizar una llamada asincrónica con VBScript.](making-an-asynchronous-call-with-vbscript.md)

**Para recibir notificaciones de eventos asincrónicas en VBScript**

1.  Cree un objeto receptor llamando a [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) y especificando el progid de "WbemScripting" y el tipo de objeto [**de SWbemSink**](swbemsink.md). El objeto receptor recibe las notificaciones.
2.  Escriba una subrutina para cada evento que desee controlar. En la tabla siguiente se enumeran [**los eventos SWbemSink.**](swbemsink.md)

    

    | Evento                                            | Significado                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [**OnObjectReady**](swbemsink-onobjectready.md) | Notifica las devoluciones de un objeto al receptor. El uso de esta llamada devuelve un objeto cada vez hasta que se completa la operación.     |
    | [**OnCompleted**](swbemsink-oncompleted.md)     | Informa cuando se completa una llamada asincrónica. Este evento nunca se produce si la operación es indefinida.                          |
    | [**OnObjectPut**](swbemsink-onobjectput.md)     | Informa de la finalización de una operación de colocación asincrónica. Este evento devuelve la ruta de acceso del objeto de la instancia o la clase guardada. |
    | [**OnProgress**](swbemsink-onprogress.md)       | Notifica el estado de una llamada asincrónica que está en curso. No todos los proveedores admiten informes de progreso provisionales.             |
    | [**Cancelar**](swbemsink-cancel.md)               | Cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.                                        |

    

     

El siguiente ejemplo de código VBScript notifica la eliminación de procesos con un intervalo de sondeo de 10 segundos. En este script, la subrutina SINK \_ OnObjectReady controla la aparición del evento. En el ejemplo, el objeto receptor se denomina "Sink", pero puede denominar este objeto como elija.


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



## <a name="receiving-asynchronous-event-notifications-in-c"></a>Recepción de notificaciones asincrónicas de eventos en C++

Para realizar una notificación asincrónica, cree un subproceso independiente únicamente para supervisar y recibir eventos de Windows Management Instrumentation (WMI). Cuando ese subproceso recibe un mensaje, el subproceso notifica a la aplicación principal.

Al dedicar un subproceso independiente, permite que el proceso principal realice otras actividades mientras espera a que llegue un evento. La entrega asincrónica de notificaciones mejora el rendimiento, pero puede proporcionar menos seguridad de la que desea. En C++, tiene la opción de usar la interfaz [**IWbemUnsecuredChev**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) o realizar comprobaciones de acceso en descriptores de seguridad. Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

**Para configurar notificaciones de eventos asincrónicas**

1.  Antes de inicializar las notificaciones asincrónicas, asegúrese de que los parámetros de evitación de memoria no memoria estén establecidos correctamente en [**\_ WMISetting de Win32.**](/windows/desktop/CIMWin32Prov/win32-wmisetting)

2.  Determine qué tipo de eventos desea recibir.

    WMI admite eventos intrínsecos y extrínsecos. Un evento intrínseco es un evento predefinido por WMI, mientras que un evento extrínseco es un evento definido por un proveedor de terceros. Para obtener más información, vea [Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)

En el procedimiento siguiente se describe cómo recibir notificaciones de eventos asincrónicas en C++.

**Para recibir notificaciones de eventos asincrónicas en C++**

1.  Configure la aplicación con llamadas a las [**funciones CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Al [**llamar a CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) se inicializa COM, mientras [**que CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) concede a WMI el permiso para llamar al proceso del consumidor. La **función CoInitializeEx** también le concede la capacidad de programar una aplicación multiproceso, que es necesaria para la notificación asincrónica. Para obtener más información, vea [Mantenimiento de la seguridad WMI.](maintaining-wmi-security.md)

    El código de este tema requiere las siguientes referencias e \# instrucciones include para compilarse correctamente.

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

    

2.  Cree un objeto receptor a través de [**la interfaz IWbemObjectSink.**](iwbemobjectsink.md)

    WMI usa [**IWbemObjectSink para**](iwbemobjectsink.md) enviar notificaciones de eventos y notificar el estado de una operación asincrónica o notificación de eventos.

3.  Registre el consumidor de eventos con una llamada [**al método IWbemServices::ExecNotificationQueryAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Asegúrese de que el *parámetro pResponseHandler* apunta al objeto receptor creado en el paso anterior.

    El propósito del registro es recibir solo las notificaciones necesarias. La recepción de notificaciones superfluas desperdicia el tiempo de procesamiento y entrega; y no usan la capacidad de filtrado de WMI al máximo potencial.

    Sin embargo, un consumidor temporal puede recibir más de un tipo de evento. En este caso, un consumidor temporal debe realizar llamadas independientes a [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) para cada tipo de evento. Por ejemplo, un consumidor podría requerir una notificación cuando se crean nuevos procesos (un evento de creación de instancias o [**\_ \_ InstanceCreationEvent)**](--instancecreationevent.md)y para los cambios en determinadas claves del Registro (un evento del Registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)). Por lo tanto, el consumidor realiza una llamada a [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) para registrarse para los eventos de creación de instancias y otra llamada a **ExecNotificationQueryAsync** para registrarse en eventos del Registro.

    Si decide crear un consumidor de eventos que se registre para varios eventos, debe evitar el registro de varias clases con el mismo receptor. En su lugar, use un receptor independiente para cada clase de evento registrado. Tener un receptor dedicado simplifica el procesamiento y ayuda en el mantenimiento, lo que le permite cancelar un registro sin afectar a los demás.

4.  Realice las actividades necesarias en el consumidor de eventos.

    Este paso debe contener la mayor parte del código e incluir actividades como mostrar eventos en una interfaz de usuario.

5.  Cuando termine, anule el registro del consumidor de eventos temporal con una llamada al evento [**IWbemServices::CancelAsyncCall.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)

    Independientemente de si la llamada a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) se realiza correctamente o no, no elimine el objeto receptor hasta que el recuento de referencias de objeto alcance cero. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

 
