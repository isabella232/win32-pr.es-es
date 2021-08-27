---
title: Códigos de error de WFP (Winerror.h)
description: (WFP) códigos de error específicos.
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
ms.openlocfilehash: 21550e0c8872f0d0f8c067b38044a946f10f452d06ca213dea414d34756ce7ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083205"
---
# <a name="wfp-error-codes"></a>Códigos de error de WFP

Windows Los códigos de error específicos de la plataforma de filtrado (WFP) son los siguientes.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**NO SE ENCONTRÓ LA LLAMADA FWP \_ \_ \_ E \_**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



La llamada no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**NO SE \_ ENCONTRÓ LA CONDICIÓN FWP E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



La condición de filtro no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**NO SE \_ ENCONTRÓ EL FILTRO FWP \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



El filtro no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**NO SE \_ ENCONTRÓ LA CAPA DE FWP \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



La capa no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**NO SE \_ ENCONTRÓ EL \_ PROVEEDOR FWP \_ \_ E**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



El proveedor no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**NO SE ENCONTRÓ EL CONTEXTO DEL PROVEEDOR FWP \_ \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



El contexto del proveedor no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**NO SE \_ ENCONTRÓ \_ LA SUBCAPA FWP \_ E \_**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



La subcapa no existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



El objeto no existe.

Las [funciones IPsecSaContext \* ](fwp-ipsec-functions.md) devuelven este error si no se encuentra el identificador de contexto de SA.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Ya existe un objeto con ese GUID o LUID.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ EN \_ USO**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



Otros objetos hacen referencia al objeto, por lo que no se puede eliminar.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**SESIÓN DINÁMICA \_ FWP E \_ EN \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



No se permite la llamada desde dentro de una sesión dinámica.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ E \_ SESIÓN \_ INCORRECTA**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



La llamada se realizó desde una sesión incorrecta, por lo que no se puede completar.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ NO \_ TXN EN \_ \_ CURSO**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



La llamada debe realizarse desde una transacción explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ TXN EN \_ \_ CURSO**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



No se permite la llamada desde dentro de una transacción explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ TXN \_ ABORTED**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



La transacción explícita se ha cancelado forzadamente.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**SESIÓN FWP \_ E \_ \_ ANULADA**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



La sesión se ha cancelado.

El identificador de sesión debe cerrarse mediante una llamada [**a FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), aunque ya no sea válido; De lo contrario, se filtrará el estado del lado cliente. Se debe crear una nueva sesión llamando [**a FwpmEngineOpen0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP \_ E \_ INCOMPATIBLE \_ TXN**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



No se permite la llamada desde dentro de una transacción de solo lectura.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**TIEMPO DE ESPERA \_ DE FWP E \_**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



Se ha producido un tiempo de espera de la llamada mientras se esperaba adquirir el bloqueo de transacción.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**EVENTOS FWP \_ E \_ NET \_ \_ DESHABILITADOS**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



La colección de eventos de diagnóstico de red está deshabilitada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**FWP \_ E \_ CAPA INCOMPATIBLE \_**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



La capa especificada no admite la operación.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**SOLO CLIENTES \_ FWP E \_ KM \_ \_**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



La llamada solo se permite para los autores de llamadas en modo kernel.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**FWP \_ E \_ LIFETIME \_ MISMATCH**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



La llamada intentó asociar dos objetos a duraciones incompatibles.

Vea [Administración de objetos para](object-management.md) obtener más información sobre la duración de los objetos y la asociación de objetos.


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**FWP \_ E \_ BUILTIN \_ (OBJETO)**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



El objeto está integrado, por lo que no se puede eliminar.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ \_ DEMASIADAS \_ LLAMADAS**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



Se ha alcanzado el número máximo de llamadas.

Como máximo, se pueden registrar 100 000 llamadas al mismo tiempo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**NOTIFICACIÓN FWP \_ E \_ \_ DESCARTADA**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



No se pudo entregar una notificación porque una cola de mensajes está en su capacidad máxima.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**ERROR DE COINCIDENCIA DE TRÁFICO DE FWP \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



Los parámetros de tráfico de red no coinciden con los del contexto de asociación de seguridad.

[**Se puede llamar a IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) varias veces, pero el autor de la llamada debe especificar el mismo [**\_ IPSEC TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) cada vez. Este error se devuelve si una llamada posterior proporciona un **\_ traffic0 de IPSEC diferente.**


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP \_ E ESTADO DE \_ SA INCOMPATIBLE \_ \_**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



No se permite la llamada para el estado de asociación de seguridad (SA) actual.

Se debe llamar a las funciones de contexto de SA en un orden específico:

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Este error se devuelve si se llaman fuera de servicio.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP \_ E \_ PUNTERO \_ NULO**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Un puntero necesario es NULL.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**ENUMERADOR FWP \_ E \_ NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Un valor de enumerador de una estructura está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP \_ E MARCAS NO \_ \_ VÁLIDAS**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



El campo flags contiene un valor no válido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E \_ INVALID \_ NET \_ MASK**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Una máscara de red no es válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E INTERVALO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Una [**estructura \_ RANGE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) no es válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E \_ INVALID \_ INTERVAL**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



El intervalo de tiempo no es válido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP \_ E \_ MATRIZ DE LONGITUD \_ \_ CERO**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Una matriz que debe contener al menos un elemento tiene una longitud cero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP \_ E \_ NULL \_ DISPLAY \_ NAME**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



El **displayData.name** campo no puede ser NULL.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E TIPO DE ACCIÓN NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



El tipo de acción no es uno de los tipos de acción permitidos para un filtro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E PESO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



El grosor del filtro no es válido.

Consulte [Asignación de peso de filtro](filter-weight-assignment.md) para obtener más información.


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**FWP \_ E \_ MATCH \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Una condición de filtro contiene un tipo de coincidencia que no es compatible con los operandos.

Vea [**FWP \_ MATCH TYPE \_ (TIPO DE COINCIDENCIA DE FWP)**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) para obtener más información.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**FWP \_ E \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Una [**estructura \_ FWP VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) o una estructura [**\_ FWPM CONDITION \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) es del tipo incorrecto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E FUERA DE \_ \_ \_ LÍMITES**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Un valor entero está fuera del intervalo permitido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ RESERVED**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Un campo reservado es distinto de cero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP \_ E \_ DUPLICATE \_ CONDITION**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Un filtro no puede contener varias condiciones que funcionan en un solo campo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP \_ E \_ DUPLICATE \_ KEYMOD**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Una directiva no puede contener el mismo módulo de claves más de una vez.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**ACCIÓN FWP \_ E \_ INCOMPATIBLE CON \_ \_ \_ LAYER**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



El tipo de acción no es compatible con la capa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**ACCIÓN FWP \_ E \_ INCOMPATIBLE CON \_ \_ \_ SUBCAPA**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



El tipo de acción no es compatible con la subcapa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**FWP \_ E \_ CONTEXT \_ INCOMPATIBLE \_ WITH \_ LAYER**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



El contexto sin formato o el contexto del proveedor no es compatible con la capa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**FWP \_ E \_ CONTEXT \_ INCOMPATIBLE \_ WITH \_ CALLOUT**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



El contexto sin formato o el contexto del proveedor no es compatible con la llamada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP \_ E MÉTODO DE \_ \_ AUTENTICACIÓN INCOMPATIBLE \_**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



El método de autenticación no es compatible con el tipo de directiva.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E GRUPO \_ DH INCOMPATIBLE \_ \_**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



El Diffie-Hellman no es compatible con el tipo de directiva.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP \_ E EM NO SE \_ \_ \_ ADMITE**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



Una directiva de IKE no puede contener una directiva de modo extendido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ NEVER \_ MATCH**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



La plantilla de enumeración o la suscripción nunca coincidirán con ningún objeto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**ERROR DE COINCIDENCIA \_ DEL CONTEXTO \_ DEL \_ PROVEEDOR \_ FWP E**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



El contexto del proveedor es del tipo incorrecto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP \_ E PARÁMETRO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



El parámetro no es correcto.

Posibles motivos de este error:

-   [**Se llamó a FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) sin establecer la marca **FWPM \_ TUNNEL FLAG POINT TO \_ \_ \_ \_ POINT** y con condiciones que no son la dirección local o remota.
-   Una cadena Unicode no válida o una cadena Unicode que contiene caracteres no imprimibles.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E \_ \_ \_ DEMASIADAS SUBCAPAS**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



Se ha alcanzado el número máximo de subcapas.

WFP admite como máximo 2 6 subcapas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**ERROR EN LA NOTIFICACIÓN DE LLAMADA DE FWP \_ \_ \_ E \_**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



La función de notificación de una llamada devolvió un error.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E TRANSFORMACIÓN DE \_ \_ AUTENTICACIÓN NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



La transformación de autenticación de IPsec no es válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E \_ INVALID \_ CIPHER \_ TRANSFORM**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



La transformación de cifrado IPsec no es válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror.h</dt> </dl> |



 

 





