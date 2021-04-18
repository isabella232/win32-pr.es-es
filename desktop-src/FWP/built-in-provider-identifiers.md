---
title: Identificadores de proveedor integrados (Fwpmu. h)
description: Los identificadores de los proveedores integrados en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666045"
---
# <a name="built-in-provider-identifiers"></a><span data-ttu-id="d5493-103">Identificadores de proveedor integrados</span><span class="sxs-lookup"><span data-stu-id="d5493-103">Built-in Provider Identifiers</span></span>

<span data-ttu-id="d5493-104">Los identificadores de los proveedores integrados en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="d5493-104">The identifiers for the providers that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="d5493-105">Estos identificadores se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="d5493-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="d5493-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_proveedor FWPM \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="d5493-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM\_PROVIDER\_IKEEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5493-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span><span class="sxs-lookup"><span data-stu-id="d5493-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span></span>
</dt> <dt>



<span data-ttu-id="d5493-108">Se usa para identificar todos los filtros agregados por IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="d5493-108">Used to identify all the filters added by IKE/AuthIP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5493-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_configuración de \_ dos de IPSec del proveedor FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d5493-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM\_PROVIDER\_IPSEC\_DOS\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5493-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span><span class="sxs-lookup"><span data-stu-id="d5493-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span></span>
</dt> <dt>



<span data-ttu-id="d5493-111">Se usa para identificar todos los filtros agregados por la protección de DoS de IPsec.</span><span class="sxs-lookup"><span data-stu-id="d5493-111">Used to identify all the filters added by IPsec DoS Protection.</span></span>

> [!Note]  
> <span data-ttu-id="d5493-112">Solo está disponible en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d5493-112">Available only on Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5493-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_ \_ \_ descarga TCP CHIMNEY \_ del proveedor FWPM**</span><span class="sxs-lookup"><span data-stu-id="d5493-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM\_PROVIDER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5493-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span><span class="sxs-lookup"><span data-stu-id="d5493-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span></span>
</dt> <dt>



<span data-ttu-id="d5493-115">Se usa para identificar todos los filtros agregados por la descarga de TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="d5493-115">Used to identify all the filters added by TCP Chimney Offload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5493-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**\_ \_ plantillas TCP del proveedor FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="d5493-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**FWPM\_PROVIDER\_TCP\_TEMPLATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5493-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span><span class="sxs-lookup"><span data-stu-id="d5493-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span></span>
</dt> <dt>



<span data-ttu-id="d5493-118">Se usa para identificar todos los filtros agregados por las plantillas TCP.</span><span class="sxs-lookup"><span data-stu-id="d5493-118">Used to identify all the filters added by TCP templates.</span></span>

> [!Note]  
> <span data-ttu-id="d5493-119">Solo está disponible en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="d5493-119">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5493-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5493-120">Requirements</span></span>



| <span data-ttu-id="d5493-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5493-121">Requirement</span></span> | <span data-ttu-id="d5493-122">Value</span><span class="sxs-lookup"><span data-stu-id="d5493-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5493-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5493-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d5493-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5493-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5493-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5493-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d5493-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5493-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5493-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5493-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5493-128"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5493-128"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





