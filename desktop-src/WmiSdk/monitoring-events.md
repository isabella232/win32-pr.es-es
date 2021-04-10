---
description: Los administradores del sistema pueden utilizar WMI para supervisar los eventos de una red.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Supervisión de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155240"
---
# <a name="monitoring-events"></a>Supervisión de eventos

Los administradores del sistema pueden utilizar WMI para supervisar los eventos de una red. Por ejemplo:

-   Un servicio se detiene inesperadamente.
-   Un servidor deja de estar disponible.
-   Una unidad de disco se llena hasta el 80% de la capacidad.
-   Los eventos de seguridad se registran en un registro de eventos de NT.

WMI admite la detección y entrega de eventos a los consumidores de eventos porque algunos proveedores de WMI son proveedores de eventos. Para obtener más información, consulte [recibir un evento WMI](receiving-a-wmi-event.md).

Los [*consumidores de eventos*](gloss-e.md) son aplicaciones o scripts que solicitan notificación de eventos y, a continuación, realizan tareas cuando se producen eventos específicos. Puede crear scripts o aplicaciones de supervisión de eventos que se supervisan temporalmente cuando se producen eventos. WMI también proporciona un conjunto de proveedores de eventos permanentes preinstalados y las clases de consumidor permanentes que permiten supervisar eventos de forma permanente. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

En este tema se describen las siguientes secciones:

-   [Usar consumidores de eventos temporales](#using-temporary-event-consumers)
-   [Uso de consumidores de eventos permanentes](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Usar consumidores de eventos temporales

Los consumidores de eventos temporales son scripts o aplicaciones que devuelven los eventos que coinciden con una consulta o un filtro de eventos. Normalmente, las consultas de eventos temporales utilizan [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en aplicaciones de C++ o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) en scripts y Visual Basic.

Una consulta de eventos solicita instancias de una clase de eventos que especifica un tipo determinado de evento, como [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) o [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

El siguiente ejemplo de código de VBScript solicita la notificación cuando se crea una instancia de [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) . Se genera una instancia de esta clase cuando se inicia o se detiene un proceso.

Para ejecutar el script, cópielo en un archivo denominado event.vbs y use la siguiente línea de comandos: **cscript event.vbs**. Puede ver la salida del script iniciando Notepad.exe o cualquier otro proceso. El script se detiene una vez que se han iniciado o detenido cinco procesos.

Este script llama a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), que es la versión [*semisincrónica*](gloss-s.md) del método. Vea el siguiente script para obtener un ejemplo de configuración de una suscripción de eventos temporal asincrónica mediante una llamada a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obtener más información, consulte [llamar a un método](calling-a-method.md). El script llama a [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para obtener y procesar cada evento a medida que llega. Guarde el script en un archivo con la extensión. vbs y ejecute el script en una línea de comandos con CScript: **cscript file.vbs**.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



Los consumidores de eventos temporales deben iniciarse manualmente y no deben conservarse entre los reinicios de WMI o los reinicios del sistema operativo. Un consumidor de eventos temporal solo puede procesar eventos mientras se está ejecutando.

En el procedimiento siguiente se describe cómo crear un consumidor de eventos temporal.

**Para crear un consumidor de eventos temporal**

1.  Decida el lenguaje de programación que se va a usar.

    El lenguaje de programación determina la API que se va a usar.

    -   Para el lenguaje de programación C++, utilice la [API com para WMI](com-api-for-wmi.md).
    -   En el caso de Visual Basic o lenguajes de scripting, utilice la [API de scripting para WMI](scripting-api-for-wmi.md).

2.  Empiece a codificar una aplicación de consumidor de eventos temporal del mismo modo que inicia una aplicación WMI.

    Los primeros pasos de la codificación dependen del lenguaje de programación. Normalmente, se inicia sesión en WMI y se establece la configuración de seguridad. Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).

3.  Defina la consulta de eventos que desea utilizar.

    Para obtener algunos tipos de datos de rendimiento, puede que necesite usar clases proporcionadas por proveedores de alto rendimiento. Para obtener más información, vea [supervisar datos de rendimiento](monitoring-performance-data.md), [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md)y [realizar consultas con WQL](querying-with-wql.md).

4.  Decida realizar una llamada asincrónica o una llamada semisincrónica y elija el método de la API.

    Las llamadas asincrónicas le permiten evitar la sobrecarga que supone el sondeo de los datos. Sin embargo, las llamadas sincrónicas proporcionan un rendimiento similar con mayor seguridad. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

5.  Realice la llamada al método asincrónico o semisincrónico e incluya una consulta de evento como el parámetro *strQuery* .

    Para las aplicaciones de C++, llame a los métodos siguientes:

    -   [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Para los scripts, llame a los métodos siguientes:

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Escriba el código para procesar el objeto de evento devuelto.

    En el caso de las consultas de eventos asincrónicos, coloque el código en los distintos métodos o eventos del receptor de objetos. En el caso de las consultas de eventos semisincrónicas, cada objeto se devuelve a medida que WMI lo obtiene, por lo que el código debe estar en el bucle que controla cada objeto.

El siguiente ejemplo de código de script es una versión asincrónica del [**script \_ ProcessTrace de Win32**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) . Dado que las operaciones asincrónicas se devuelven inmediatamente, un cuadro de diálogo mantiene el script activo mientras espera eventos.

En lugar de llamar a [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para recibir cada evento, el script tiene un controlador de eventos para el evento [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) .


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> Una devolución de llamada asincrónica, como una devolución de llamada administrada por la `SINK_OnObjectReady` subrutina, permite que un usuario no autenticado proporcione datos al receptor. Para mejorar la seguridad, utilice la comunicación semisincrónica o la comunicación sincrónica. Para obtener más información, vea los temas siguientes:
>
> -   [Realización de una llamada semisincrónica con C++](making-a-semisynchronous-call-with-c--.md)
> -   [Realización de una llamada semisincrónica con VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Realización de una llamada asincrónica con C++](making-an-asynchronous-call-with-c--.md)
> -   [Realización de una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md)
> -   [Protección de los clientes de scripting](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Uso de consumidores de eventos permanentes

Un consumidor de eventos permanente se ejecuta hasta que su registro se cancela explícitamente y, a continuación, se inicia cuando WMI o el sistema se reinicia.

Un consumidor de eventos permanente es una combinación de clases de WMI, filtros y objetos COM de un sistema.

En la lista siguiente se identifican los elementos necesarios para crear un consumidor de eventos permanente:

-   Objeto COM que contiene el código que implementa el consumidor permanente.
-   Nueva clase de consumidor permanente.
-   Instancia de la clase de consumidor permanente.
-   Filtro que contiene la consulta de eventos.
-   Un vínculo entre el consumidor y el filtro.

Para obtener más información, consulte [recibir eventos en todo momento](--filtertoconsumerbinding.md).

WMI proporciona varios consumidores permanentes. Las clases de consumidor y el objeto COM que contiene el código están preinstalados. Por ejemplo, puede crear y configurar una instancia de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para ejecutar un script cuando se produce un evento. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md). Para obtener un ejemplo del uso de **ActiveScriptEventConsumer**, vea [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md).

En el procedimiento siguiente se describe cómo crear un consumidor de eventos permanente.

**Para crear un consumidor de eventos permanente**

1.  [Registre el proveedor de eventos](registering-a-provider.md) con el espacio de nombres que está usando.

    Algunos proveedores de eventos solo pueden usar un espacio de nombres específico. Por ejemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) es un evento intrínseco que es compatible con el [proveedor de Win32](/windows/desktop/CIMWin32Prov/win32-provider) y se registra de forma predeterminada con el \\ espacio de \\ nombres root cimv2.

    > [!Note]  
    > Puede usar la propiedad **EventNamespace** de [**\_ \_ EventFilter**](--eventfilter.md) que se usa en el registro para crear una suscripción entre espacios de nombres. Para obtener más información, consulte [implementación de suscripciones de eventos permanentes entre espacios de nombres](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Registre el proveedor del consumidor de eventos](registering-an-event-consumer-provider.md) con el espacio de nombres donde se encuentran las clases de eventos.

    WMI usa un proveedor de consumidor de eventos para buscar un consumidor de eventos que sea permanente. El consumidor de eventos permanente es la aplicación que WMI inicia cuando se recibe un evento. Para registrar el consumidor de eventos, los proveedores crean instancias de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Cree una instancia de la clase que represente el consumidor de eventos permanente que desee usar.

    Las clases de consumidor de eventos se derivan de la clase [**\_ \_ EventConsumer**](--eventconsumer.md). Establezca las propiedades que requiere la instancia del consumidor de eventos.

4.  Registre el consumidor con COM mediante la utilidad **regsvr32** .
5.  Cree una instancia de la clase de filtro de eventos [**\_ \_ EventFilter**](--eventfilter.md).

    Establezca los campos obligatorios para la instancia de filtro de eventos. Los campos obligatorios para [**\_ \_ EventFilter**](--eventfilter.md) son **nombre**, **QueryLanguage** y **consulta**. La propiedad **Name** puede ser cualquier nombre único de una instancia de esta clase. La propiedad **QueryLanguage** siempre se establece en "WQL". La propiedad de **consulta** es una cadena que contiene una consulta de evento. Se genera un evento cuando se produce un error en la consulta del consumidor de eventos permanente. El origen del evento es WinMgmt, el ID. de evento es 10 y el tipo de evento es error.

6.  Cree una instancia de la clase [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar un consumidor de eventos lógicos a un filtro de eventos.

    WMI utiliza una asociación para buscar el consumidor de eventos asociado al evento que coincide con los criterios especificados en el filtro de eventos. WMI utiliza el proveedor de consumidor de eventos para encontrar la aplicación de consumidor de eventos permanente que se va a iniciar.

 

 
