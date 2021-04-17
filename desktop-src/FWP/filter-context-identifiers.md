---
title: Identificadores de contexto de filtro (Fwpmu. h)
description: Los identificadores de los contextos de filtro integrados en la plataforma de filtrado de Windows.
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
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666067"
---
# <a name="filter-context-identifiers"></a>Identificadores de contexto de filtro

Los identificadores de los contextos de filtro integrados en la plataforma de filtrado de Windows se definen como se indica a continuación.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**\_contexto \_ de FWPM \_ de entrada IPSec de Inbound \_ , contexto de FWPM de \_ \_ \_ \_ \_ seguridad de conexión persistente \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Contextos de filtro de transporte IPsec en el nivel de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**\_contexto \_ de FWPM \_ de tráfico \_ de salida de IPSec \_ de detección de FWPM de \_ contexto de \_ IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>



Contextos de filtro de transporte IPsec en el nivel de salida.

> [!Note]  
> En Windows 7, use el **contexto FWPM de la negociación de \_ \_ supresión de \_ salida \_ \_ de IPSec**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**la \_ \_ conexión del conjunto Ale de FWPM context \_ \_ \_ requiere \_ \_ seguridad de IPSec, FWPM \_ contexto Ale de configuración de la \_ \_ \_ conexión \_ \_ \_**
</dt> <dd> <dl> <dt>



Contextos de filtro usados en el nivel de conexión de ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**la \_ conexión FWPM context \_ Ale \_ set \_ \_ requiere \_ \_ cifrado IPSec, FWPM \_ Context \_ Ale set de la \_ \_ conexión \_ permitir \_ primer \_ PKT entrante sin \_ \_ cifrar, FWPM \_ contextual \_ Ale \_ permitir \_ auth \_ FW**
</dt> <dd> <dl> <dt>



Contextos de filtro usados en la capa de aceptación o conexión de ALE.

> [!Note]  
> En Windows 7, use **FWPM \_ Context \_ Ale \_ set \_ Connection \_ Allow \_ First \_ entrantes de entrada \_ \_ sin cifrar** o **FWPM de \_ contexto \_ Ale de \_ \_ autorización permitir autenticación \_ FW**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_ \_ \_ \_ deshabilitación de la descarga TCP Chimney de FWPM de contexto \_ de FWPM \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Contextos usados por las llamadas de descarga de TCP Chimney.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**auditoría de FWPM de \_ contexto \_ RPC \_ \_ habilitada**
</dt> <dd> <dl> <dt>



Contextos usados en el subnivel de auditoría de RPC.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





