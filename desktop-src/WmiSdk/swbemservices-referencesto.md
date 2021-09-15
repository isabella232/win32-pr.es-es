---
description: Devuelve una colección de todas las clases o instancias de asociación que hacen referencia a una clase o instancia de origen específica.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: Método SWbemServices.ReferencesTo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465596"
---
# <a name="swbemservicesreferencesto-method"></a>Método SWbemServices.ReferencesTo

El **método ReferencesTo** del objeto [**SWbemServices**](swbemservices.md) devuelve una colección de todas las clases o instancias de asociación que hacen referencia a una clase o instancia de origen específica. Este método realiza la misma función que realiza [la consulta REFERENCES OF](references-of-statement.md) WQL.

Se llama a este método en el modo semisincronoso. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Necesario. Cadena que contiene la ruta de acceso del objeto del origen para este método. Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strResultClass* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de clase. Si se especifica, este parámetro indica que los objetos de asociación devueltos deben pertenecer a o derivarse de la clase especificada en este parámetro.

</dd> <dt>

*strRole* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los objetos de asociación devueltos deben limitarse a aquellos en los que el objeto de origen desempeña un rol específico. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*bClassesOnly* \[ Opcional\]
</dt> <dd>

Valor booleano que indica si se debe devolver o no una lista de nombres de clase en lugar de instancias reales de las clases. Estas son las clases a las que pertenecen los objetos de asociación. El valor predeterminado de este parámetro es **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Opcional\]
</dt> <dd>

Valor booleano que indica si la consulta se aplica o no al esquema en lugar de a los datos. El valor predeterminado de este parámetro es **FALSE.** Solo se puede establecer en **TRUE si** el *parámetro strObjectPath* especifica la ruta de acceso del objeto de una clase. Cuando se establece en **TRUE**, el conjunto de puntos de conexión devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.

</dd> <dt>

*strRequiredQualifier* \[ Opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los objetos de asociación devueltos deben incluir el calificador especificado.

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Entero que especifica marcas adicionales para la operación. El valor predeterminado de este parámetro es **wbemFlagReturnImmediately**, que dirige a la llamada a que se devuelva inmediatamente en lugar de esperar hasta que se haya completado la consulta. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly** (32 (0x20))


</dt> <dd>

Hace que se devuelva un enumerador de solo avance. Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional** (0 (0x0))


</dt> <dd>

Hace Windows Management Instrumentation (WMI) conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.

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

Hace que WMI devuelva datos de modificación de clase junto con la definición de clase base. Para obtener más información, vea [Localización de información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el método devuelve un [**objeto SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ReferencesTo,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

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

**wbemFlagUseAmendedQualifiers:** 131072 (0x20000)
</dt> <dd>

Hace que WMI devuelva datos de modificación de clase con la definición de clase base.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las referencias de consulta WQL asociada, instancias de origen y objetos de asociación, vea [LA INSTRUCCIÓN ASSOCIATORS OF](associators-of-statement.md).

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

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> </dl>

 

 




