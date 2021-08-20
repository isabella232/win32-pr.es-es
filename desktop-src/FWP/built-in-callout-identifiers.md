---
title: Identificadores de llamada integrados (Fwpmu.h)
description: Los identificadores de las funciones de llamada integradas en Windows Filtering Platform (WFP) se representan mediante un GUID. Estos identificadores se definen de la manera siguiente.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d430f44e6e72f575d5e2ff0fd30681c04e81892f0438f0508be994d53c1643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151431"
---
# <a name="built-in-callout-identifiers"></a>Identificadores de llamada integrados

Los identificadores de las funciones de llamada integradas en Windows Filtering Platform (WFP) se representan mediante un GUID. Estos identificadores se definen de la manera siguiente.

Los sufijos V4 y V6 al final de los identificadores de llamada indican si la llamada es para la pila de red IPv4 o para la pila de red IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC INBOUND TRANSPORT \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad del modo de transporte llega de forma segura.

Esta llamada es aplicable en la capa de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC OUTBOUND TRANSPORT \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec el tráfico saliente que debe protegerse a través de asociaciones de seguridad en modo de transporte.

Esta llamada es aplicable en la capa de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TUNNEL \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC INBOUND TUNNEL \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad del modo de túnel llega de forma segura.

Esta llamada es aplicable en la capa de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TUNNEL \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC OUTBOUND TUNNEL \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec el tráfico saliente que debe protegerse a través de asociaciones de seguridad del modo de túnel.

Esta llamada es aplicable en la capa de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD INBOUND TUNNEL \_ \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC FORWARD INBOUND \_ TUNNEL \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad del modo de túnel llega de forma segura.

Esta llamada es aplicable en la capa de reenvío.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD OUTBOUND TUNNEL \_ \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC FORWARD OUTBOUND \_ TUNNEL \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Indica a IPsec el tráfico saliente que debe protegerse a través de una asociación de seguridad del modo de túnel.

Esta llamada es aplicable en la capa de reenvío.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND INITIATE SECURE \_ \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC INBOUND INITIATE \_ SECURE \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Comprueba que todas las conexiones entrantes que se supone que llegan de forma segura llegan de forma segura.

Esta llamada es aplicable en la capa de aceptación de ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TUNNEL \_ \_ ALE ACCEPT \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC INBOUND TUNNEL \_ \_ \_ ALE ACCEPT \_ \_ V6**
</dt> <dd> <dl> <dt>



Permite los paquetes IP en IP en modo de túnel IPsec cuando se clasifican en la capa de aceptación de ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ ALE \_ CONNECT \_ V4 /FWPM \_ CALLOUT \_ IPSEC \_ ALE CONNECT \_ \_ V6**
</dt> <dd> <dl> <dt>



Aplica modificadores de directiva IPsec a las aplicaciones cliente.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ DOSP \_ FORWARD \_ V4 /FWPM \_ CALLOUT \_ IPSEC \_ DOSP FORWARD \_ \_ V6**
</dt> <dd> <dl> <dt>



Indica a IPsec DoS Protection que el tráfico debe comprobarse en busca de posibles doS y puede que tenga que limitarse la velocidad.

> [!Note]  
> Disponible solo en Windows 7 y Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ CALLOUT \_ WFP \_ TRANSPORT LAYER \_ \_ V4 SILENT DROP \_ \_ /FWPM \_ CALLOUT \_ WFP TRANSPORT LAYER \_ \_ \_ V6 SILENT \_ \_ DROP**
</dt> <dd> <dl> <dt>



Implementa el filtrado en modo silencioso mediante la colocación silenciosa de todos los paquetes entrantes para los que TCP no tiene un punto de conexión de escucha.

Esta llamada es aplicable en la capa de descarte de transporte de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP CHIMNEY CONNECT LAYER \_ \_ \_ \_ V4 /FWPM \_ CALLOUT TCP CHIMNEY CONNECT \_ LAYER \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Habilita o deshabilita la descarga tcp-in-tcp para cada conexión saliente.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP CHIMNEY ACCEPT LAYER \_ \_ \_ \_ V4 /FWPM \_ CALLOUT TCP CHIMNEY ACCEPT \_ LAYER \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Habilita o deshabilita la descarga tcp-in-chimney para cada conexión entrante.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**OPCIONES DEL CONJUNTO DE LLAMADAS DE FWPM \_ \_ \_ \_ AUTH \_ CONNECT LAYER \_ \_ V4 /FWPM \_ CALLOUT SET OPTIONS \_ \_ \_ AUTH CONNECT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Establece las opciones de clasificación en los flujos de salida.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH \_ RECV ACCEPT LAYER \_ \_ \_ V4 /FWPM \_ CALLOUT SET OPTIONS \_ \_ \_ AUTH \_ RECV ACCEPT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Establece las opciones de clasificación en los flujos de entrada.

> [!Note]  
> Disponible solo en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ RESERVED \_ AUTH CONNECT LAYER \_ \_ \_ V4 /FWPM \_ CALLOUT RESERVED \_ \_ AUTH CONNECT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Este identificador está reservado para uso interno.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE LISTEN \_ \_ V6 /FWPM \_ CALLOUT \_ TEREDO \_ ALE LISTEN \_ \_ V6**
</dt> <dd> <dl> <dt>



Indica al servicio Teredo que una aplicación requiere una dirección Teredo.

> [!Note]  
> Para Windows 7 y versiones posteriores, use **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V6 /FWPM \_ CALLOUT \_ TEREDO \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Indica al servicio Teredo que una aplicación requiere una dirección Teredo.

> [!Note]  
> Para Windows 7 y versiones posteriores, use **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ RESOURCE \_ ASSIGNMENT \_ V4** 
</dt> <dd> <dl> <dt>



Este identificador está reservado para su uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V4**
</dt> <dd> <dl> <dt>



Este identificador está reservado para su uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP TEMPLATES CONNECT LAYER \_ \_ \_ \_ V4 /FWPM \_ CALLOUT TCP TEMPLATES CONNECT \_ LAYER \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Aplica la configuración de la plantilla TCP para las conexiones salientes que coincidan.

> [!Note]  
> Disponible solo en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**LAS PLANTILLAS TCP \_ DE LLAMADA \_ DE FWPM ACEPTAN LA \_ \_ CAPA \_ \_ V4/ FWPM \_ CALLOUT TCP TEMPLATES ACCEPT \_ \_ LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Aplica la configuración de la plantilla TCP para las conexiones entrantes que coincidan.

> [!Note]  
> Disponible solo en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





