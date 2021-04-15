---
title: Funciones de IPsec
description: Funciones de IPsec
ms.assetid: db656c58-7776-44c4-a7ce-c38e59b37c74
keywords:
- Funciones IPsec de la API de la plataforma de filtrado de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261e767888b4581587ee550bf240c929f6db4531
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665823"
---
# <a name="ipsec-functions"></a><span data-ttu-id="71280-104">Funciones de IPsec</span><span class="sxs-lookup"><span data-stu-id="71280-104">IPsec Functions</span></span>

<span data-ttu-id="71280-105">Las funciones de la plataforma de filtrado de Windows (WFP) que interactúan con el protocolo de seguridad de Internet (IPsec) son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="71280-105">The Windows Filtering Platform (WFP) functions that interact with Internet Protocol Security (IPsec) are as follows.</span></span>

-   <span data-ttu-id="71280-106">FwpmIPsecTunnelAdd:</span><span class="sxs-lookup"><span data-stu-id="71280-106">FwpmIPsecTunnelAdd:</span></span>
    -   <span data-ttu-id="71280-107">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-107">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-108">[**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="71280-108">[**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7)</span></span>
    -   <span data-ttu-id="71280-109">[**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="71280-109">[**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8)</span></span>
-   [<span data-ttu-id="71280-110">**FwpmIPsecTunnelDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="71280-110">**FwpmIPsecTunnelDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)
-   [<span data-ttu-id="71280-111">**\_Dictado de clave del administrador de claves IPSec \_ \_ \_ \_ CHECK0**</span><span class="sxs-lookup"><span data-stu-id="71280-111">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="71280-112">**El \_ Administrador de claves IPSec \_ \_ dicta \_ KEY0**</span><span class="sxs-lookup"><span data-stu-id="71280-112">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="71280-113">**\_Administrador de claves IPSec \_ \_ notificar a \_ KEY0**</span><span class="sxs-lookup"><span data-stu-id="71280-113">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="71280-114">**Contexto de SA de IPSEC \_ \_ \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="71280-114">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="71280-115">**IPsecDospGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="71280-115">**IPsecDospGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetsecurityinfo0)
-   [<span data-ttu-id="71280-116">**IPsecDospGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="71280-116">**IPsecDospGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetstatistics0)
-   [<span data-ttu-id="71280-117">**IPsecDospSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="71280-117">**IPsecDospSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospsetsecurityinfo0)
-   [<span data-ttu-id="71280-118">**IPsecDospStateCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="71280-118">**IPsecDospStateCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0)
-   [<span data-ttu-id="71280-119">**IPsecDospStateDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="71280-119">**IPsecDospStateDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatedestroyenumhandle0)
-   [<span data-ttu-id="71280-120">**IPsecDospStateEnum0**</span><span class="sxs-lookup"><span data-stu-id="71280-120">**IPsecDospStateEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstateenum0)
-   <span data-ttu-id="71280-121">IPsecGetStatistics:</span><span class="sxs-lookup"><span data-stu-id="71280-121">IPsecGetStatistics:</span></span>
    -   <span data-ttu-id="71280-122">[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-122">[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-123">[**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-123">[**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="71280-124">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="71280-124">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="71280-125">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="71280-125">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="71280-126">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="71280-126">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="71280-127">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="71280-127">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="71280-128">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="71280-128">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   <span data-ttu-id="71280-129">IPsecSaContextAddInbound:</span><span class="sxs-lookup"><span data-stu-id="71280-129">IPsecSaContextAddInbound:</span></span>
    -   <span data-ttu-id="71280-130">[**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-130">[**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-131">[**IPsecSaContextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-131">[**IPsecSaContextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="71280-132">IPsecSaContextAddOutbound:</span><span class="sxs-lookup"><span data-stu-id="71280-132">IPsecSaContextAddOutbound:</span></span>
    -   <span data-ttu-id="71280-133">[**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-133">[**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-134">[**IPsecSaContextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-134">[**IPsecSaContextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="71280-135">IPsecSaContextCreate:</span><span class="sxs-lookup"><span data-stu-id="71280-135">IPsecSaContextCreate:</span></span>
    -   <span data-ttu-id="71280-136">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-136">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-137">[**IPsecSaContextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-137">[**IPsecSaContextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="71280-138">**IPsecSaContextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="71280-138">**IPsecSaContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)
-   [<span data-ttu-id="71280-139">**IPsecSaContextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="71280-139">**IPsecSaContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)
-   [<span data-ttu-id="71280-140">**IPsecSaContextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="71280-140">**IPsecSaContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0)
-   <span data-ttu-id="71280-141">IPsecSaContextEnum:</span><span class="sxs-lookup"><span data-stu-id="71280-141">IPsecSaContextEnum:</span></span>
    -   <span data-ttu-id="71280-142">[**IPsecSaContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-142">[**IPsecSaContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-143">[**IPsecSaContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-143">[**IPsecSaContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="71280-144">**IPsecSaContextExpire0**</span><span class="sxs-lookup"><span data-stu-id="71280-144">**IPsecSaContextExpire0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)
-   <span data-ttu-id="71280-145">IPsecSaContextGetById:</span><span class="sxs-lookup"><span data-stu-id="71280-145">IPsecSaContextGetById:</span></span>
    -   <span data-ttu-id="71280-146">[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-146">[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-147">[**IPsecSaContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-147">[**IPsecSaContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="71280-148">IPsecSaContextGetSpi:</span><span class="sxs-lookup"><span data-stu-id="71280-148">IPsecSaContextGetSpi:</span></span>
    -   <span data-ttu-id="71280-149">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-149">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-150">[**IPsecSaContextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-150">[**IPsecSaContextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="71280-151">**IPsecSaContextSetSpi0**</span><span class="sxs-lookup"><span data-stu-id="71280-151">**IPsecSaContextSetSpi0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsetspi0)
-   [<span data-ttu-id="71280-152">**IPsecSaContextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="71280-152">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="71280-153">**IPsecSaContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="71280-153">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="71280-154">**IPsecSaContextUpdate0**</span><span class="sxs-lookup"><span data-stu-id="71280-154">**IPsecSaContextUpdate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [<span data-ttu-id="71280-155">**IPsecSaContextUpdate0**</span><span class="sxs-lookup"><span data-stu-id="71280-155">**IPsecSaContextUpdate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [<span data-ttu-id="71280-156">**IPsecSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="71280-156">**IPsecSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)
-   [<span data-ttu-id="71280-157">**IPsecSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="71280-157">**IPsecSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbgetsecurityinfo0)
-   [<span data-ttu-id="71280-158">**IPsecSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="71280-158">**IPsecSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbsetsecurityinfo0)
-   [<span data-ttu-id="71280-159">**IPsecSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="71280-159">**IPsecSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0)
-   <span data-ttu-id="71280-160">IPsecSaEnum:</span><span class="sxs-lookup"><span data-stu-id="71280-160">IPsecSaEnum:</span></span>
    -   <span data-ttu-id="71280-161">[**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="71280-161">[**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="71280-162">[**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="71280-162">[**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 and later)</span></span>

 

 