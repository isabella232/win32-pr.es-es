---
title: Códigos de error de WFP (Winerror.h)
description: Códigos de error específicos de (WFP).
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491728"
---
# <a name="wfp-error-codes"></a>Códigos de error de WFP

Los códigos de error específicos de la plataforma de filtrado de Windows (WFP) son los siguientes.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_ \_ \_ no \_ se encontró el FWP E llamada**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



La llamada no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_ \_ \_ no \_ se encontró la condición de FWP E**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



La condición de filtro no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_ \_ \_ no \_ se encontró el filtro de FWP E**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



El filtro no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**\_ \_ \_ no \_ se encontró el nivel de FWP E**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



La capa no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_ \_ \_ no \_ se encontró el proveedor de FWP E**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



El proveedor no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**\_ \_ \_ \_ no se encontró el contexto \_ del proveedor de FWP E**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



El contexto del proveedor no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**\_ \_ \_ no \_ se encontró el subnivel de FWP E**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



La subcapa no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**\_ \_ no \_ se encontró el FWP E**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



El objeto no existe.

Las [funciones \* IPsecSaContext](fwp-ipsec-functions.md) devuelven este error si no se encuentra el identificador de contexto de SA.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**el FWP \_ E \_ ya \_ existe**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Ya existe un objeto con ese GUID o LUID.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ en \_ uso**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



Otros objetos hacen referencia al objeto, por lo que no se puede eliminar.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ sesión dinámica de FWP E \_ \_ en \_ curso**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



No se permite la llamada desde dentro de una sesión dinámica.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**sesión de FWP \_ E \_ incorrecta \_**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



La llamada se realizó desde una sesión incorrecta, por lo que no se puede completar.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ no \_ TXN \_ en \_ curso**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



La llamada se debe realizar desde una transacción explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ TXN \_ en \_ curso**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



No se permite la llamada desde dentro de una transacción explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ TXN \_ anulado**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



Se ha cancelado la transacción explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**se \_ \_ anuló la sesión \_ de FWP E**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



Se ha cancelado la sesión.

El identificador de sesión debe cerrarse llamando a [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), aunque ya no sea válido. de lo contrario, se filtrará el estado del lado cliente. Se debe crear una nueva sesión mediante una llamada a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**\_ \_ TXN incompatible de FWP E incompatible \_**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



No se permite la llamada desde una transacción de solo lectura.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**tiempo de espera de FWP \_ E \_**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



Se agotó el tiempo de espera de la llamada mientras se esperaba a adquirir el bloqueo de la transacción.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_eventos net de FWP E \_ \_ \_ deshabilitados**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



La colección de eventos de diagnóstico de red está deshabilitada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**nivel de FWP \_ E \_ incompatible \_**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



La capa especificada no admite la operación.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**solo clientes de FWP \_ E \_ km \_ \_**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



Solo se permite la llamada a los autores de llamadas en modo kernel.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**\_ \_ duración \_ no coincidente de FWP E**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



La llamada intentó asociar dos objetos con duraciones incompatibles.

Vea [Administración de objetos](object-management.md) para obtener más información sobre la duración de los objetos y la Asociación de objetos.


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**FWP \_ E \_ Builtin ( \_ objeto)**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



El objeto está integrado, por lo que no se puede eliminar.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ demasiadas \_ \_ llamadas**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



Se ha alcanzado el número máximo de llamadas.

Como máximo, se pueden registrar 100.000 llamadas al mismo tiempo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**se \_ \_ quitó la notificación de FWP E \_**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



No se pudo entregar una notificación porque una cola de mensajes está a su capacidad máxima.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**el \_ tráfico de FWP E \_ \_ no coincide**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



Los parámetros de tráfico de red no coinciden con los del contexto de la Asociación de seguridad.

Se puede llamar a [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) varias veces, pero el autor de la llamada debe especificar el mismo [**\_ TRAFFIC0 de IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) cada vez. Se devuelve este error si una llamada subsiguiente proporciona un **\_ TRAFFIC0 de IPSec** diferente.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**\_Estado de \_ SA incompatible de FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



La llamada no está permitida para el estado de la Asociación de seguridad (SA) actual.

Las funciones de contexto SA deben llamarse en un orden específico:

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Se devuelve este error si se llama fuera de orden.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**\_ \_ puntero nulo de FWP E \_**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Un puntero requerido es NULL.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**\_enumerador de FWP E \_ no válido \_**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Un valor de enumerador de una estructura está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**\_ \_ marcas no válidas de FWP E \_**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



El campo Flags contiene un valor no válido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**\_máscara de \_ red no válida de FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Una máscara de red no es válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**\_ \_ rango no válido de FWP E \_**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Una estructura de [**FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) no es válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**\_ \_ intervalo no válido de FWP E \_**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



El intervalo de tiempo no es válido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**\_matriz de \_ longitud de cero \_ \_ de FWP**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Una matriz que debe contener al menos un elemento tiene una longitud cero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**nombre para mostrar de FWP \_ E \_ null \_ \_**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



El campo **displayData.Name** no puede ser null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**\_tipo de \_ acción no válido de FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



El tipo de acción no es ninguno de los tipos de acción permitidos para un filtro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**\_ \_ peso no válido de FWP E \_**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



El peso del filtro no es válido.

Para obtener más información, vea [asignación de pesos de filtro](filter-weight-assignment.md) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**\_ \_ \_ no coinciden los tipos de coincidencia de FWP E \_**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Una condición de filtro contiene un tipo de coincidencia que no es compatible con los operandos.

Consulte [**\_ \_ tipo de coincidencia de FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) para obtener más información.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**error \_ de \_ coincidencia de tipo de FWP E \_**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Una estructura de [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) o una estructura VALUE0 de la [**\_ \_ condición FWPM**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) es de tipo incorrecto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E \_ fuera \_ de los \_ límites**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Un valor entero está fuera del intervalo permitido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ reservado**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Un campo reservado es distinto de cero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**\_ \_ condición duplicada de FWP E \_**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Un filtro no puede contener varias condiciones que operan en un único campo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**\_ \_ KEYMOD duplicado de FWP E \_**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Una directiva no puede contener el mismo módulo de creación de claves más de una vez.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**\_ \_ acción de FWP E \_ incompatible \_ con el \_ nivel**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



El tipo de acción no es compatible con la capa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**\_ \_ acción de FWP E \_ incompatible \_ con \_ subcapa**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



El tipo de acción no es compatible con la subcapa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**\_ \_ contexto de FWP E \_ incompatible \_ con el \_ nivel**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



El contexto sin formato o el contexto del proveedor no es compatible con la capa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**\_ \_ contexto de FWP E \_ incompatible \_ con la \_ llamada**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



El contexto sin formato o el contexto del proveedor no es compatible con la llamada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**método de autenticación de FWP \_ E \_ incompatible \_ \_**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



El método de autenticación no es compatible con el tipo de directiva.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**\_Grupo DH de FWP E \_ incompatible \_ \_**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



El grupo de Diffie-Hellman no es compatible con el tipo de directiva.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**no se admite el FWP \_ E \_ em \_ \_**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



Una directiva IKE no puede contener una directiva de modo extendido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ nunca \_ coinciden**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



La plantilla o la suscripción de enumeración nunca coincidirán con ningún objeto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**\_ \_ \_ no coincide el contexto del proveedor \_ de FWP E**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



El contexto del proveedor es de un tipo incorrecto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**\_ \_ parámetro no válido de FWP E \_**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



El parámetro no es correcto.

Causas posibles de este error:

-   Se llamó a [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) sin establecer la marca de túnel de marca **FWPM \_ \_ \_ \_ en \_ punto** y con condiciones distintas de la dirección local o remota.
-   Una cadena Unicode no válida o una cadena Unicode que contiene caracteres no imprimibles.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E \_ demasiadas \_ \_ subcapas**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



Se ha alcanzado el número máximo de subcapas.

WFP admite como máximo 2 6 subcapas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**error en la notificación de llamada de FWP \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



La función de notificación de una llamada devolvió un error.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**transformación de autenticación de FWP \_ E \_ no válida \_ \_**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



La transformación de autenticación de IPsec no es válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**\_transformación de \_ \_ cifrado de FWP E no válida \_**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



La transformación de cifrado de IPsec no es válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



 

 





