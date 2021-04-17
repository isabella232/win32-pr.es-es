---
description: La interfaz IAzAuthorizationStore expone las siguientes propiedades.
ms.assetid: FAA581E5-98F4-48DD-9B21-911896AE5A31
title: Propiedades de IAzAuthorizationStore
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ecd324ce31397007ac8e665df37d2308217673e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668238"
---
# <a name="iazauthorizationstore-properties"></a><span data-ttu-id="b9cf8-103">Propiedades de IAzAuthorizationStore</span><span class="sxs-lookup"><span data-stu-id="b9cf8-103">IAzAuthorizationStore Properties</span></span>

<span data-ttu-id="b9cf8-104">La interfaz [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9cf8-104">The [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b9cf8-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b9cf8-105">In this section</span></span>

-   [<span data-ttu-id="b9cf8-106">**Propiedad ApplicationData**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-106">**ApplicationData Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applicationdata)
-   [<span data-ttu-id="b9cf8-107">**Propiedad ApplicationGroups**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-107">**ApplicationGroups Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applicationgroups)
-   [<span data-ttu-id="b9cf8-108">**Propiedad Applications**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-108">**Applications Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applications)
-   [<span data-ttu-id="b9cf8-109">**Propiedad ApplyStoreSacl**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-109">**ApplyStoreSacl Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applystoresacl)
-   [<span data-ttu-id="b9cf8-110">**Propiedad DelegatedPolicyUsers**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-110">**DelegatedPolicyUsers Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_delegatedpolicyusers)
-   [<span data-ttu-id="b9cf8-111">**Propiedad DelegatedPolicyUsersName**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-111">**DelegatedPolicyUsersName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_delegatedpolicyusersname)
-   [<span data-ttu-id="b9cf8-112">**Description (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-112">**Description Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_description)
-   [<span data-ttu-id="b9cf8-113">**Propiedad DomainTimeout**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-113">**DomainTimeout Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_domaintimeout)
-   [<span data-ttu-id="b9cf8-114">**Propiedad GenerateAudits**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-114">**GenerateAudits Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_generateaudits)
-   [<span data-ttu-id="b9cf8-115">**Propiedad MaxScriptEngines**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-115">**MaxScriptEngines Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_maxscriptengines)
-   [<span data-ttu-id="b9cf8-116">**Propiedad PolicyAdministrators**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-116">**PolicyAdministrators Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyadministrators)
-   [<span data-ttu-id="b9cf8-117">**Propiedad PolicyAdministratorsName**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-117">**PolicyAdministratorsName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyadministratorsname)
-   [<span data-ttu-id="b9cf8-118">**Propiedad PolicyReaders**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-118">**PolicyReaders Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyreaders)
-   [<span data-ttu-id="b9cf8-119">**Propiedad PolicyReadersName**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-119">**PolicyReadersName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyreadersname)
-   [<span data-ttu-id="b9cf8-120">**Propiedad ScriptEngineTimeout**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-120">**ScriptEngineTimeout Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_scriptenginetimeout)
-   [<span data-ttu-id="b9cf8-121">**Propiedad TargetMachine**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-121">**TargetMachine Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_targetmachine)
-   [<span data-ttu-id="b9cf8-122">**Propiedad grabable**</span><span class="sxs-lookup"><span data-stu-id="b9cf8-122">**Writable Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_writable)

 

 



