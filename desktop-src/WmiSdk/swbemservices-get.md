---
description: Recupera un objeto , que es una definición de clase o una instancia de , en función de la ruta de acceso del objeto.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Método SWbemServices.Get (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d448d92cddf24e98f05cf023116e7087ad8cc3dcd310b7ccd3657571ee7650ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312664"
---
# <a name="swbemservicesget-method"></a>Método SWbemServices.Get

El **método Get** del objeto [**SWbemServices**](swbemservices.md) recupera un objeto , que es una definición de clase o una instancia de , en función de la ruta de acceso del objeto. Este método recupera solo los objetos del espacio de nombres asociado al objeto **SWbemServices** actual.

Se llama al método en modo sincrónico. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strObjectPath* \[ Opcional\]
</dt> <dd>

Cadena que contiene la ruta de acceso del objeto que se recuperará. Si este valor está vacío, el objeto vacío que se devuelve puede convertirse en una nueva clase. Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Entero que determina el comportamiento de la consulta. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI devuelva datos de modificación de clase con la definición de clase base. Para obtener más información sobre los calificadores modificados, vea [Localización de información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve [**un objeto SWbemObject**](swbemobject.md) que representa el objeto solicitado.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método Get,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para acceder al objeto.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrInvalidObjectPath:** 2147749946 (0x8004103A)
</dt> <dd>

La ruta de acceso especificada no era válida.

</dd> <dt>

**wbemErrNotFound** : 2147749890 (0x80041002)
</dt> <dd>

No se encontró el objeto solicitado.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

A diferencia [**de los métodos ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) e [**InstancesOf,**](swbemservices-instancesof.md) el método Get siempre devuelve [**un objeto SWbemObject**](swbemobject.md) que representa una instancia específica de un recurso administrado por WMI. Para obtener una instancia específica de un recurso administrado por WMI mediante el método Get, debe decir a Get que recupere la instancia pasando al método la ruta de acceso del objeto, como se muestra en el siguiente script.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



Puede usar este método para obtener objetos [*singleton,*](gloss-s.md) como [**\_ \_ CIMOMIdentification**](--cimomidentification.md), que contiene información de versión sobre la instalación de WMI que se está ejecutando.

Puede examinar el repositorio con una herramienta de visualización como [CIM Studio](further-information.md) para comprobar que aparecen la nueva clase y la instancia. Para obtener un ejemplo de cómo quitar una clase y una instancia del repositorio, vea [**SWbemServices.Delete**](swbemservices-delete.md) o [**SWbemObject.Delete. \_**](swbemobject-delete-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




