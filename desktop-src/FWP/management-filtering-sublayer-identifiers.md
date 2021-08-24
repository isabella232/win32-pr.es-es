---
title: Filtrar identificadores de subcapa (Fwpmu.h)
description: Constantes de identificador de subcapa de filtrado de WFP API Management.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d597fa1b75f6c965da9cf8d71bcc3e729d0b0b2f4f4220c984a1be8c94c09d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068885"
---
# <a name="filtering-sublayer-identifiers"></a>Filtrado de identificadores de subcapa

Cada Windows identificadores de subcapa de la plataforma de filtrado de filtros (WFP) se representan mediante un GUID.

Estos identificadores se definen de la manera siguiente.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM \_ SUBLAYER \_ EDGE \_ TRAVERSAL /FWPM \_ SUBLAYER \_ TEREDO**
</dt> <dd> <dl> <dt>



Los filtros transversales perimetrales se agregan a esta subcapa.

> [!Note]  
> Para Windows 7 y versiones posteriores, use **FWPM \_ SUBLAYER \_ EDGE \_ TRAVERSAL**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**INSPECCIÓN DE \_ SUBCAPAS FWPM \_**
</dt> <dd> <dl> <dt>



Se trata de la subcapa ponderada más baja. Solo se usa para los filtros de inspección.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**DOSP \_ DE IPSEC DE \_ SUBCAPA FWPM \_**
</dt> <dd> <dl> <dt>



Los filtros de IPsec DoS Protection se agregan a esta subcapa.

> [!Note]  
> Solo está disponible en Windows Vista con SP1, Windows Server 2008 y versiones posteriores.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**TÚNEL DE SALIDA \_ DE REENVÍO DE IPSEC DE \_ SUBCAPA \_ \_ FWPM \_**
</dt> <dd> <dl> <dt>



Los filtros de túnel de salida hacia delante de IPsec se agregan a esta subcapa.

> [!Note]  
> Disponible solo en Windows 7, Windows Server 2008 R2 y versiones posteriores.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**TÚNEL \_ IPSEC DE \_ SUBCAPA \_ FWPM**
</dt> <dd> <dl> <dt>



Los filtros de túnel IPsec se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM \_ \_ SUBLAYERLAYERLAYERLAYER (SUBCAPA FWPM)**
</dt> <dd> <dl> <dt>



Los filtros IPsec heredados se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM \_ SUBLAYER \_ RPC \_ AUDIT**
</dt> <dd> <dl> <dt>



Los filtros de auditoría RPC se agregan a esta subcapa. Estos filtros auditan las llamadas entrantes RPC como parte de C2 y el cumplimiento de criterios comunes.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**SOCKET SEGURO \_ DE SUBCAPA FWPM \_ \_**
</dt> <dd> <dl> <dt>



Los filtros de sockets seguros se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**DESCARGA DE LA CAMPANA \_ TCP DE \_ SUBCAPA FWPM \_ \_**
</dt> <dd> <dl> <dt>



Los filtros de descarga de TCP Chimney se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**PLANTILLAS \_ TCP DE SUBCAPA \_ FWPM \_** 
</dt> <dd> <dl> <dt>



Los filtros de plantilla TCP se agregan a esta subcapa.

> [!Note]  
> Solo está disponible en Windows 8, Windows Server 2012 y versiones posteriores.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM \_ SUBLAYER \_ UNIVERSAL**
</dt> <dd> <dl> <dt>



Esta subcapa hospeda todos los filtros que no están asignados a ninguna de las otras subcapas.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





