---
description: Ejecuta una consulta para recibir eventos.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: Método SWbemServices.ExecNotificationQueryAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465479"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a>Método SWbemServices.ExecNotificationQueryAsync

El **método ExecNotificationQueryAsync** del objeto [**SWbemServices**](swbemservices.md) ejecuta una consulta para recibir eventos. Esta llamada se devuelve inmediatamente y los resultados y el estado se devuelven al autor de la llamada a través de eventos entregados al receptor especificado en *objWbemSink*.

Los eventos especificados en la consulta pueden ser eventos Windows Management Instrumentation (WMI) intrínsecos, como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)o eventos extrínsecos, como [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) o [**RegistryKeyChangeEvent.**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) Para obtener más información, vea [Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)

Se llama al método en modo asincrónico. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Necesario. Receptor de objetos que recibe la notificación de eventos de forma asincrónica. Cree un [**objeto SWbemSink**](swbemsink.md) para recibir los objetos.

</dd> <dt>

*strQuery* 
</dt> <dd>

Necesario. Cadena que contiene el texto de la consulta relacionada con eventos. Este parámetro no puede estar en blanco. Para obtener más información sobre la creación de cadenas de consulta WMI, vea Consulta con [WQL](querying-with-wql.md) y la referencia [de WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opcional\]
</dt> <dd>

Cadena que contiene el lenguaje de consulta que se va a usar. Si se especifica, este valor debe ser "WQL".

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Entero que determina el comportamiento de la consulta. Este parámetro se puede establecer en los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que proporciona servicios a la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ Opcional\]
</dt> <dd>

Se trata de [**un objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro para realizar varias llamadas asincrónicas con el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. El **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obtener más información, vea [Llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si se realiza correctamente, el receptor recibe un [**evento OnObjectReady**](swbemsink-onobjectready.md) por instancia. Después de la última instancia, el receptor del objeto recibe [**un evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ExecNotificationQueryAsync,** el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error identificados en la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no está autorizado para ver el conjunto de resultados.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se ha especificado un parámetro no válido.

</dd> <dt>

**wbemErrInvalidQuery:** 2147749911 (0x80041017)
</dt> <dd>

La sintaxis de consulta no es válida.

</dd> <dt>

**wbemErrInvalidQueryType:** 2147749912 (0x80041018)
</dt> <dd>

No se admite el lenguaje de consulta solicitado.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **método ExecNotificationQueryAsync devuelve** objetos de tipo de evento que generan eventos futuros. Los objetos de evento que **solicita ExecNotificationQueryAsync** pueden ser intrínsecos (por ejemplo, [**\_ \_ InstanceCreationEvent)**](--instancecreationevent.md)o extrínsecos (por ejemplo, [**eventos RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) o SNMP). Para obtener más información, vea [Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)

La llamada a **ExecNotificationQueryAsync** se devuelve inmediatamente. Los objetos y el estado solicitados se devuelven al autor de la llamada a través de devoluciones de llamada entregadas al receptor especificado en *objWbemSink*. Para procesar cada objeto cuando se devuelve, cree *un objeto objWbemSink*. [**Subrutina de eventos OnObjectReady.**](swbemsink-onobjectready.md) Una vez devueltos todos los objetos, realice el procesamiento final para implementar *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Una devolución de llamada asincrónica permite a un usuario no autenticado proporcionar datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

Hay límites en el número de palabras clave **AND** y **OR** que se pueden usar en consultas WQL. Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error **WBEM \_ E QUOTA \_ \_ VIOLATION** como valor **HRESULT.** El límite de palabras clave WQL depende de la complejidad de la consulta.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra un script que está esperando una notificación de eventos WMI que indica que un proceso ha finalizado. Está esperando un evento intrínseco wmi, una instancia de la clase de eventos [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md). **\_ \_ InstanceDeletionEvent debe** representar la eliminación de una instancia de [**Proceso de Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process) Para obtener más información sobre los eventos intrínsecos de WMI, vea [Determinar el tipo de evento que se debe recibir.](determining-the-type-of-event-to-receive.md)

El siguiente script se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script. Para detener el script manualmente, use Administrador de tareas para detener el proceso. Para detenerla mediante programación, use el [**método Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) en la clase Process de Win32. \_


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
</dt> <dt>

[Registro de eventos del Registro del sistema](registering-for-system-registry-events.md)
</dt> <dt>

[Determinar el tipo de evento que se recibirá](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> <dt>

[Establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

