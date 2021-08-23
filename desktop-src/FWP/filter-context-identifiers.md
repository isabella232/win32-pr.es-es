---
title: Filtrar identificadores de contexto (Fwpmu.h)
description: Identificadores de los contextos de filtro integrados en la plataforma Windows filtrado.
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc7d9914a9b6089ace87e7e9b942499d8e65dc7705bf524f74cddf96ee419d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951274"
---
# <a name="filter-context-identifiers"></a>Filtrar identificadores de contexto

Los identificadores de los contextos de filtro integrados en la Windows de filtrado se definen de la siguiente manera.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PASSTHRU, FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PERSIST \_ CONNECTION \_ SECURITY, FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ RESERVED**
</dt> <dd> <dl> <dt>



Contextos de filtro de transporte IPsec en la capa de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM \_ CONTEXT \_ IPSEC \_ OUTBOUND \_ NEGOTIATE \_ DISCOVER, FWPM \_ CONTEXT \_ IPSEC \_ OUTBOUND \_ SUPPRESS \_ NEGOTIATION**
</dt> <dd> <dl> <dt>



Contextos de filtro de transporte IPsec en la capa de salida.

> [!Note]  
> Para Windows 7, use **FWPM \_ CONTEXT \_ IPSEC OUTBOUND SUPPRESS \_ \_ \_ NEGOTIATION**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**LA CONEXIÓN DE CONJUNTO DE ALE DE CONTEXTO FWPM REQUIERE SEGURIDAD \_ \_ \_ \_ \_ \_ \_ IPSEC, FWPM \_ CONTEXT \_ ALE SET CONNECTION \_ \_ \_ LAZY SD \_ \_ EVALUATION**
</dt> <dd> <dl> <dt>



Filtrar contextos usados en la capa de conexión de ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**LA CONEXIÓN DE CONJUNTO DE ALE DE CONTEXTO FWPM REQUIERE CIFRADO IPSEC, LA CONEXIÓN DE CONJUNTO DE ALE DE CONTEXTO FWPM PERMITE LA PRIMERA PKT ENTRANTE SIN \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ CIFRAR, FWPM \_ CONTEXT \_ ALE \_ ALLOW \_ AUTH \_ FW**
</dt> <dd> <dl> <dt>



Filtrar contextos usados en la capa de conexión o aceptación de ALE.

> [!Note]  
> Para Windows 7, use **FWPM \_ CONTEXT \_ ALE SET CONNECTION ALLOW \_ FIRST INBOUND \_ \_ \_ \_ \_ PKT \_ UNENCRYPTED** o **FWPM CONTEXT \_ \_ ALE ALLOW \_ \_ AUTH \_ FW**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM \_ CONTEXT \_ TCP \_ CHIMNEY \_ OFFLOAD \_ ENABLE, FWPM \_ CONTEXT \_ TCP \_ CHIMNEY \_ OFFLOAD \_ DISABLE**
</dt> <dd> <dl> <dt>



Contextos usados por las llamadas de descarga de TCP Chimney.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**AUDITORÍA RPC \_ DE CONTEXTO \_ FWPM \_ \_ HABILITADA**
</dt> <dd> <dl> <dt>



Contextos usados en la subcapa de auditoría RPC.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





