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
# <a name="built-in-callout-identifiers"></a><span data-ttu-id="dfa2d-104">Identificadores de llamada integrados</span><span class="sxs-lookup"><span data-stu-id="dfa2d-104">Built-in Callout Identifiers</span></span>

<span data-ttu-id="dfa2d-105">Los identificadores de las funciones de llamada integradas en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-105">The identifiers for the callout functions that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="dfa2d-106">Estos identificadores se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-106">These identifiers are defined as follows.</span></span>

<span data-ttu-id="dfa2d-107">Los sufijos V4 y V6 al final de los identificadores de llamada indican si la llamada es para la pila de red IPv4 o para la pila de red IPv6.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-107">The V4 and V6 suffixes at the end of the callout identifiers indicate whether the callout is for the IPv4 network stack or for the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="dfa2d-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V4/llamada de FWPM para el transporte de \_ \_ \_ entrada IPSec \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-109">Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad del modo de transporte llega de forma segura.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-109">Verifies that each received packet that is supposed to arrive over a transport mode security association arrives securely.</span></span>

<span data-ttu-id="dfa2d-110">Esta llamada es aplicable en el nivel de transporte.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-110">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V4/FWPM \_ llamada IPSec de transporte de \_ \_ salida \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-112">Indica a IPsec el tráfico saliente que se debe proteger a través de las asociaciones de seguridad del modo de transporte.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-112">Indicates to IPsec the outbound traffic that must be secured over transport mode security associations.</span></span>

<span data-ttu-id="dfa2d-113">Esta llamada es aplicable en el nivel de transporte.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-113">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**Llamada de FWPM de \_ \_ \_ túnel entrante de IPSec \_ \_ V4/ \_ llamada FWPM \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-115">Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad en modo de túnel llega de forma segura.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-115">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="dfa2d-116">Esta llamada es aplicable en el nivel de transporte.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-116">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**Llamada de FWPM de \_ \_ túnel de salida de IPSec \_ \_ \_ V4/FWPM \_ llamada IPSec del túnel de \_ \_ salida \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-118">Indica a IPsec el tráfico saliente que debe protegerse a través de las asociaciones de seguridad del modo de túnel.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-118">Indicates to IPsec the outbound traffic that must be secured over tunnel mode security associations.</span></span>

<span data-ttu-id="dfa2d-119">Esta llamada es aplicable en el nivel de transporte.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-119">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**Llamada de FWPM de \_ \_ IPSec \_ reenviar túnel de \_ entrada \_ \_ V4/FWPM \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-121">Comprueba que cada paquete recibido que se supone que llega a través de una asociación de seguridad en modo de túnel llega de forma segura.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-121">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="dfa2d-122">Esta llamada es aplicable en la capa de reenvío.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-122">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**Llamada de FWPM de \_ \_ IPSec \_ reenviar \_ túnel de salida \_ \_ V4/FWPM \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-124">Indica a IPsec el tráfico saliente que se debe proteger a través de una asociación de seguridad en modo de túnel.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-124">Indicates to IPsec the outbound traffic that must be secured over a tunnel mode security association.</span></span>

<span data-ttu-id="dfa2d-125">Esta llamada es aplicable en la capa de reenvío.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-125">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**Llamada de FWPM \_ llamada de \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V4/FWPM \_ llamada \_ IPSec \_ entrante \_ iniciar \_ Secure \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-127">Comprueba que todas las conexiones entrantes que se supone que llegan a ser seguras llegan de forma segura.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-127">Verifies that each incoming connection that is supposed to arrive secure arrives securely.</span></span>

<span data-ttu-id="dfa2d-128">Esta llamada es aplicable a la capa de aceptación de ALE.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-128">This callout is applicable at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**Llamada de FWPM \_ llamada \_ Ale de \_ túnel entrante de IPSec \_ \_ \_ Accept \_ V4/FWPM \_ CALLOUT \_ IPSec \_ \_ tunelización entrante \_ \_ aceptación \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-130">Permite los paquetes IP en modo de túnel de IPsec cuando se clasifican en la capa de aceptación de ALE.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-130">Permits the IPsec tunnel mode IP-in-IP packets when they get classified at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**Llamada de FWPM de \_ \_ IPSec \_ Ale de \_ conexión \_ V4/FWPM \_ llamada a \_ IPSec \_ Ale \_ Connect \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V4 / FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-132">Aplica los modificadores de directivas IPsec a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-132">Applies IPsec policy modifiers to client applications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**\_Llamada FWPM \_ IPSec \_ DOSP \_ reenvío \_ V4/FWPM \_ llamada \_ IPSec \_ DOSP \_ Forward \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V4 / FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-134">Señala a la protección de DoS de IPsec que el tráfico debe comprobarse para posibles DoS y puede que tenga que tener una velocidad limitada.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-134">Signals to IPsec DoS Protection that traffic needs to be verified for potential DoS and may need to be rate limited.</span></span>

> [!Note]  
> <span data-ttu-id="dfa2d-135">Solo está disponible en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-135">Available only in Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ llamada \_ WFP \_ nivel de transporte WFP \_ \_ V4 \_ eliminación silenciosa \_ /FWPM \_ llamada \_ WFP \_ nivel de transporte WFP \_ \_ V6 \_ eliminación silenciosa \_**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V4\_SILENT\_DROP / FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V6\_SILENT\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-137">Implementa el filtrado en modo oculto mediante la eliminación silenciosa de todos los paquetes entrantes para los que TCP no tiene un extremo de escucha.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-137">Implements stealth-mode filtering by silently dropping all incoming packets for which TCP does not have a listening endpoint.</span></span>

<span data-ttu-id="dfa2d-138">Esta llamada es aplicable en el nivel de descartar transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-138">This callout is applicable at the inbound transport discard layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ Callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V4/FWPM \_ Callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-140">Habilita o deshabilita la descarga TCP Chimney para cada conexión de salida.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-140">Enables or disables TCP chimney offload for each outgoing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ llamada \_ TCP \_ Chimney \_ aceptación \_ capa \_ V4/FWPM \_ llamada \_ TCP \_ Chimney \_ aceptación \_ capa \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-142">Habilita o deshabilita la descarga TCP Chimney para cada conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-142">Enables or disables TCP chimney offload for each incoming connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ Callout \_ set \_ Options \_ auth \_ Connect \_ Layer \_ V4/FWPM \_ Callout \_ set \_ Options \_ auth \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-144">Establece las opciones de clasificación en los flujos de salida.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-144">Sets classify options on outbound flows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ Callout \_ set \_ Options \_ auth \_ RECV \_ Accept \_ capa \_ V4/FWPM \_ Callout \_ set \_ Options \_ auth \_ RECV \_ Accept \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-146">Establece las opciones de clasificación en los flujos de entrada.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-146">Sets classify options on inbound flows.</span></span>

> [!Note]  
> <span data-ttu-id="dfa2d-147">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-147">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ Callout \_ Reserved \_ auth \_ Connect \_ Layer \_ V4/FWPM \_ llamada \_ Reserved \_ auth \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-149">Este identificador está reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-149">This identifier is reserved for internal use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM de extremo de llamada de recorrido de la \_ \_ periferia \_ \_ \_ \_ V6/FWPM \_ llamada \_ Teredo \_ escucha de Ale \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-151">Indica al servicio Teredo que una aplicación requiere una dirección Teredo.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-151">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="dfa2d-152">En Windows 7 y versiones posteriores, use **FWPM \_ CALLOUT \_ Edge \_ traversary \_ \_ Listen \_**.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-152">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM de \_ llamada de límite de asignación de recursos de \_ \_ \_ Ale \_ \_ \_ V6/FWPM llamada a la \_ asignación de \_ recursos Ale de Teredo \_ \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-154">Indica al servicio Teredo que una aplicación requiere una dirección Teredo.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-154">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="dfa2d-155">En Windows 7 y versiones posteriores, use la **asignación de recursos de Ale de borde de llamada FWPM \_ \_ \_ \_ \_ \_ \_ V6**.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-155">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM de la \_ \_ asignación de \_ recursos Ale de la periferia del borde de llamada \_ \_ \_ \_ V4**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V4**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-157">Este identificador se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-157">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM de la llamada de recorrido de la \_ \_ periferia \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V4**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-159">Este identificador se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-159">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ Callout \_ TCP \_ plantillas \_ Connect \_ Layer \_ V4/FWPM \_ Callout \_ TCP \_ de \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-161">Aplica la configuración de plantilla TCP para las conexiones salientes coincidentes.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-161">Applies TCP template settings for matching outgoing connections.</span></span>

> [!Note]  
> <span data-ttu-id="dfa2d-162">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-162">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfa2d-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM \_ Callout \_ TCP \_ plantillas \_ Accept \_ Layer \_ V4/FWPM \_ Callout \_ TCP \_ \_ Accept \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="dfa2d-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfa2d-164">Aplica la configuración de plantilla TCP para las conexiones entrantes coincidentes.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-164">Applies TCP template settings for matching incoming connections.</span></span>

> [!Note]  
> <span data-ttu-id="dfa2d-165">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dfa2d-165">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfa2d-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa2d-166">Requirements</span></span>



| <span data-ttu-id="dfa2d-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa2d-167">Requirement</span></span> | <span data-ttu-id="dfa2d-168">Value</span><span class="sxs-lookup"><span data-stu-id="dfa2d-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa2d-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfa2d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa2d-170">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dfa2d-170">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dfa2d-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfa2d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa2d-172">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dfa2d-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dfa2d-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfa2d-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfa2d-174"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa2d-174"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





