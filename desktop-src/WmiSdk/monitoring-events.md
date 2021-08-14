---
description: Los administradores del sistema pueden usar WMI para supervisar eventos en una red.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Supervisión de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90a0a6eef87f88543e8f2414bc38bdea4f7d89c577471d79d23393f331b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317119"
---
# <a name="monitoring-events"></a>Supervisión de eventos

Los administradores del sistema pueden usar WMI para supervisar eventos en una red. Por ejemplo:

-   Un servicio se detiene inesperadamente.
-   Un servidor deja de estar disponible.
-   Una unidad de disco se llena al 80 % de su capacidad.
-   Los eventos de seguridad se notifican a un registro de eventos NT.

WMI admite la detección y entrega de eventos a los consumidores de eventos porque algunos proveedores WMI son proveedores de eventos. Para obtener más información, vea [Recibir un evento WMI](receiving-a-wmi-event.md).

[*Los consumidores de eventos*](gloss-e.md) son aplicaciones o scripts que solicitan la notificación de eventos y, a continuación, realizan tareas cuando se producen eventos específicos. Puede crear scripts de supervisión de eventos o aplicaciones que supervisen temporalmente cuándo se producen los eventos. WMI también proporciona un conjunto de proveedores de eventos permanentes preinstalados y las clases de consumidor permanentes que permiten supervisar eventos de forma permanente. Para obtener más información, [vea Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

En este tema se de abordan las secciones siguientes:

-   [Uso de consumidores de eventos temporales](#using-temporary-event-consumers)
-   [Uso de consumidores de eventos permanentes](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Uso de consumidores de eventos temporales

Los consumidores de eventos temporales son scripts o aplicaciones que devuelven los eventos que coinciden con una consulta o filtro de eventos. Las consultas de eventos temporales suelen usar [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en aplicaciones de C++ oSWbemServices.Exe [**cNotificationQuery**](swbemservices-execnotificationquery.md) en scripts y Visual Basic.

Una consulta de eventos solicita instancias de una clase de evento que especifica un determinado tipo de evento, como [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) o [**RegistryKeyChangeEvent.**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)

En el ejemplo de código de VBScript siguiente se solicita una notificación cuando se crea una instancia de [**\_ ProcessTrace de Win32.**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) Una instancia de esta clase se genera cuando se inicia o detiene un proceso.

Para ejecutar el script, cópielo en un archivo denominado event.vbs y use la siguiente línea de comandos: **cscript event.vbs**. Puede ver la salida del script iniciando Notepad.exe o cualquier otro proceso. El script se detiene después de que se han iniciado o detenido cinco procesos.

Este script llama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), que es la [*versión semisincronosa*](gloss-s.md) del método. Vea el siguiente script para obtener un ejemplo de configuración de una suscripción de eventos temporales asincrónica llamando a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obtener más información, vea [Llamar a un método](calling-a-method.md). El script llama [**a SWbemEventSource.NextEvent para**](swbemeventsource-nextevent.md) obtener y procesar cada evento a medida que llega. Guarde el script en un archivo con una extensión .vbs y ejecute el script en una línea de comandos mediante CScript: **cscript file.vbs**.


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



Los consumidores de eventos temporales deben iniciarse manualmente y no deben persistir entre reinicios de WMI o reinicios del sistema operativo. Un consumidor de eventos temporal solo puede procesar eventos mientras se está ejecutando.

En el procedimiento siguiente se describe cómo crear un consumidor de eventos temporal.

**Para crear un consumidor de eventos temporal**

1.  Decida qué lenguaje de programación usar.

    El lenguaje de programación determina la API que se usará.

    -   Para el lenguaje de programación C++, use la [API COM para WMI.](com-api-for-wmi.md)
    -   Para Visual Basic o lenguajes de scripting, use [scripting API para WMI.](scripting-api-for-wmi.md)

2.  Empiece a codificar una aplicación de consumidor de eventos temporal de la misma manera que inicia una aplicación WMI.

    Los primeros pasos de codificación dependen del lenguaje de programación. Normalmente, inicia sesión en WMI y configura la configuración de seguridad. Para obtener más información, vea [Crear una aplicación WMI o script](creating-a-wmi-application-or-script.md).

3.  Defina la consulta de eventos que desea usar.

    Para obtener algunos tipos de datos de rendimiento, puede que tenga que usar clases proporcionadas por proveedores de alto rendimiento. Para obtener más información, vea [Monitoring Performance Data](monitoring-performance-data.md), Determining the Type of Event To [Receive](determining-the-type-of-event-to-receive.md)y [Querying with WQL](querying-with-wql.md).

4.  Decida realizar una llamada asincrónica o una llamada semisincronosa y elija el método de API.

    Las llamadas asincrónicas permiten evitar la sobrecarga del sondeo de datos. Sin embargo, las llamadas semisincronosas proporcionan un rendimiento similar con mayor seguridad. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

5.  Realice la llamada a método asincrónico o semisincronoso e incluya una consulta de eventos como parámetro *strQuery.*

    Para las aplicaciones de C++, llame a los métodos siguientes:

    -   [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    En el caso de los scripts, llame a los métodos siguientes:

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Escriba el código para procesar el objeto de evento devuelto.

    Para las consultas de eventos asincrónicas, coloque el código en los distintos métodos o eventos del receptor del objeto. Para las consultas de eventos semisincronosos, cada objeto se devuelve a medida que WMI lo obtiene, por lo que el código debe estar en el bucle que controla cada objeto.

El siguiente ejemplo de código de script es una versión asincrónica del script [**\_ ProcessTrace de Win32.**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) Dado que las operaciones asincrónicas se devuelven inmediatamente, un cuadro de diálogo mantiene el script activo mientras espera eventos.

En lugar de llamar a [**SWbemEventSource.NextEvent para**](swbemeventsource-nextevent.md) recibir cada evento, el script tiene un controlador de eventos para el evento [**OnObjectReady de SWbemSink.**](swbemsink-onobjectready.md)


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
> Una devolución de llamada asincrónica, como una devolución de llamada que controla la subrutina, permite a un usuario no autenticado proporcionar datos `SINK_OnObjectReady` al receptor. Para mejorar la seguridad, use la comunicación semisincronosa o la comunicación sincrónica. Para obtener más información, vea los temas siguientes:
>
> -   [Realizar una llamada semisincronosa con C++](making-a-semisynchronous-call-with-c--.md)
> -   [Realizar una llamada semisincronosa con VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Realizar una llamada asincrónica con C++](making-an-asynchronous-call-with-c--.md)
> -   [Realizar una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md)
> -   [Protección de clientes de scripting](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Uso de consumidores de eventos permanentes

Un consumidor de eventos permanente se ejecuta hasta que su registro se cancela explícitamente y, a continuación, se inicia cuando se reinicia WMI o el sistema.

Un consumidor de eventos permanente es una combinación de clases WMI, filtros y objetos COM en un sistema.

En la lista siguiente se identifican los elementos necesarios para crear un consumidor de eventos permanente:

-   Objeto COM que contiene el código que implementa el consumidor permanente.
-   Nueva clase de consumidor permanente.
-   Instancia de la clase de consumidor permanente.
-   Filtro que contiene la consulta de eventos.
-   Vínculo entre el consumidor y el filtro.

Para obtener más información, vea [Recepción de eventos en todo momento.](--filtertoconsumerbinding.md)

WMI proporciona varios consumidores permanentes. Las clases de consumidor y el objeto COM que contiene el código están preinstalados. Por ejemplo, puede crear y configurar una instancia de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para ejecutar un script cuando se produce un evento. Para obtener más información, [vea Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md) Para obtener un ejemplo del uso **de ActiveScriptEventConsumer,** vea [Ejecutar un script basado en un evento](running-a-script-based-on-an-event.md).

En el procedimiento siguiente se describe cómo crear un consumidor de eventos permanente.

**Para crear un consumidor de eventos permanente**

1.  [Registre el proveedor de eventos](registering-a-provider.md) con el espacio de nombres que está usando.

    Algunos proveedores de eventos solo pueden usar un espacio de nombres específico. Por ejemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) es un evento intrínseco que es compatible con el proveedor [win32](/windows/desktop/CIMWin32Prov/win32-provider) y está registrado de forma predeterminada con el espacio de nombres \\ \\ cimv2 raíz.

    > [!Note]  
    > Puede usar la propiedad **EventNamespace** de [**\_ \_ EventFilter**](--eventfilter.md) que se usa en el registro para crear una suscripción entre espacios de nombres. Para obtener más información, vea Implementar suscripciones de eventos [permanentes entre espacios de nombres.](implementing-cross-namespace-permanent-event-subscriptions.md)

     

2.  [Registre el proveedor de consumidores de eventos](registering-an-event-consumer-provider.md) con el espacio de nombres donde se encuentran las clases de eventos.

    WMI usa un proveedor de consumidores de eventos para buscar un consumidor de eventos que sea permanente. El consumidor de eventos permanente es la aplicación que WMI inicia cuando se recibe un evento. Para registrar el consumidor de eventos, los proveedores crean instancias de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Cree una instancia de la clase que represente el consumidor de eventos permanente que desea usar.

    Las clases de consumidor de eventos se derivan de la [**\_ \_ clase EventConsumer**](--eventconsumer.md). Establezca las propiedades que requiere la instancia del consumidor de eventos.

4.  Registre el consumidor con COM mediante la **utilidad regsvr32.**
5.  Cree una instancia de la clase de filtro de eventos [**\_ \_ EventFilter**](--eventfilter.md).

    Establezca los campos necesarios para la instancia de filtro de eventos. Los campos necesarios para [**\_ \_ EventFilter**](--eventfilter.md) son **Name**, **QueryLanguage** y **Query**. La **propiedad Name** puede ser cualquier nombre único para una instancia de esta clase. La **propiedad QueryLanguage** siempre se establece en "WQL". La **propiedad Query** es una cadena que contiene una consulta de eventos. Se genera un evento cuando se produce un error en la consulta de un consumidor de eventos permanente. El origen del evento es WinMgmt, el identificador de evento es 10 y el tipo de evento es Error.

6.  Cree una instancia de la [**\_ \_ clase FilterToConsumerBinding para**](--filtertoconsumerbinding.md) asociar un consumidor de eventos lógicos a un filtro de eventos.

    WMI usa una asociación para buscar el consumidor de eventos asociado al evento que coincide con los criterios especificados en el filtro de eventos. WMI usa el proveedor de consumidores de eventos para buscar la aplicación de consumidor de eventos permanente que se debe iniciar.

 

 
