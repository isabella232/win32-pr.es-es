---
description: La \_ clase de error CIM contiene información sobre el error de una operación CIM.
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: CIM_Error (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360128"
---
# <a name="cim_error-class"></a>CIM ( \_ clase de error)

La clase de **\_ error CIM** contiene información sobre el error de una operación CIM.

## <a name="syntax"></a>Sintaxis

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a>Miembros

La clase de **\_ error CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ error CIM** tiene estas propiedades.

<dl> <dt>

**CIMStatusCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. ERROR de DMTF \| . CÓDIGO \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**CIMStatusCodeDescription**")
</dt> </dl>

El código de estado de CIM que caracteriza esta instancia. Esta propiedad define los códigos de estado que puede devolver un servidor CIM o un agente de escucha.

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_ \_Error de Err** (1)


</dt> <dd>

Se produjo un error general que no está incluido en un código de error más específico.

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_ ERROR de \_ acceso \_ denegado** (2)


</dt> <dd>

El acceso a un recurso CIM no estaba disponible para el cliente.

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_ ERROR \_ de \_ espacio de nombres no válido** (3)


</dt> <dd>

El espacio de nombres de destino no existe.

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_ ERROR \_ de \_ parámetro no válido** (4)


</dt> <dd>

Uno o varios valores de parámetro pasados al método no eran válidos.

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_ ERR \_ ( \_ clase no válida** ) (5)


</dt> <dd>

La clase especificada no existe.

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ \_No \_ se encontró el error** (6)


</dt> <dd>

No se encontró el objeto solicitado.

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ \_No se \_ admite el error** (7)


</dt> <dd>

No se admite la operación solicitada.

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ La \_ clase Err \_ tiene \_ elementos secundarios** (8)


</dt> <dd>

No se puede realizar la operación en esta clase porque tiene instancias.

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ La \_ clase Err \_ tiene \_ instancias** (9)


</dt> <dd>

No se puede realizar la operación en esta clase porque tiene instancias.

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_ ERROR \_ de \_ superclase no válida** (10)


</dt> <dd>

No se puede realizar la operación porque la superclase especificada no existe.

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_ ERR \_ ya \_ existe** (11)


</dt> <dd>

No se puede realizar la operación porque ya existe un objeto.

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_ NO se trata de una \_ \_ \_ propiedad de este tipo** (12)


</dt> <dd>

La propiedad especificada no existe.

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_ ERROR \_ de \_ coincidencia de tipos** (13)


</dt> <dd>

El valor proporcionado no es compatible con el tipo.

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_ \_No se \_ \_ \_ admite el lenguaje de consulta de Err** (14)


</dt> <dd>

No se reconoce o no se admite el lenguaje de consulta.

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_ ERROR \_ de \_ consulta no válida** (15)


</dt> <dd>

La consulta no es válida para el lenguaje de consulta especificado.

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ \_Método Err \_ no \_ disponible** (16)


</dt> <dd>

No se pudo ejecutar el método extrínseco.

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_ \_ \_ No \_ se encontró el método Err** (17)


</dt> <dd>

El método extrínseco especificado no existe.

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_ ERROR \_ de \_ respuesta inesperada** (18)


</dt> <dd>

No se esperaba la respuesta devuelta a la operación asincrónica.

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_ ERROR \_ de \_ \_ destino de respuesta no válido** (19)


</dt> <dd>

El destino especificado para la respuesta asincrónica no es válido.

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_ El \_ espacio de nombres Err \_ no \_ está vacío** (20)


</dt> <dd>

El espacio de nombres especificado no está vacío.

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_ ERROR en el \_ \_ \_ contexto de enumeración no válido** (21)


</dt> <dd>

El contexto de enumeración proporcionado no es válido.

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_ ERROR \_ de \_ tiempo de \_ espera de operación no válida** (22)


</dt> <dd>

El espacio de nombres especificado no está vacío.

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_ Se \_ ha \_ \_ \_ abandonado la extracción de Err** (23)


</dt> <dd>

El espacio de nombres especificado no está vacío.

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_ \_ \_ No se puede \_ \_ abandonar la extracción de Err** (24)


</dt> <dd>

Error al intentar abandonar una operación de extracción.

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ \_ \_ No se \_ \_ admite la enumeración filtrada de Err** (25)


</dt> <dd>

No se admiten los Enumeratrions filtrados.

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_ \_No se \_ \_ \_ \_ admite la continuación de Err en el error** (26)


</dt> <dd>

No se admite continuar después de un error.

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ Se \_ han \_ \_ superado los límites de servidor de Err** (27)


</dt> <dd>

Se han superado los límites del servidor WBEM (por ejemplo, memoria, conexiones, etc.).

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ El \_ servidor de Err \_ se está \_ cerrando \_** (28)


</dt> <dd>

El servidor WBEM se está cerrando.

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_ \_No se \_ \_ \_ admite la característica de consulta Err** (29)


</dt> <dd>

No se admite la característica de consulta especificada.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**CIMStatusCodeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. ERROR de DMTF \| . Descripción \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**CIMStatusCode**")
</dt> </dl>

Cadena de forma libre que contiene una descripción inteligible del valor de la propiedad **CIMStatusCode** .

> [!Note]  
> Esta descripción puede extenderse, pero debe ser coherente con la definición de **CIMStatusCode**.

 

</dd> <dt>

**ErrorSource**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorSourceFormat**")
</dt> </dl>

Información que identifica la entidad que generó el error. Si el esquema CIM modela la entidad, esta propiedad contiene la ruta de acceso a la instancia codificada como un parámetro de cadena. De lo contrario, la propiedad contiene una cadena que asigna un nombre a la entidad que generó el error. El formato de esta propiedad se especifica mediante la propiedad **ErrorSourceFormat** .

</dd> <dt>

**ErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorSource**","**\_ error de CIM**.**OtherErrorSourceFormat**")
</dt> </dl>

Formato de la propiedad **ErrorSource** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Una aplicación cliente CIM no reconoce el formato o lo interpreta de forma significativa.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

El formato se define mediante el valor de la propiedad **OtherErrorSourceFormat** .

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)


</dt> <dd>

Una ruta de acceso de objeto CIM tal y como se define en la especificación de infraestructura CIM.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**OtherErrorType**")
</dt> </dl>

El tipo de error principal.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Error de comunicaciones** (2)


</dt> <dd>

Los errores de este tipo están asociados principalmente a los procedimientos y/o procesos necesarios para transmitir información de un punto a otro.

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Error de calidad de servicio** (3)


</dt> <dd>

Los errores de este tipo están asociados principalmente a errores que dan lugar a una funcionalidad o un rendimiento reducidos.

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Error de software** (4)


</dt> <dd>

Un error de este tipo está asociado principalmente a un software o un error de procesamiento.

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Error de hardware** (5)


</dt> <dd>

Los errores de este tipo están asociados principalmente a un error de hardware o de equipo.

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Error de entorno** (6)


</dt> <dd>

otras consideraciones del entorno.

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Error de seguridad** (7)


</dt> <dd>

Los errores de este tipo están asociados a infracciones de seguridad, detección de virus y problemas similares.

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Error de sobresuscripción** (8)


</dt> <dd>

Los errores de este tipo están asociados principalmente al error de asignación de recursos suficientes para completar la operación.

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Error de recurso no disponible** (9)


</dt> <dd>

Los errores de este tipo están asociados principalmente al error de acceso a un recurso necesario.

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Error de operación no compatible** (10)


</dt> <dd>

Los errores de este tipo están asociados principalmente a las solicitudes que no se admiten.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**MessageID**","**\_ error de CIM**.**MessageArguments**")
</dt> </dl>

Mensaje con formato.

> [!Note]  
> Este mensaje se crea combinando los elementos dinámicos de la propiedad **MessageArguments** con los elementos estáticos de la propiedad **MessageID** y agregándolos después a un registro de mensajes o catálogo asociado a **OwningEntity**.

 

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**MessageID**","**\_ error de CIM**.**Mensaje**")
</dt> </dl>

Una matriz que contiene el contenido dinámico del mensaje.

</dd> <dt>

**Identificador**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ error**.**Mensaje**","**\_ error de CIM**.**MessageArguments**")
</dt> </dl>

Cadena opaca que identifica de forma única, dentro del ámbito de OwningEntity, el formato del mensaje.

</dd> <dt>

**OtherErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorSourceFormat**")
</dt> </dl>

Una cadena que define el valor de **ErrorSourceFormat** cuando **ErrorSourceFormat** se establece en "1" (otro).

</dd> <dt>

**OtherErrorType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorType**")
</dt> </dl>

Cadena de forma libre que describe el valor de **ErrorType** cuando se establece en "1" (otro).

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

IDENTIFICADOR único de la entidad que posee el formato del mensaje descrito por esta instancia.

> [!Note]  
> Esta propiedad debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad de negocio o del cuerpo de los estándares que haya definido el formato de mensaje.

 

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Gravedad percibida ")
</dt> </dl>

Una descripción de la gravedad del error desde el punto de vista del elemento que envió el mensaje de error.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

la gravedad percibida de la indicación es desconocida o indeterminada.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

Indica que el valor de la gravedad se puede encontrar en la propiedad **OtherSeverity** .

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)


</dt> <dd>

La información se debe utilizar al proporcionar una respuesta informativa.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)


</dt> <dd>

Debe usarse cuando sea adecuado para permitir que el usuario decida si es necesario realizar alguna acción.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundaria** (4)


</dt> <dd>

La acción es necesaria, pero la situación no es seria en este momento.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)


</dt> <dd>

La acción es necesaria ahora.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)


</dt> <dd>

La acción es necesaria ahora y el ámbito es amplio (es posible que se produzca una interrupción inminente en un recurso crítico).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrecuperable/no recuperable** (7)


</dt> <dd>

se produjo un error, pero es demasiado tarde para tomar medidas correctivas.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Causa probable: "," recommendation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ error de CIM**.**ProbableCauseDescription**")
</dt> </dl>

Una descripción de la causa probable del error.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

**Error de tarjeta/adaptador** (2)


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

**Error del subsistema de aplicación** (3)


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

**Ancho de banda reducido** (4)


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

**Error de establecimiento de conexión** (5)


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

**Error de protocolo de comunicaciones** (6)


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

**Error del subsistema de comunicaciones** (7)


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

**Error de configuración/personalización** (8)


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

**Congestión** (9)


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

**Datos dañados** (10)


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

Se **superó el límite de ciclos de CPU** (11)


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

**Error de conjunto** de


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

**Señal degradada** (13)


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

**Error de la interfaz DTE-DCE** (14)


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

Abertura de la **puerta del gabinete** (15)


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

**Funcionamiento incorrecto del equipo** (16)


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

**Vibración excesiva** (17)


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

**Error de formato de archivo** (18)


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

**Desencadenamiento detectado** (19)


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

**Inundación detectada** (20)


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

**Error de tramas** (21)


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

**Problema de HVAC** (22)


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

**Humedad inaceptable** (23)


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

**Error de dispositivo de e/s** (24)


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

**Error de dispositivo de entrada** (25)


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

**Error de LAN** (26)


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

**Pérdida no tóxica detectada** (27)


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

**Error de transmisión del nodo local** (28)


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

**Pérdida de fotograma** (29)


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

**Pérdida de señal** (30)


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

**Suministro de material agotado** (31)


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

**Problema del multiplexor** (32)


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

**Memoria insuficiente** (33)


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

**Error de dispositivo de salida** (34)


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

**Rendimiento degradado** (35)


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

**Problema de energía** (36)


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

**Presión inaceptable** (37)


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

**Problema del procesador (error interno de la máquina)** (38)


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

**Error de bombeo** (39)


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

**Tamaño de cola superado** (40)


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

**Error de recepción** (41)


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

**Error del receptor** (42)


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

**Error de transmisión de nodo remoto** (43)


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

**Recursos a la capacidad o en proximidad** (44)


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

**Tiempo de respuesta excesivo** (45)


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

**Tasa de retransmisión excesiva** (46)


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

**Error de software** (47)


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

**Programa de software finalizado** de manera anómala (48)


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

**Error del programa de software (resultados incorrectos)** (49)


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

**Problema de capacidad de almacenamiento** (50)


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

**Temperatura inaceptable** (51)


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

**Umbral superado** (52)


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

**Problema de sincronización** (53)


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

**Pérdida tóxica detectada** (54)


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

**Error de transmisión** (55)


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

**Error de transmisor** (56)


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

**Recurso subyacente no disponible** (57)


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

**Discrepancia de versiones** (58)


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

**Alerta anterior desactivada** (59)


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

**Error de intentos de inicio de sesión** (60)


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

**Virus de software detectado** (61)


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

**Seguridad de hardware infringida** (62)


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

**Denegación de servicio detectada** (63)


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

**No coincide la credencial de seguridad** (64)


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

**Acceso no autorizado** (65)


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

**Alarma recibida** (66)


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

**Pérdida de puntero** (67)


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

Error de **coincidencia de carga** (68)


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

**Error de transmisión** (69)


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

**Tasa de errores excesiva** (70)


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

**Problema de seguimiento** (71)


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

**Elemento no disponible** (72)


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

**Falta el elemento** (73)


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

**Pérdida de varios fotogramas** (74)


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

**Error de canal de difusión** (75)


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

Se **recibió un mensaje no válido** (76)


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

**Error de enrutamiento** (77)


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

**Error de backplane** (78)


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

**Duplicación de identificadores** (79)


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

**Error de ruta de protección** (80)


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

**Pérdida o desigualdad de sincronización** (81)


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

**Problema de terminal** (82)


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

**Error de reloj en tiempo real** (83)


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

**Error de antena** (84)


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

**Error de carga** de la batería (85)


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

**Error de disco** (86)


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

**Error de salto de frecuencia** (87)


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

**Pérdida de redundancia** (88)


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

**Error** de la fuente de alimentación (89)


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

**Problema de calidad** de la señal (90)


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

**Descarga** de la batería (91)


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

**Error de batería** (92)


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

**Problema de alimentación comercial** (93)


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

**Error de ventilador** (94)


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

**Error del motor** (95)


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

**Error del sensor** (96)


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

**Error de fusible** (97)


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

**Error del generador** (98)


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

**Batería baja** (99)


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

**Combustible bajo** (100)


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

**Bajo agua** (101)


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

**Gas explosivo** (102)


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

**Viento alto** (103)


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

**Acumulación de hielo** (104)


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

**Humo** (105)


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

**No coincide la memoria** (106)


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

**Ciclos de CPU agotados** (107)


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

**Problema del entorno de software** (108)


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

**Error de descarga de software** (109)


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

**Elemento reinicializado** (110)


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

**Tiempo de espera** (111)


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

**Problemas de registro** (112)


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

**Pérdida detectada** (113)


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

**Error del mecanismo de protección** (114)


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

**Error de protección de recursos** (115)


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

Incoherencia de la **base de datos** (116)


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

**Error de autenticación** (117)


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

**Infracción de la confidencialidad** (118)


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

**Manipulación de cables** (119)


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

**Información retrasada** (120)


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

**Información duplicada** (121)


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

**Falta información** (122)


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

**Modificación** de la información (123)


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

**Información fuera de secuencia** (124)


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

**Clave expirada** (125)


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

**Error sin repudio** (126)


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

**Actividad fuera de horas** (127)


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

**Fuera de servicio** (128)


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

**Error de procedimiento** (129)


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

**Información inesperada** (130)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ProbableCause**")
</dt> </dl>

Cadena de forma libre que describe la causa probable del error, cuando la propiedad **ProbableCause** se establece en "1" (otro).

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas de formato libre que describen las acciones recomendadas que se deben realizar para resolver el error.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

