---
description: 'SWbemServices.Exemétodo cQuery: ejecuta una consulta para recuperar objetos.'
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cQuery (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9e827b1297a2bdd3bac39a22efa7f80e0d4723ded689e691423c6945a88bb729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897495"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.Exemétodo cQuery

El **método ExecQuery** del [**objeto SWbemServices**](swbemservices.md) ejecuta una consulta para recuperar objetos. Estos objetos están disponibles a través de la [**colección SWbemObjectSet**](swbemobjectset.md) devuelta.

Se llama a este método en modo semisincronoso. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObjectSet = .ExecQuery( _
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

Obligatorio. Cadena que contiene el texto de la consulta. Este parámetro no puede estar en blanco. Para obtener más información sobre la creación de cadenas de consulta WMI, vea Consulta con [WQL](querying-with-wql.md) y la referencia [de WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opcional\]
</dt> <dd>

Cadena que contiene el lenguaje de consulta que se va a usar. Si se especifica, este valor debe ser "WQL".

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Entero que determina el comportamiento de la consulta y determina si esta llamada se devuelve inmediatamente. El valor predeterminado de este parámetro es **wbemFlagReturnImmediately**. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly** (32 (0x20))


</dt> <dd>

Hace que se devuelva un enumerador de solo avance. Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional** (0 (0x0))


</dt> <dd>

Hace que WMI conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Hace que la llamada se devuelva inmediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Hace que esta llamada se bloquee hasta que se complete la consulta. Esta marca llama al método en modo sincrónico.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype** (2 (0x2))


</dt> <dd>

Se usa para la creación de prototipos. Esta marca impide que se haga la consulta y devuelve un objeto que parece un objeto de resultado típico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI devuelva datos de modificación de clases con la definición de clase base. Para obtener más información, vea [Localizing WMI Class Information](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si no se produce ningún error, este método devuelve un [**objeto SWbemObjectSet.**](swbemobjectset.md) Se trata de una colección de objetos que contiene el conjunto de resultados de la consulta. El autor de la llamada puede examinar la colección mediante la implementación de colecciones para el lenguaje de programación que está usando. Para obtener más información, vea [Accessing a Collection](accessing-a-collection.md).

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ExecQuery,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para ver el conjunto de resultados.

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

## <a name="remarks"></a>Comentarios

**ExecQuery** es una de las llamadas más usadas para recuperar información de WMI. Una llamada estándar a **ExecQuery** tiene un aspecto similar al siguiente:


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



Tenga en cuenta que crea el objeto [**SWbemServices**](swbemservices.md) con un moniker que representa el espacio de nombres y la seguridad adecuados y, a continuación, realiza la llamada **a ExecQuery** a través del servicio. Para obtener una explicación más completa, vea [Crear un script WMI](creating-a-wmi-script.md) y [Enumerar WMI.](enumerating-wmi.md)

Al igual [**que el método InstancesOf,**](swbemservices-instancesof.md) **el método ExecQuery** siempre devuelve una [**colección SWbemObjectSet.**](swbemobjectset.md) Por lo tanto, el script WMI debe enumerar la colección que devuelve ExecQuery para tener acceso a cada instancia de recurso administrado de la colección, como se muestra aquí:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Otros [**métodos SWbemServices**](swbemservices.md) que devuelven [**un SWbemObjectSet**](swbemobjectset.md) incluyen [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md)y [**SubclassesOf**](swbemservices-subclassesof.md).

No es un error que la consulta devuelva un conjunto de resultados vacío. El **método ExecQuery** devuelve propiedades de clave independientemente de si se solicita o no la propiedad de clave en el *argumento strQuery.* Si se produce un error al ejecutar este método y no se usa la marca **wbemFlagReturnImmediately,** el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) no se establece hasta que se intenta acceder al conjunto de objetos devuelto. Sin embargo, si usa la marca **wbemFlagReturnWhenComplete,** el objeto Err se establece cuando se llama al método **ExecQuery.**

Hay límites en el número de palabras clave **AND** y **OR** que se pueden usar en consultas WQL. Un gran número de palabras clave WQL que se usan en una consulta compleja puede hacer que WMI devuelva el código de error **WBEM \_ E QUOTA \_ \_ VIOLATION** como **un valor HRESULT.** El límite de palabras clave de WQL depende de lo compleja que sea la consulta.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se localizan todas las unidades de disco en el equipo local y se muestra el identificador de dispositivo y el tipo de la unidad de disco.


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> <dt>

[Consulta con WQL](querying-with-wql.md)
</dt> <dt>

[Crear un script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Enumeración de WMI](enumerating-wmi.md)
</dt> </dl>

 

