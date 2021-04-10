---
description: WMI contiene una infraestructura de eventos que genera notificaciones sobre los cambios en los datos y servicios de WMI. Las clases de eventos WMI proporcionan una notificación cuando se producen eventos específicos.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Recibir un evento de WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155861"
---
# <a name="receiving-a-wmi-event"></a>Recibir un evento de WMI

WMI contiene una infraestructura de eventos que genera notificaciones sobre los cambios en los datos y servicios de WMI. [*Las clases de eventos*](gloss-e.md) WMI proporcionan una notificación cuando se producen eventos específicos.

En este tema se describen las siguientes secciones:

-   [Consultas de eventos](#event-queries)
-   [Ejemplo](#example)
-   [Consumidores de eventos](#event-consumers)
-   [Proporcionar eventos](#providing-events)
-   [Cuotas de suscripción](#subscription-quotas)
-   [Temas relacionados](#related-topics)

## <a name="event-queries"></a>Consultas de eventos

Puede crear una consulta [semisincrónica](receiving-synchronous-and-semisynchronous-event-notifications.md) o [**asincrónica**](receiving-asynchronous-event-notifications.md) para supervisar los cambios en los registros de eventos, la creación de procesos, el estado del servicio, la disponibilidad del equipo o el espacio libre en la unidad de disco, y otras entidades o eventos. En scripting, el método [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) se usa para suscribirse a eventos. En C++, se utiliza [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) . Para obtener más información, consulte [llamar a un método](calling-a-method.md).

La notificación de un cambio en el modelo de datos WMI estándar se denomina [*evento intrínseco*](gloss-i.md). [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) o [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) son ejemplos de eventos intrínsecos. La notificación de un cambio que realiza un proveedor para definir un evento de proveedor se denomina [*evento extrínseco*](gloss-e.md). Por ejemplo, el proveedor de [registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), el [proveedor de eventos de administración de energía](/windows/desktop/CIMWin32Prov/power-management-event-provider)y el proveedor de [Win32](/windows/desktop/CIMWin32Prov/win32-provider) definen sus propios eventos. Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).

## <a name="example"></a>Ejemplo

El siguiente ejemplo de código de script es una consulta para el [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrínseco de la clase de evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Puede ejecutar este programa en segundo plano y, cuando se produce un evento, aparece un mensaje. Si cierra el cuadro **de diálogo esperando eventos** , el programa deja de esperar los eventos. Tenga en cuenta que **SeSecurityPrivilege** debe estar habilitado.


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





En el ejemplo de código de VBScript siguiente se muestra el evento extrínseco [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) que define el proveedor del registro. El script crea un consumidor temporal mediante la llamada a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)y solo recibe eventos cuando se ejecuta el script. El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script. Para detener el script manualmente, use el administrador de tareas para detener el proceso. Para detenerlo mediante programación, use el método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) en la clase de proceso de Win32 \_ . Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a>Consumidores de eventos

Puede supervisar o consumir eventos mediante los siguientes consumidores mientras se ejecuta un script o una aplicación:

-   Consumidores de eventos temporales

    Un [*consumidor temporal*](gloss-t.md) es una aplicación cliente de WMI que recibe un evento WMI. WMI incluye una interfaz única que se utiliza para especificar los eventos que WMI envía a una aplicación cliente. Un consumidor de eventos temporal se considera temporal porque solo funciona cuando lo carga específicamente un usuario. Para obtener más información, consulte [recepción de eventos para la duración de la aplicación](receiving-events-for-the-duration-of-your-application.md).

-   Consumidores de eventos permanentes

    Un [*consumidor permanente*](gloss-p.md) es un objeto com que puede recibir un evento WMI en todo momento. Un consumidor de eventos permanente utiliza un conjunto de objetos y filtros persistentes para capturar un evento WMI. Al igual que un consumidor de eventos temporal, se configura una serie de objetos y filtros WMI que capturan un evento WMI. Cuando se produce un evento que coincide con un filtro, WMI carga el consumidor de eventos permanente y lo notifica sobre el evento. Dado que un consumidor permanente está implementado en el repositorio WMI y es un archivo ejecutable que se registra en WMI, el consumidor de eventos permanente opera y recibe los eventos una vez creado, e incluso después de reiniciar el sistema operativo, siempre y cuando WMI se esté ejecutando. Para obtener más información, consulte [recibir eventos en todo momento](receiving-events-at-all-times.md).

Los scripts o las aplicaciones que reciben eventos tienen consideraciones de seguridad especiales. Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).

Una aplicación o un script puede usar un proveedor de eventos WMI integrado que proporciona [clases de consumidor estándar](standard-consumer-classes.md). Cada clase de consumidor estándar responde a un evento con una acción diferente mediante el envío de un mensaje de correo electrónico o la ejecución de un script. No es necesario escribir código de proveedor para usar una clase de consumidor estándar para crear un consumidor de eventos permanente. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="providing-events"></a>Proporcionar eventos

Un proveedor de eventos es un componente COM que envía un evento a WMI. Puede crear un proveedor de eventos para enviar un evento en una aplicación de C++ o C#. La mayoría de los proveedores de eventos administran un objeto para WMI, por ejemplo, una aplicación o un elemento de hardware. Para obtener más información, consulte [escribir un proveedor de eventos](writing-an-event-provider.md).

Un evento de tiempo o repetición es un evento que se produce en un tiempo predeterminado.

WMI proporciona las siguientes formas de crear eventos de tiempo o repetición para las aplicaciones:

-   La infraestructura de eventos estándar de Microsoft.
-   Una clase de temporizador especializada.

Para obtener más información, consulte [recibir un evento con tiempo o repetir](receiving-a-timed-or-repeating-event.md). Al escribir un proveedor de eventos, tenga en cuenta la información de seguridad identificada en [proporcionar eventos de forma segura](providing-events-securely.md).

Se recomienda que las suscripciones de eventos permanentes se compilen en el espacio de nombres de la \\ \\ suscripción raíz. Para obtener más información, consulte [implementación de suscripciones de eventos permanentes entre espacios de nombres](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Cuotas de suscripción

El sondeo de eventos puede degradar el rendimiento de los proveedores que admiten consultas en conjuntos de datos de gran tamaño. Además, cualquier usuario que tenga acceso de lectura a un espacio de nombres con proveedores dinámicos puede realizar un ataque de denegación de servicio (DoS). WMI mantiene cuotas para todos los usuarios combinados y para cada consumidor de eventos en la única instancia de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) que se encuentra en el \\ espacio de nombres raíz. Estas cuotas son globales en lugar de para cada espacio de nombres. No se pueden cambiar las cuotas.

WMI actualmente aplica cuotas mediante las propiedades de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). Cada cuota tiene un por usuario y una versión total que incluye todos los usuarios combinados, no por espacio de nombres. En la tabla siguiente se enumeran las cuotas que se aplican a las propiedades de **\_ \_ ArbitratorConfiguration** .



| Total/perusuario                                                                   | Quota                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| TemporarySubscriptionsTotal<br/> TemporarySubscriptionsPerUser<br/> | 10 000<br/> 1,000<br/>                                          |
| PermanentSubscriptionsTotal<br/> PermanentSubscriptionsPerUser<br/> | 10 000<br/> 1,000<br/>                                          |
| PollingInstructionsTotal<br/> PollingInstructionsPerUser<br/>       | 10 000<br/> 1,000<br/>                                          |
| PollingMemoryTotal<br/> PollingMemoryPerUser<br/>                   | 10 millones (0x989680) bytes<br/> 5 millones (0x4CB40) bytes<br/> |



 

Un administrador o un usuario con permiso de **\_ escritura completo** en el espacio de nombres puede modificar la instancia singleton de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). WMI realiza un seguimiento de la cuota por usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar WMI](using-wmi.md)
</dt> </dl>

 

