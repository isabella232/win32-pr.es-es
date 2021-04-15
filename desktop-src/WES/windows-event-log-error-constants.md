---
title: Constantes de error del registro de eventos de Windows (WinError. h)
description: A continuación se muestran los códigos de error que define el registro de eventos de Windows.
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
ms.openlocfilehash: efa5443d98c53d6abedbe3a0027e8e2e524ae9df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696024"
---
# <a name="windows-event-log-error-constants"></a>Constantes de error del registro de eventos de Windows

A continuación se muestran los códigos de error que define el registro de eventos de Windows.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR \_ evt \_ \_ ruta de acceso de canal no válida \_**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



La ruta de acceso del canal especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR \_ evt \_ consulta no válida \_**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



La consulta especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR \_ evt \_ metadatos del publicador \_ \_ no \_ encontrados**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



No se encuentran los metadatos del proveedor en el recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la plantilla de evento evt**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



No se encuentra la plantilla para una definición de evento en el recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR \_ evt \_ \_ nombre de publicador no válido \_**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



El nombre de proveedor especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR \_ evt \_ \_ datos de evento no válidos \_**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



Los datos de evento generados por el proveedor no son compatibles con la definición de la plantilla de evento en el manifiesto del proveedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR \_ : \_ \_ no \_ se encontró el canal evt**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



No se encuentra el canal especificado. Compruebe la configuración del canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR \_ evt de \_ \_ texto XML con formato incorrecto \_**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



El texto XML especificado no tiene el formato correcto. Para obtener más información, llame a la función [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) .


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR \_ \_ de suscripción \_ de EVT a \_ \_ canal directo**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



No se puede suscribir a un canal analítico o de depuración; los eventos de un canal analítico o de depuración van directamente a un archivo de registro y no se pueden suscribir.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**error \_ : \_ error de configuración de EVT \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Error en la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR \_ de \_ consulta evt \_ resultado \_ obsoleto**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



El resultado de la consulta no es válido. Esto puede deberse a que el registro se borra o se revierte una vez creado el resultado de la consulta. Libere el objeto de resultado de la consulta y vuelva a emitir la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR \_ : \_ \_ \_ posición no válida del resultado de la consulta evt \_**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



El cursor del resultado de la consulta no está señalando a una posición válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR \_ evt \_ no \_ validando \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



El analizador MSXML registrado no admite la validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR \_ evt \_ filtro \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Una expresión puede ir seguida de un cambio de operación de ámbito solo si la expresión se evalúa como un conjunto de nodos y aún no forma parte de otro cambio de operación de ámbito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR \_ evt \_ filtro \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



No se puede realizar una operación Step a partir de un término que no representa un conjunto de elementos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR \_ evt \_ filtro \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Los argumentos en el lado izquierdo de un operador binario deben ser atributos, nodos o variables, y los argumentos del lado derecho deben ser constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR \_ evt \_ filtro \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Una operación Step debe implicar una prueba de nodo o, en el caso de un predicado, una expresión algebraica en la que probar cada nodo del conjunto de nodos identificado por el conjunto de nodos anterior que se puede evaluar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR \_ evt \_ filtro \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Este tipo de datos no se admite.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR \_ evt \_ filtro \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



Se produjo un error de sintaxis en la posición especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR \_ evt \_ filtro \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Este operador no es compatible con esta implementación del filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR \_ evt \_ filtro \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



El token encontrado era inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR \_ evt \_ operación no válida \_ \_ en el \_ \_ canal directo habilitado \_**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



La operación solicitada no se puede realizar a través de un canal de depuración o analítico habilitado. Debe deshabilitar el canal antes de realizar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR \_ evt \_ \_ valor de \_ propiedad de canal no válido \_**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



La propiedad de canal contiene un valor que no es válido. El tipo del valor puede no ser válido, el valor puede estar fuera del intervalo o el valor no se puede actualizar o no se admite para este tipo de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR \_ evt \_ \_ valor de propiedad de publicador no válido \_ \_**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



La propiedad de proveedor contiene un valor que no es válido. El tipo del valor no puede ser válido, el valor puede estar fuera del intervalo o el valor no se puede actualizar o no se admite para este tipo de proveedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR: el \_ \_ canal evt \_ no se puede \_ activar**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



No se pudo activar el canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR \_ : \_ filtro evt \_ demasiado \_ complejo**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



La expresión XPath superó la complejidad admitida. Simplifique la expresión o divídala en dos o más expresiones simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR \_ : \_ mensaje evt \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



El recurso de mensaje está presente, pero el mensaje no se encuentra en la cadena o la tabla de mensajes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró el identificador de mensaje evt**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



No se puede encontrar el identificador de mensaje.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR \_ evt: \_ inserción de \_ valor sin resolver \_**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



No se puede encontrar la cadena de sustitución para el índice de inserción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR \_ evt: \_ inserción de \_ parámetro sin resolver \_**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



No se encuentra la cadena de descripción de la referencia de parámetro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR \_ evt se \_ alcanzó el número máximo de \_ inserciones \_**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



Se ha alcanzado el número máximo de reemplazos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la definición del evento evt**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



No se encuentra la definición de evento para el identificador de evento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la configuración regional del mensaje evt**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



El recurso específico de la configuración regional para el mensaje deseado no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR \_ evt \_ versión \_ demasiado \_ antigua**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



El recurso es demasiado antiguo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR \_ evt \_ versión \_ demasiado \_ nueva**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



El recurso es demasiado nuevo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR \_ evt \_ no se puede \_ abrir el \_ canal \_ de la \_ consulta**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



No se puede abrir el canal situado en el índice especificado de la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR \_ evt \_ publicador \_ deshabilitado**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



El proveedor se ha deshabilitado y sus recursos no están disponibles. Esto puede ocurrir cuando el proveedor se ha desinstalado o actualizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR \_ \_ de filtro evt \_ fuera \_ del \_ intervalo**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Se intentó crear un tipo numérico que está fuera de su intervalo válido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





