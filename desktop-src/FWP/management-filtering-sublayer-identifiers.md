---
title: Filtrar los identificadores de subcapa (Fwpmu. h)
description: Constantes de identificador de subcapa de filtrado de API de WFP.
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
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905494"
---
# <a name="filtering-sublayer-identifiers"></a>Filtrado de identificadores de subnivel

Los identificadores de subnivel de la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.

Estos identificadores se definen como se indica a continuación.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM de subcapas de \_ \_ \_ cruce transversal/FWPM del perímetro de \_ subcapas \_**
</dt> <dd> <dl> <dt>



Los filtros de cruce seguro del perímetro se agregan a esta subcapa.

> [!Note]  
> En Windows 7 y versiones posteriores, use el **\_ \_ \_ cruce seguro del perímetro de subcapas de FWPM**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_inspección de SUBcapas de FWPM \_**
</dt> <dd> <dl> <dt>



Esta es la subcapa ponderada más baja. Solo se usa para los filtros de inspección.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_DOSP de IPSec de subcapa FWPM \_ \_**
</dt> <dd> <dl> <dt>



Los filtros de protección DoS de IPsec se agregan a esta subcapa.

> [!Note]  
> Solo está disponible en Windows Vista con SP1, Windows Server 2008 y versiones posteriores.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_túnel de salida de \_ \_ reenvío IPSec de \_ subcapa FWPM \_**
</dt> <dd> <dl> <dt>



Los filtros de túnel de salida de reenvío IPsec se agregan a esta subcapa.

> [!Note]  
> Solo está disponible en Windows 7, Windows Server 2008 R2 y versiones posteriores.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_túnel IPSec de subcapa FWPM \_ \_**
</dt> <dd> <dl> <dt>



Los filtros de túnel IPsec se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_Lip de SUBcapa de FWPM \_**
</dt> <dd> <dl> <dt>



Los filtros IPsec heredados se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_Auditoría de RPC de subcapa FWPM \_ \_**
</dt> <dd> <dl> <dt>



Los filtros de auditoría de RPC se agregan a esta subcapa. Estos filtros auditan las llamadas entrantes de RPC como parte del cumplimiento de criterios de C2 y común.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_socket seguro de subcapa FWPM \_ \_**
</dt> <dd> <dl> <dt>



Los filtros de sockets seguros se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ descarga de TCP \_ CHIMNEY \_ de subcapa FWPM**
</dt> <dd> <dl> <dt>



Los filtros de descarga TCP Chimney se agregan a esta subcapa.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_plantillas TCP de subcapa FWPM \_ \_** 
</dt> <dd> <dl> <dt>



Los filtros de plantilla TCP se agregan a esta subcapa.

> [!Note]  
> Solo está disponible en Windows 8, Windows Server 2012 y versiones posteriores.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM de \_ subnivel \_ universal**
</dt> <dd> <dl> <dt>



Este subnivel hospeda todos los filtros que no están asignados a ninguno de los demás subnivels.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





