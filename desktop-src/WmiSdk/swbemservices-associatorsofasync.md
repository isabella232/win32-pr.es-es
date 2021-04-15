---
description: Devuelve una colección de objetos (clases o instancias) denominada puntos de conexión que están asociados a un objeto especificado.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Método SWbemServices. AssociatorsOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83f2eb33b7cd2d6ce6345d9b40a2367539dfec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715722"
---
# <a name="swbemservicesassociatorsofasync-method"></a>SWbemServices. AssociatorsOfAsync, método

El método **AssociatorsOfAsync** del objeto [**SWbemServices**](swbemservices.md) devuelve una colección de objetos (clases o instancias) denominados extremos que están asociados a un objeto especificado. La llamada a **AssociatorsOfAsync** se devuelve inmediatamente, y los resultados y el estado se devuelven al autor de la llamada a través de los eventos entregados al receptor especificado en *objWbemSink*. Para controlar cada objeto devuelto, cree un *objWbemSink*. Controlador de eventos [**OnObjectReady**](swbemsink-onobjectready.md) .

Después de que lleguen todos los objetos, el procesamiento se realiza en *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) . Este método realiza la misma función que realizan los asociados de la consulta WQL. Para obtener más información acerca de la creación de un receptor, consulte [recibir un evento WMI](receiving-a-wmi-event.md).

Se llama al método en el modo asincrónico. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
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
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obligatorio. Receptor de objeto que recibe los objetos de forma asincrónica. Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obligatorio. Cadena que contiene la ruta de acceso del objeto de la clase o instancia de origen. Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strAssocClass* \[ opta\]
</dt> <dd>

Cadena que contiene una clase de asociación. Cuando se especifica, este parámetro indica que los extremos devueltos deben estar asociados al origen a través de la clase de asociación especificada o una clase derivada de esta clase de asociación.

</dd> <dt>

*strResultClass* \[ opta\]
</dt> <dd>

Cadena que contiene un nombre de clase. Si se especifica, este parámetro opcional indica que los extremos devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.

</dd> <dt>

*strResultRole* \[ opta\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los extremos devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*strRole* \[ opta\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los extremos devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado. El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.

</dd> <dt>

*bClassesOnly* \[ opta\]
</dt> <dd>

Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases. Estas son las clases a las que pertenecen las instancias de extremo. El valor predeterminado de este parámetro es **false**.

</dd> <dt>

*bSchemaOnly* \[ opta\]
</dt> <dd>

Valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos. El valor predeterminado de este parámetro es **false**. Solo se puede establecer en **true** si el parámetro *strObjectPath* especifica la ruta de acceso del objeto de una clase. Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.

</dd> <dt>

*strRequiredAssocQualifier* \[ opta\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los extremos devueltos deben asociarse con el objeto de origen a través de una clase de asociación que incluye el calificador especificado.

</dd> <dt>

*strRequiredQualifier* \[ opta\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los extremos devueltos deben incluir el calificador especificado.

</dd> <dt>

*iFlags* \[ opta\]
</dt> <dd>

Entero que especifica las marcas adicionales para la operación. El valor predeterminado para este parámetro es **wbemFlagDontSendStatus**. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0X0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Hace que WMI devuelva datos de modificación de clase junto con la definición de clase base. Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ opta\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ opta\]
</dt> <dd>

Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obtener más información, consulte [llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia. Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Códigos de error

Después de completar el método **AssociatorsOfAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

No se encontró el elemento solicitado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta llamada se devuelve inmediatamente. Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*. Para procesar cada objeto cuando vuelva, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) . Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

Use el parámetro *objWbemAsyncContext* en scripts para comprobar el origen de una llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.AssociatorsAsync\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**SWbemObject. References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemObject.ReferencesAsync\_**](swbemobject-referencesasync-.md)
</dt> <dt>

[**SWbemServices. References**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

