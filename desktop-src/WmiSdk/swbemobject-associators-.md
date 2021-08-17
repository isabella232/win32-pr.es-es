---
description: El método Associators del objeto SWbemObject devuelve una colección de objetos (clases o instancias) que están \_ asociados al objeto actual.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: SWbemObject.Associators_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 87458cec77a6b003a6dd35d0fc0f1a39fb785522401b46fa50a515f869760889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857435"
---
# <a name="swbemobjectassociators_-method"></a>Método SWbemObject.Associators \_

El **método \_ Associators** del objeto [**SWbemObject**](swbemobject.md) devuelve una colección de objetos (clases o instancias) que están asociados al objeto actual. Estos objetos devueltos se denominan puntos de conexión. Este método realiza la misma función que realiza la consulta ASSOCIATORS OF WQL.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObjectSet = .Associators_( _
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

*strAssocClass* \[ in, opcional\]
</dt> <dd>

Cadena que contiene una clase de asociación. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben asociarse con el origen a través de la clase de asociación especificada o una clase derivada de esta clase de asociación.

</dd> <dt>

*strResultClass* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de clase. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben pertenecer a o derivarse de la clase especificada en este parámetro.

</dd> <dt>

*strResultRole* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*strRole* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*bClassesOnly* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases. Estas son las clases a las que pertenecen las instancias de punto de conexión. El valor predeterminado de este parámetro es **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ in, opcional\]
</dt> <dd>

Se trata de un valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos. El valor predeterminado de este parámetro es **FALSE.** Solo se puede establecer en **TRUE** si el objeto en el que se invoca este método es una clase . Cuando se establece en **TRUE**, el conjunto de puntos de conexión devueltos representa clases que están asociadas adecuadamente a la clase de origen en el esquema.

</dd> <dt>

*strRequiredAssocQualifier* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Este parámetro, si se especifica, indica que los puntos de conexión devueltos deben estar asociados al objeto de origen a través de una clase de asociación que incluye el calificador especificado.

</dd> <dt>

*strRequiredQualifier* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Este parámetro, si se especifica, indica que los puntos de conexión devueltos deben incluir el calificador especificado.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Entero que especifica marcas adicionales a la operación. El valor predeterminado de este parámetro es **wbemFlagReturnImmediately**, que dirige a la llamada a que se devuelva inmediatamente en lugar de esperar hasta que se haya completado la consulta. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly** (32 (0x20))


</dt> <dd>

Hace que se devuelva un enumerador de solo avance. Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional** (0 (0x0))


</dt> <dd>

Hace que WMI conserve punteros a objetos de la enumeración hasta que el cliente libera el enumerador.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Hace que la llamada se devuelva inmediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Hace que esta llamada se bloquee hasta que se haya completado la consulta.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI devuelva datos de modificación de clase con la definición de clase base. La inclusión de esta marca hace que el texto del calificador de descripción localizada esté disponible para clases, propiedades y métodos. Para obtener más información sobre los calificadores modificados, vea [Localización de información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Códigos de error

Después de completar el **método \_ Associators,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

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

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory** : 2147749894
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener más información sobre la consulta, las instancias de origen y los puntos de conexión asociados de ASSOCIATORS OF, vea [INSTRUCCIÓN ASSOCIATORS OF](associators-of-statement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




