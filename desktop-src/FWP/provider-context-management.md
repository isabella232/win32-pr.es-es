---
title: Administración de contexto de proveedor
description: Administración de contexto de proveedor
ms.assetid: A73A6171-C81B-48EF-A689-3219E0B6B7C3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7970cdd6f3a69760a74ba4f0419ecb5022a339
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790552"
---
# <a name="provider-context-management"></a><span data-ttu-id="6e486-103">Administración de contexto de proveedor</span><span class="sxs-lookup"><span data-stu-id="6e486-103">Provider Context Management</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6e486-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6e486-104">In this section</span></span>

-   [<span data-ttu-id="6e486-105">**Cambio de contexto del proveedor de FWPM \_ \_ \_ \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="6e486-105">**FWPM\_PROVIDER\_CONTEXT\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0)
-   [<span data-ttu-id="6e486-106">**FwpmProviderContextAdd0**</span><span class="sxs-lookup"><span data-stu-id="6e486-106">**FwpmProviderContextAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)
-   [<span data-ttu-id="6e486-107">**FwpmProviderContextAdd1**</span><span class="sxs-lookup"><span data-stu-id="6e486-107">**FwpmProviderContextAdd1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd1)
-   [<span data-ttu-id="6e486-108">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="6e486-108">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="6e486-109">**FwpmProviderContextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="6e486-109">**FwpmProviderContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0)
-   [<span data-ttu-id="6e486-110">**FwpmProviderContextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="6e486-110">**FwpmProviderContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebyid0)
-   [<span data-ttu-id="6e486-111">**FwpmProviderContextDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="6e486-111">**FwpmProviderContextDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebykey0)
-   [<span data-ttu-id="6e486-112">**FwpmProviderContextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="6e486-112">**FwpmProviderContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0)
-   [<span data-ttu-id="6e486-113">**FwpmProviderContextEnum0**</span><span class="sxs-lookup"><span data-stu-id="6e486-113">**FwpmProviderContextEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum0)
-   [<span data-ttu-id="6e486-114">**FwpmProviderContextEnum1**</span><span class="sxs-lookup"><span data-stu-id="6e486-114">**FwpmProviderContextEnum1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum1)
-   [<span data-ttu-id="6e486-115">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="6e486-115">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="6e486-116">**FwpmProviderContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="6e486-116">**FwpmProviderContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0)
-   [<span data-ttu-id="6e486-117">**FwpmProviderContextGetById1**</span><span class="sxs-lookup"><span data-stu-id="6e486-117">**FwpmProviderContextGetById1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid1)
-   [<span data-ttu-id="6e486-118">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="6e486-118">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="6e486-119">**FwpmProviderContextGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="6e486-119">**FwpmProviderContextGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey0)
-   [<span data-ttu-id="6e486-120">**FwpmProviderContextGetByKey1**</span><span class="sxs-lookup"><span data-stu-id="6e486-120">**FwpmProviderContextGetByKey1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey1)
-   [<span data-ttu-id="6e486-121">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="6e486-121">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="6e486-122">**FwpmProviderContextGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="6e486-122">**FwpmProviderContextGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetsecurityinfobykey0)
-   [<span data-ttu-id="6e486-123">**FwpmProviderContextSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="6e486-123">**FwpmProviderContextSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsetsecurityinfobykey0)
-   [<span data-ttu-id="6e486-124">**FwpmProviderContextSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="6e486-124">**FwpmProviderContextSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0)
-   [<span data-ttu-id="6e486-125">**FwpmProviderContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="6e486-125">**FwpmProviderContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscriptionsget0)
-   [<span data-ttu-id="6e486-126">**FwpmProviderContextUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="6e486-126">**FwpmProviderContextUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextunsubscribechanges0)

 

 