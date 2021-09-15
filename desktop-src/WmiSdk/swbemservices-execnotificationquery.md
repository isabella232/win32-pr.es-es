---
description: Ejecuta una consulta para recibir eventos. La llamada se devuelve inmediatamente.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: Método SWbemServices.ExecNotificationQuery (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465480"
---
# <a name="swbemservicesexecnotificationquery-method"></a>Método SWbemServices.ExecNotificationQuery

El **método ExecNotificationQuery** del objeto [**SWbemServices**](swbemservices.md) ejecuta una consulta para recibir eventos. La llamada se devuelve inmediatamente. El usuario puede sondear el enumerador devuelto en busca de eventos a medida que llegan.

Se llama al método en modo semisincronoso. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strQuery* 
</dt> <dd>

Necesario. Cadena que contiene el texto de la consulta relacionada con eventos. Este parámetro no puede estar en blanco. Para obtener más información sobre la creación de cadenas de consulta WMI, vea [Consulta con WQL](querying-with-wql.md) y la [referencia de WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opcional\]
</dt> <dd>

Cadena que contiene el lenguaje de consulta que se va a usar. Si se especifica, este valor debe ser "WQL".

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Se trata de un entero que determina el comportamiento de la consulta. El valor predeterminado es **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly.** Si especifica este parámetro, este parámetro debe establecerse en **wbemFlagReturnImmediately** y **wbemFlagForwardOnly** o se produce un error en la llamada. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly** (32 (0x20))


</dt> <dd>

Hace que se devuelva un enumerador de solo avance. Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Hace que la llamada se devuelva inmediatamente.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si no se produce ningún error, este método devuelve un [**objeto SWbemEventSource.**](swbemeventsource.md) Puede llamar al método [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) para recuperar eventos a medida que llegan.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ExecNotificationQuery,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

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

Se especificó un parámetro no válido.

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

A diferencia [**del método SWbemServices.ExecQueryAsync,**](swbemservices-execqueryasync.md) **ExecNotificationQuery** devuelve objetos de tipo de evento generados por eventos futuros en lugar de objetos existentes. Los objetos de evento que **solicita ExecNotificationQuery** pueden ser intrínsecos (como [**\_ \_ InstanceCreationEvent)**](--instancecreationevent.md)o extrínsecos (por ejemplo, eventos de proveedor del Registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) o eventos SNMP). Para obtener más información, vea [Determinar el tipo de evento que se debe recibir](determining-the-type-of-event-to-receive.md) y recibir notificaciones de [eventos](receiving-event-notifications.md).

Hay límites en el número de palabras clave **AND** **y OR** que se pueden usar en consultas WQL. Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error **WBEM \_ E QUOTA \_ \_ VIOLATION** como **un valor HRESULT.** El límite de palabras clave WQL depende de lo compleja que sea la consulta.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se supervisan los cambios en los volúmenes de un equipo local. Tenga en [**cuenta que Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) es un evento extrínseco definido por un proveedor que no es un evento intrínseco definido por WMI. Para obtener más información, [vea Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



En el ejemplo de código de VBScript siguiente se supervisa la eliminación de procesos. Si elimina un proceso en Administrador de tareas cerrar una aplicación, el script muestra un mensaje. Tenga en cuenta que este script consulta un evento intrínseco definido por WMI: [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
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

[**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[Recepción de un evento WMI](receiving-a-wmi-event.md)
</dt> <dt>

[Consulta con WQL](querying-with-wql.md)
</dt> <dt>

[WQL (SQL para WMI)](wql-sql-for-wmi.md)
</dt> <dt>

[Determinar el tipo de evento que se recibirá](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

