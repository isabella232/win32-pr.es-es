---
title: Identificadores de llamada integrados (Fwpmu. h)
description: Los identificadores de las funciones de llamada integradas en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID. Estos identificadores se definen como se indica a continuación.
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
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997062"
---
# <a name="built-in-callout-identifiers"></a>Identificadores de llamada integrados

Los identificadores de las funciones de llamada integradas en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID. Estos identificadores se definen como se indica a continuación.

Los sufijos V4 y V6 al final de los identificadores de llamada indican si la llamada es para la pila de red IPv4 o para la pila de red IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V4/llamada de FWPM para el transporte de \_ \_ \_ entrada IPSec \_ \_ V6** 
</dt> <dd> <dl> <dt>



Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad del modo de transporte llega de forma segura.

Esta llamada es aplicable en el nivel de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V4/FWPM \_ llamada IPSec de transporte de \_ \_ salida \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec el tráfico saliente que se debe proteger a través de las asociaciones de seguridad del modo de transporte.

Esta llamada es aplicable en el nivel de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**Llamada de FWPM de \_ \_ \_ túnel entrante de IPSec \_ \_ V4/ \_ llamada FWPM \_ \_ \_ \_** 
</dt> <dd> <dl> <dt>



Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad en modo de túnel llega de forma segura.

Esta llamada es aplicable en el nivel de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**Llamada de FWPM de \_ \_ túnel de salida de IPSec \_ \_ \_ V4/FWPM \_ llamada IPSec del túnel de \_ \_ salida \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec el tráfico saliente que debe protegerse a través de las asociaciones de seguridad del modo de túnel.

Esta llamada es aplicable en el nivel de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**Llamada de FWPM de \_ \_ IPSec \_ reenviar túnel de \_ entrada \_ \_ V4/FWPM \_ \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad en modo de túnel llega de forma segura.

Esta llamada es aplicable en la capa de reenvío.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**Llamada de FWPM de \_ \_ IPSec \_ reenviar \_ túnel de salida \_ \_ V4/FWPM \_ \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Indica a IPsec el tráfico saliente que se debe proteger a través de una asociación de seguridad en modo de túnel.

Esta llamada es aplicable en la capa de reenvío.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**Llamada de FWPM \_ llamada de \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V4/FWPM \_ llamada \_ IPSec \_ entrante \_ iniciar \_ Secure \_ V6** 
</dt> <dd> <dl> <dt>



Comprueba que todas las conexiones entrantes que se supone que llegan a ser seguras llegan de forma segura.

Esta llamada es aplicable a la capa de aceptación de ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**Llamada de FWPM \_ llamada \_ Ale de \_ túnel entrante de IPSec \_ \_ \_ Accept \_ V4/FWPM \_ CALLOUT \_ IPSec \_ \_ tunelización entrante \_ \_ aceptación \_ V6**
</dt> <dd> <dl> <dt>



Permite los paquetes IP en modo de túnel de IPsec cuando se clasifican en la capa de aceptación de ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**Llamada de FWPM de \_ \_ IPSec \_ Ale de \_ conexión \_ V4/FWPM \_ llamada a \_ IPSec \_ Ale \_ Connect \_ V6**
</dt> <dd> <dl> <dt>



Aplica los modificadores de directivas IPsec a las aplicaciones cliente.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**\_Llamada FWPM \_ IPSec \_ DOSP \_ reenvío \_ V4/FWPM \_ llamada \_ IPSec \_ DOSP \_ Forward \_ V6**
</dt> <dd> <dl> <dt>



Señala a la protección de DoS de IPsec que el tráfico debe comprobarse para posibles DoS y puede que tenga que tener una velocidad limitada.

> [!Note]  
> Solo está disponible en Windows 7 y Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ llamada \_ WFP \_ nivel de transporte WFP \_ \_ V4 \_ eliminación silenciosa \_ /FWPM \_ llamada \_ WFP \_ nivel de transporte WFP \_ \_ V6 \_ eliminación silenciosa \_**
</dt> <dd> <dl> <dt>



Implementa el filtrado en modo oculto mediante la eliminación silenciosa de todos los paquetes entrantes para los que TCP no tiene un extremo de escucha.

Esta llamada es aplicable en el nivel de descartar transporte de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ Callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V4/FWPM \_ Callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Habilita o deshabilita la descarga TCP Chimney para cada conexión de salida.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ llamada \_ TCP \_ Chimney \_ aceptación \_ capa \_ V4/FWPM \_ llamada \_ TCP \_ Chimney \_ aceptación \_ capa \_ V6**
</dt> <dd> <dl> <dt>



Habilita o deshabilita la descarga TCP Chimney para cada conexión entrante.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ Callout \_ set \_ Options \_ auth \_ Connect \_ Layer \_ V4/FWPM \_ Callout \_ set \_ Options \_ auth \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Establece las opciones de clasificación en los flujos de salida.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ Callout \_ set \_ Options \_ auth \_ RECV \_ Accept \_ capa \_ V4/FWPM \_ Callout \_ set \_ Options \_ auth \_ RECV \_ Accept \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Establece las opciones de clasificación en los flujos de entrada.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ Callout \_ Reserved \_ auth \_ Connect \_ Layer \_ V4/FWPM \_ llamada \_ Reserved \_ auth \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Este identificador está reservado para uso interno.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM de extremo de llamada de recorrido de la \_ \_ periferia \_ \_ \_ \_ V6/FWPM \_ llamada \_ Teredo \_ escucha de Ale \_ \_ V6**
</dt> <dd> <dl> <dt>



Indica al servicio Teredo que una aplicación requiere una dirección Teredo.

> [!Note]  
> En Windows 7 y versiones posteriores, use **FWPM \_ CALLOUT \_ Edge \_ traversary \_ \_ Listen \_**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM de \_ llamada de límite de asignación de recursos de \_ \_ \_ Ale \_ \_ \_ V6/FWPM llamada a la \_ asignación de \_ recursos Ale de Teredo \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Indica al servicio Teredo que una aplicación requiere una dirección Teredo.

> [!Note]  
> En Windows 7 y versiones posteriores, use la **asignación de recursos de Ale de borde de llamada FWPM \_ \_ \_ \_ \_ \_ \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM de la \_ \_ asignación de \_ recursos Ale de la periferia del borde de llamada \_ \_ \_ \_ V4** 
</dt> <dd> <dl> <dt>



Este identificador se reserva para uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM de la llamada de recorrido de la \_ \_ periferia \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Este identificador se reserva para uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ Callout \_ TCP \_ plantillas \_ Connect \_ Layer \_ V4/FWPM \_ Callout \_ TCP \_ de \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Aplica la configuración de plantilla TCP para las conexiones salientes coincidentes.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM \_ Callout \_ TCP \_ plantillas \_ Accept \_ Layer \_ V4/FWPM \_ Callout \_ TCP \_ \_ Accept \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Aplica la configuración de plantilla TCP para las conexiones entrantes coincidentes.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





