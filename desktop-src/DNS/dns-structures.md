---
title: Estructuras DNS
description: Página de navegación de estructuras del sistema de nombres de dominio (DNS).
ms.assetid: 636399be-43a5-4ddf-b652-f8efb81fbf42
keywords:
- Estructuras del sistema de nombres de dominio
- Estructuras DNS
- Sistema de nombres de dominio, referencia, estructuras
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 65da2f26026ef1d9fe443fc3cfc05736459a3743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078149"
---
# <a name="dns-structures"></a><span data-ttu-id="875e0-106">Estructuras DNS</span><span class="sxs-lookup"><span data-stu-id="875e0-106">DNS Structures</span></span>

<span data-ttu-id="875e0-107">Las siguientes estructuras se definen para su uso con DNS:</span><span class="sxs-lookup"><span data-stu-id="875e0-107">The following structures are defined for use with DNS:</span></span>

- [<span data-ttu-id="875e0-108">**DNS_ADDR**</span><span class="sxs-lookup"><span data-stu-id="875e0-108">**DNS_ADDR**</span></span>](/windows/win32/api/windns/ns-windns-dns_addr)
- [<span data-ttu-id="875e0-109">**DNS_ADDR_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="875e0-109">**DNS_ADDR_ARRAY**</span></span>](/windows/win32/api/windns/ns-windns-dns_addr_array)
- [<span data-ttu-id="875e0-110">**DNS_HEADER**</span><span class="sxs-lookup"><span data-stu-id="875e0-110">**DNS_HEADER**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_header)
- [<span data-ttu-id="875e0-111">**DNS_MESSAGE_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="875e0-111">**DNS_MESSAGE_BUFFER**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_message_buffer)
- [<span data-ttu-id="875e0-112">**DNS_PROXY_INFORMATION**</span><span class="sxs-lookup"><span data-stu-id="875e0-112">**DNS_PROXY_INFORMATION**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_proxy_information)
- [<span data-ttu-id="875e0-113">**DNS_QUERY_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="875e0-113">**DNS_QUERY_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_query_request)
- [<span data-ttu-id="875e0-114">**DNS_RECORD**</span><span class="sxs-lookup"><span data-stu-id="875e0-114">**DNS_RECORD**</span></span>](/windows/win32/api/windns/ns-windns-dns_recorda)
- [<span data-ttu-id="875e0-115">**DNS_RECORD_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="875e0-115">**DNS_RECORD_FLAGS**</span></span>](/windows/win32/api/windns/ns-windns-dns_record_flags)
- [<span data-ttu-id="875e0-116">**DNS_SERVICE_BROWSE_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="875e0-116">**DNS_SERVICE_BROWSE_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_browse_request)
- [<span data-ttu-id="875e0-117">**DNS_SERVICE_CANCEL**</span><span class="sxs-lookup"><span data-stu-id="875e0-117">**DNS_SERVICE_CANCEL**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_cancel)
- [<span data-ttu-id="875e0-118">**DNS_SERVICE_INSTANCE**</span><span class="sxs-lookup"><span data-stu-id="875e0-118">**DNS_SERVICE_INSTANCE**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_instance)
- [<span data-ttu-id="875e0-119">**DNS_SERVICE_REGISTER_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="875e0-119">**DNS_SERVICE_REGISTER_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_register_request)
- [<span data-ttu-id="875e0-120">**DNS_SERVICE_RESOLVE_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="875e0-120">**DNS_SERVICE_RESOLVE_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_resolve_request)
- [<span data-ttu-id="875e0-121">**IP4_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="875e0-121">**IP4_ARRAY**</span></span>](/windows/desktop/api/Windns/ns-windns-ip4_array)
- [<span data-ttu-id="875e0-122">**IP6_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="875e0-122">**IP6_ADDRESS**</span></span>](/windows/win32/api/windns/ns-windns-ip6_address)
- [<span data-ttu-id="875e0-123">**MDNS_QUERY_HANDLE**</span><span class="sxs-lookup"><span data-stu-id="875e0-123">**MDNS_QUERY_HANDLE**</span></span>](/windows/desktop/api/Windns/ns-windns-mdns_query_handle)
- [<span data-ttu-id="875e0-124">**MDNS_QUERY_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="875e0-124">**MDNS_QUERY_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-mdns_query_request)

<span data-ttu-id="875e0-125">Las siguientes estructuras de registro de recursos (RR) también se incluyen en la API de DNS.</span><span class="sxs-lookup"><span data-stu-id="875e0-125">The following Resource Record (RR) structures are also included in the DNS API.</span></span> <span data-ttu-id="875e0-126">Estas estructuras se utilizan con la estructura **DNS_RECORD** para administrar mediante programación los registros de recursos DNS.</span><span class="sxs-lookup"><span data-stu-id="875e0-126">These structures are used with the **DNS_RECORD** structure to programmatically manage DNS resource records.</span></span>

- [<span data-ttu-id="875e0-127">**DNS_A_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-127">**DNS_A_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_a_data)
- [<span data-ttu-id="875e0-128">**DNS_AAAA_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-128">**DNS_AAAA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_aaaa_data)
- [<span data-ttu-id="875e0-129">**DNS_ATMA_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-129">**DNS_ATMA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_atma_data)
- [<span data-ttu-id="875e0-130">**DNS_DHCID_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-130">**DNS_DHCID_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_dhcid_data)
- <span data-ttu-id="875e0-131">[**DNS_DNSKEY_DATA**](/previous-versions/windows/desktop/legacy/dd392295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="875e0-131">[**DNS_DNSKEY_DATA**](/previous-versions/windows/desktop/legacy/dd392295(v=vs.85))</span></span>
- [<span data-ttu-id="875e0-132">**DNS_DS_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-132">**DNS_DS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_ds_data)
- [<span data-ttu-id="875e0-133">**DNS_KEY_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-133">**DNS_KEY_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_key_data)
- [<span data-ttu-id="875e0-134">**DNS_LOC_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-134">**DNS_LOC_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_loc_data)
- [<span data-ttu-id="875e0-135">**DNS_MINFO_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-135">**DNS_MINFO_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_minfo_dataw)
- [<span data-ttu-id="875e0-136">**DNS_MX_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-136">**DNS_MX_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_mx_dataa)
- [<span data-ttu-id="875e0-137">**DNS_NAPTR_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-137">**DNS_NAPTR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_naptr_dataw)
- [<span data-ttu-id="875e0-138">**DNS_NSEC_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-138">**DNS_NSEC_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_nsec_dataw)
- [<span data-ttu-id="875e0-139">**DNS_NULL_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-139">**DNS_NULL_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_null_data)
- [<span data-ttu-id="875e0-140">**DNS_NXT_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-140">**DNS_NXT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_nxt_dataw)
- [<span data-ttu-id="875e0-141">**DNS_OPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-141">**DNS_OPT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_opt_data)
- [<span data-ttu-id="875e0-142">**DNS_PTR_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-142">**DNS_PTR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_ptr_dataw)
- [<span data-ttu-id="875e0-143">**DNS_RRSET**</span><span class="sxs-lookup"><span data-stu-id="875e0-143">**DNS_RRSET**</span></span>](/windows/win32/api/windns/ns-windns-dns_rrset)
- [<span data-ttu-id="875e0-144">**DNS_RRSIG_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-144">**DNS_RRSIG_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_sig_dataw)
- <span data-ttu-id="875e0-145">[**DNS_SIG_DATA**](/previous-versions/windows/desktop/legacy/ms682094(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="875e0-145">[**DNS_SIG_DATA**](/previous-versions/windows/desktop/legacy/ms682094(v=vs.85))</span></span>
- [<span data-ttu-id="875e0-146">**DNS_SOA_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-146">**DNS_SOA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_soa_dataw)
- [<span data-ttu-id="875e0-147">**DNS_SRV_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-147">**DNS_SRV_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_srv_dataw)
- [<span data-ttu-id="875e0-148">**DNS_TKEY_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-148">**DNS_TKEY_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_tkey_dataw)
- [<span data-ttu-id="875e0-149">**DNS_TSIG_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-149">**DNS_TSIG_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_tsig_dataw)
- [<span data-ttu-id="875e0-150">**DNS_TXT_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-150">**DNS_TXT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_txt_dataw)
- [<span data-ttu-id="875e0-151">**DNS_WINS_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-151">**DNS_WINS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_wins_data)
- [<span data-ttu-id="875e0-152">**DNS_WINSR_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-152">**DNS_WINSR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_winsr_dataw)
- [<span data-ttu-id="875e0-153">**DNS_WIRE_QUESTION**</span><span class="sxs-lookup"><span data-stu-id="875e0-153">**DNS_WIRE_QUESTION**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_wire_question)
- [<span data-ttu-id="875e0-154">**DNS_WIRE_RECORD**</span><span class="sxs-lookup"><span data-stu-id="875e0-154">**DNS_WIRE_RECORD**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_wire_record)
- [<span data-ttu-id="875e0-155">**DNS_WKS_DATA**</span><span class="sxs-lookup"><span data-stu-id="875e0-155">**DNS_WKS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_wks_data)