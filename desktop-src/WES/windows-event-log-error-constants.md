---
title: Windows Constantes de error del registro de eventos (WinError.h)
description: Estos son los códigos de error que define Windows registro de eventos.
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f6f0bd3e2805c02dad78c064b56a443bfbb596cf42f25e9b52ac7ba584f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031945"
---
# <a name="windows-event-log-error-constants"></a>Windows Constantes de error del registro de eventos

Estos son los códigos de error que define Windows registro de eventos.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR \_ EVT \_ RUTA DE ACCESO DE CANAL NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



La ruta de acceso del canal especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR \_ EVT \_ INVALID \_ QUERY**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



La consulta especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR \_ NO SE ENCONTRARON \_ \_ METADATOS DEL \_ PUBLICADOR EVT \_**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Los metadatos del proveedor no se pueden encontrar en el recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**NO SE \_ ENCONTRÓ LA PLANTILLA DE EVENTO \_ EVT DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



La plantilla de una definición de evento no se encuentra en el recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR \_ EVT \_ INVALID \_ PUBLISHER \_ NAME**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



El nombre de proveedor especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR \_ EVT \_ INVALID \_ EVENT \_ DATA**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



Los datos de evento que genera el proveedor no son compatibles con la definición de la plantilla de evento en el manifiesto del proveedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**NO \_ SE ENCONTRÓ EL CANAL \_ EVT DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



No se encuentra el canal especificado. Compruebe la configuración del canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR \_ EVT \_ MALFORMED \_ XML \_ TEXT**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



El texto XML especificado no tenía el formato correcto. Para obtener más información, llame [**a la función EvtGetExtendedStatus.**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus)


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR \_ DE SUSCRIPCIÓN DE EVT AL CANAL \_ \_ \_ \_ DIRECTO**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



No puede suscribirse a un canal analítico o de depuración; los eventos de un canal analítico o de depuración van directamente a un archivo de registro y no se pueden suscribir.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR \_ DE CONFIGURACIÓN DE EVT \_ \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Error en la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR \_ EVT \_ QUERY \_ RESULT \_ STALE**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



El resultado de la consulta no es válido. Esto puede deberse a que el registro se borra o se redova después de crear el resultado de la consulta. Libere el objeto de resultado de la consulta y vuelva a emitir la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR \_ EVT \_ QUERY \_ RESULT \_ INVALID \_ POSITION**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



El cursor del resultado de la consulta no apunta a una posición válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR \_ EVT \_ NON \_ VALIDATING \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



El analizador MSXML registrado no admite la validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR \_ EVT \_ FILTER \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Una expresión puede ir seguida de un cambio de operación de ámbito solo si la expresión se evalúa como un conjunto de nodos y aún no forma parte de algún otro cambio de operación de ámbito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR \_ EVT \_ FILTER \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



No se puede realizar una operación de paso a partir de un término que no representa un conjunto de elementos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR \_ EVT \_ FILTER \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Los argumentos del lado izquierdo de un operador binario deben ser atributos, nodos o variables, y los argumentos del lado derecho deben ser constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR \_ EVT \_ FILTER \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Una operación de paso debe implicar una prueba de nodo o, en el caso de un predicado, se puede evaluar una expresión algebraica con la que probar cada nodo del conjunto de nodos identificado por el conjunto de nodos anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR \_ EVT \_ FILTER \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Este tipo de datos no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR \_ EVT \_ FILTER \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



Error de sintaxis en la posición especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR \_ EVT \_ FILTER \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Esta implementación del filtro no admite este operador.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR \_ EVT \_ FILTER \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



El token encontrado fue inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR \_ EVT \_ INVALID \_ OPERATION \_ OVER \_ ENABLED \_ DIRECT \_ CHANNEL**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



La operación solicitada no se puede realizar a través de un canal analítico o de depuración habilitado. Debe deshabilitar el canal antes de realizar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR \_ EVT \_ INVALID \_ CHANNEL \_ PROPERTY \_ VALUE**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



La propiedad channel contiene un valor que no es válido. El tipo del valor puede no ser válido, el valor puede estar fuera del intervalo o el valor no se puede actualizar o no se admite para este tipo de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR \_ EVT \_ INVALID \_ PUBLISHER \_ PROPERTY \_ VALUE**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



La propiedad provider contiene un valor que no es válido. El tipo del valor puede no ser válido, el valor puede estar fuera del intervalo o el valor no se puede actualizar o no se admite para este tipo de proveedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR \_ EL CANAL EVT NO SE \_ PUEDE \_ \_ ACTIVAR**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



No se pudo activar el canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR \_ EVT FILTER TOO COMPLEX (FILTRO EVT \_ DE ERROR DEMASIADO \_ \_ COMPLEJO)**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



La expresión XPath superó la complejidad admitida. Simplifique la expresión o divida en dos o más expresiones simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**MENSAJE \_ EVT \_ DE ERROR NO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



El recurso de mensaje está presente, pero el mensaje no se encuentra en la tabla de cadenas o mensajes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR \_ EVT \_ MESSAGE \_ ID \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



No se encuentra el identificador del mensaje.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR \_ EVT \_ UNRESOLVED \_ VALUE \_ INSERT**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



No se encuentra la cadena de sustitución para el índice de inserción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR \_ EVT \_ UNRESOLVED \_ PARAMETER \_ INSERT**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



No se encuentra la cadena de descripción para la referencia de parámetros (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR \_ EVT \_ MAX \_ INSERTS \_ REACHED**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



Se ha alcanzado el número máximo de reemplazos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA \_ DEFINICIÓN DEL EVENTO \_ \_ \_ EVT**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



No se puede encontrar la definición de evento para el identificador de evento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR \_ EVT \_ MESSAGE \_ LOCALE \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



El recurso específico de la configuración regional para el mensaje deseado no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR \_ EVT \_ VERSION \_ TOO \_ OLD**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



El recurso es demasiado antiguo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR \_ EVT \_ VERSION \_ TOO \_ NEW**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



El recurso es demasiado nuevo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR \_ EVT \_ NO PUEDE ABRIR EL CANAL DE \_ \_ \_ \_ CONSULTA**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



No se puede abrir el canal en el índice especificado de la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR \_ EVT \_ PUBLISHER \_ DISABLED**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



El proveedor se ha deshabilitado y sus recursos no están disponibles. Esto puede ocurrir cuando se desinstala o actualiza el proveedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR \_ EVT \_ FILTER \_ OUT \_ OF \_ RANGE**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Se intentó crear un tipo numérico que está fuera de su intervalo válido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



 

 





