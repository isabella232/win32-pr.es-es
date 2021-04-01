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
# <a name="filtering-sublayer-identifiers"></a><span data-ttu-id="17d49-103">Filtrado de identificadores de subnivel</span><span class="sxs-lookup"><span data-stu-id="17d49-103">Filtering Sublayer Identifiers</span></span>

<span data-ttu-id="17d49-104">Los identificadores de subnivel de la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="17d49-104">The Windows Filtering Platform (WFP) sublayer identifiers are each represented by a GUID.</span></span>

<span data-ttu-id="17d49-105">Estos identificadores se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="17d49-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="17d49-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM de subcapas de \_ \_ \_ cruce transversal/FWPM del perímetro de \_ subcapas \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM\_SUBLAYER\_EDGE\_TRAVERSAL / FWPM\_SUBLAYER\_TEREDO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-107">Los filtros de cruce seguro del perímetro se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-107">Edge traversal filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="17d49-108">En Windows 7 y versiones posteriores, use el **\_ \_ \_ cruce seguro del perímetro de subcapas de FWPM**.</span><span class="sxs-lookup"><span data-stu-id="17d49-108">For Windows 7 and later, use **FWPM\_SUBLAYER\_EDGE\_TRAVERSAL**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_inspección de SUBcapas de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM\_SUBLAYER\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-110">Esta es la subcapa ponderada más baja.</span><span class="sxs-lookup"><span data-stu-id="17d49-110">This is the lowest weighted sublayer.</span></span> <span data-ttu-id="17d49-111">Solo se usa para los filtros de inspección.</span><span class="sxs-lookup"><span data-stu-id="17d49-111">It is used only for inspection filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_DOSP de IPSec de subcapa FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM\_SUBLAYER\_IPSEC\_DOSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-113">Los filtros de protección DoS de IPsec se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-113">IPsec DoS Protection filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="17d49-114">Solo está disponible en Windows Vista con SP1, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="17d49-114">Available only on Windows Vista with SP1, Windows Server 2008, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_túnel de salida de \_ \_ reenvío IPSec de \_ subcapa FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-116">Los filtros de túnel de salida de reenvío IPsec se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-116">IPsec forward outbound tunnel filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="17d49-117">Solo está disponible en Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="17d49-117">Available only on Windows 7, Windows Server 2008 R2, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_túnel IPSec de subcapa FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-119">Los filtros de túnel IPsec se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-119">IPsec tunnel filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_Lip de SUBcapa de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM\_SUBLAYER\_LIPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-121">Los filtros IPsec heredados se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-121">Legacy IPsec filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_Auditoría de RPC de subcapa FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM\_SUBLAYER\_RPC\_AUDIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-123">Los filtros de auditoría de RPC se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-123">RPC audit filters are added to this sublayer.</span></span> <span data-ttu-id="17d49-124">Estos filtros auditan las llamadas entrantes de RPC como parte del cumplimiento de criterios de C2 y común.</span><span class="sxs-lookup"><span data-stu-id="17d49-124">These filters audit RPC incoming calls as part of C2 and common criteria compliance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_socket seguro de subcapa FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM\_SUBLAYER\_SECURE\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-126">Los filtros de sockets seguros se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-126">Secure socket filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ descarga de TCP \_ CHIMNEY \_ de subcapa FWPM**</span><span class="sxs-lookup"><span data-stu-id="17d49-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM\_SUBLAYER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-128">Los filtros de descarga TCP Chimney se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-128">TCP Chimney Offload filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_plantillas TCP de subcapa FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17d49-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM\_SUBLAYER\_TCP\_TEMPLATES**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-130">Los filtros de plantilla TCP se agregan a esta subcapa.</span><span class="sxs-lookup"><span data-stu-id="17d49-130">TCP template filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="17d49-131">Solo está disponible en Windows 8, Windows Server 2012 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="17d49-131">Available only on Windows 8, Windows Server 2012, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="17d49-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM de \_ subnivel \_ universal**</span><span class="sxs-lookup"><span data-stu-id="17d49-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM\_SUBLAYER\_UNIVERSAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17d49-133">Este subnivel hospeda todos los filtros que no están asignados a ninguno de los demás subnivels.</span><span class="sxs-lookup"><span data-stu-id="17d49-133">This sublayer hosts all filters that are not assigned to any of the other sublayers.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17d49-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17d49-134">Requirements</span></span>



| <span data-ttu-id="17d49-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="17d49-135">Requirement</span></span> | <span data-ttu-id="17d49-136">Value</span><span class="sxs-lookup"><span data-stu-id="17d49-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17d49-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17d49-137">Minimum supported client</span></span><br/> | <span data-ttu-id="17d49-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17d49-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="17d49-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17d49-139">Minimum supported server</span></span><br/> | <span data-ttu-id="17d49-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="17d49-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17d49-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17d49-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d49-142"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="17d49-142"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





