---
description: 'Método SWbemServices.AssociatorsOf: devuelve una colección de objetos (clases o instancias) denominados extremos asociados a un objeto especificado.'
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: Método SWbemServices.AssociatorsOf (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b04c70cca8da8527d0d9f19ec872c35ec2ee610e3b0e98d88fbffbbfd3d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794405"
---
# <a name="swbemservicesassociatorsof-method"></a>Método SWbemServices.AssociatorsOf

El **método AssociatorsOf** del objeto [**SWbemServices**](swbemservices.md) devuelve una colección de objetos (clases o instancias) denominados extremos asociados a un objeto especificado. Este método realiza la misma función que la consulta ASSOCIATORS OF WQL.

De forma predeterminada, se llama a este método en modo semisincronoso. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObjectSet = .AssociatorsOf( _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatorio. Cadena que contiene la ruta de acceso del objeto de la clase o instancia de origen. Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strAssocClass* \[ Opcional\]
</dt> <dd>

Cadena que contiene una clase de asociación. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben estar asociados al origen a través de la clase de asociación especificada o de una clase derivada de esta clase de asociación.

</dd> <dt>

*strResultClass* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de clase. Si se especifica, este parámetro opcional indica que los puntos de conexión devueltos deben pertenecer a o derivarse de la clase especificada en este parámetro.

</dd> <dt>

*strResultRole* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*strRole* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*bClassesOnly* \[ Opcional\]
</dt> <dd>

Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases. Estas son las clases a las que pertenecen las instancias de punto de conexión. El valor predeterminado de este parámetro es **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Opcional\]
</dt> <dd>

Valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos. El valor predeterminado de este parámetro es **FALSE.** Solo se puede establecer en **TRUE si** el *parámetro strObjectPath* especifica la ruta de acceso del objeto de una clase. Cuando se establece en **TRUE,** el conjunto de puntos de conexión devueltos representa clases que están asociadas adecuadamente a la clase de origen en el esquema.

</dd> <dt>

*strRequiredAssocQualifier* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben asociarse al objeto de origen a través de una clase de asociación que incluya el calificador especificado.

</dd> <dt>

*strRequiredQualifier* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben incluir el calificador especificado.

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Entero que especifica marcas adicionales para la operación. El valor predeterminado de este parámetro es **wbemFlagReturnImmediately**, que llama al método en modo semisincronoso. Este parámetro puede aceptar los valores siguientes.

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

Hace que esta llamada se bloquee hasta que se haya completado la consulta. Esta marca llama al método en modo sincrónico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI devuelva datos de modificación de clase junto con la definición de clase base. Para obtener más información, vea [Localizing WMI Class Information](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Códigos de error

Después de completar el **método AssociatorsOf,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

> [!Note]  
> Una colección devuelta con cero elementos no es un error.

 

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> <dt>

**wbemErrNotFound:** 2147749890 (0x80041002)
</dt> <dd>

No se encontró el elemento solicitado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El método recupera las instancias de recursos administrados que están asociados a un recurso especificado a través de una o varias clases de asociación. Proporcione la ruta de acceso del objeto para el punto de conexión de origen y AssociatorsOf devuelve los recursos administrados en el extremo opuesto. El método AssociatorsOf realiza la misma función que la consulta ASSOCIATORS OF WQL.

Para obtener más información sobre la consulta ASSOCIATORS OF WQL, las instancias de origen y los puntos de conexión, vea [la instrucción ASSOCIATORS OF](associators-of-statement.md).

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

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.AssociatorsAsync\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




