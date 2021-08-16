---
description: El método AssociatorsAsync de SWbemObject obtiene objetos (clases o \_ instancias) asociados al objeto actual. Estos objetos se denominan puntos de conexión. Este método realiza la misma función que la consulta ASSOCIATORS OF WQL.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: SWbemObject.AssociatorsAsync_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b0a8cb6a3bf5099821e50e85699b1327462ee12ef6af10e3ebc3cc9fe0bf7f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314113"
---
# <a name="swbemobjectassociatorsasync_-method"></a>Método SWbemObject.AssociatorsAsync \_

El **método AssociatorsAsync \_** de [**SWbemObject**](swbemobject.md) obtiene objetos (clases o instancias) asociados al objeto actual. Estos objetos se denominan puntos de conexión. Este método realiza la misma función que la consulta ASSOCIATORS OF WQL.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemSink* \[ En\]
</dt> <dd>

Obligatorio. Receptor de objetos que recibe los objetos de forma asincrónica como devolución de llamada.

</dd> <dt>

*strAssocClass* \[ en, opcional\]
</dt> <dd>

Cadena que contiene una clase de asociación. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben estar asociados al origen a través de la clase de asociación especificada o una clase derivada de esta clase de asociación.

</dd> <dt>

*strResultClass* \[ en, opcional\]
</dt> <dd>

Cadena que contiene un nombre de clase. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben pertenecer a o derivarse de la clase especificada en este parámetro.

</dd> <dt>

*strResultRole* \[ en, opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*strRole* \[ en, opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*bClassesOnly* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases. Estas son las clases a las que pertenecen las instancias de punto de conexión. El valor predeterminado de este parámetro es **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos. El valor predeterminado de este parámetro es **FALSE.** Solo se puede establecer en **TRUE** si el objeto en el que se invoca este método es una clase. Cuando se establece en **TRUE,** el conjunto de puntos de conexión devueltos representa clases que están asociadas adecuadamente a la clase de origen en el esquema.

</dd> <dt>

*strRequiredAssocQualifier* \[ en, opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben asociarse al objeto de origen a través de una clase de asociación que incluya el calificador especificado.

</dd> <dt>

*strRequiredQualifier* \[ en, opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los puntos de conexión devueltos deben incluir el calificador especificado.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Entero que especifica marcas adicionales a la operación. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink.OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI devuelva las descripciones de propiedad y clase localizadas. Para obtener más información, vea [Localizing WMI Class Information](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ en, opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ en, opcional\]
</dt> <dd>

Se trata de [**un objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obtener más información, vea [Llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si se realiza correctamente, el receptor recibe un [**evento OnObjectReady**](swbemsink-onobjectready.md) por instancia. Después de la última instancia, el receptor del objeto recibe [**un evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Códigos de error

Después de completar el **método AssociatorsAsync, \_** el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.

</dd> <dt>

**wbemErrFailed:** 2147449889 (0x7FFF7C21)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta llamada se devuelve inmediatamente. Los objetos y el estado solicitados se devuelven al autor de la llamada a través de las llamadas devueltas al receptor que se especifica en *objWbemSink*. Para procesar cada objeto cuando llegue, cree *un objeto objWbemSink*. Subrutina de eventos [**OnObjectReady.**](swbemsink-onobjectready.md) Una vez devueltos todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Una devolución de llamada asincrónica permite a un usuario no autenticado proporcionar datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, use la comunicación semisincronosa o la comunicación sincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener más información sobre las consultas asociadas de WQL ASSOCIATORS OF, las instancias de origen y los puntos de conexión, vea [ASSOCIATORS OF (Instrucción](associators-of-statement.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

