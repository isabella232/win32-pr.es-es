---
description: La interfaz IAzAuthorizationStore expone los métodos siguientes.
ms.assetid: ECBCD34B-4AF0-4FED-8E1D-BFD544390804
title: Métodos IAzAuthorizationStore
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c8d71185e9e52d46d1a51e2f2966334a72ad0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668239"
---
# <a name="iazauthorizationstore-methods"></a><span data-ttu-id="b2d0f-103">Métodos IAzAuthorizationStore</span><span class="sxs-lookup"><span data-stu-id="b2d0f-103">IAzAuthorizationStore Methods</span></span>

<span data-ttu-id="b2d0f-104">La interfaz [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b2d0f-104">The [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b2d0f-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b2d0f-105">In this section</span></span>

-   [<span data-ttu-id="b2d0f-106">**Método AddDelegatedPolicyUser**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-106">**AddDelegatedPolicyUser Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser)
-   [<span data-ttu-id="b2d0f-107">**Método AddDelegatedPolicyUserName**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-107">**AddDelegatedPolicyUserName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyusername)
-   [<span data-ttu-id="b2d0f-108">**Método AddPolicyAdministrator**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-108">**AddPolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyadministrator)
-   [<span data-ttu-id="b2d0f-109">**Método AddPolicyAdministratorName**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-109">**AddPolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyadministratorname)
-   [<span data-ttu-id="b2d0f-110">**Método AddPolicyReader**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-110">**AddPolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyreader)
-   [<span data-ttu-id="b2d0f-111">**Método AddPolicyReaderName**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-111">**AddPolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyreadername)
-   [<span data-ttu-id="b2d0f-112">**Método AddPropertyItem**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-112">**AddPropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpropertyitem)
-   [<span data-ttu-id="b2d0f-113">**Método CloseApplication**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-113">**CloseApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-closeapplication)
-   [<span data-ttu-id="b2d0f-114">**Método CreateApplication**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-114">**CreateApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-createapplication)
-   [<span data-ttu-id="b2d0f-115">**Método CreateApplicationGroup**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-115">**CreateApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-createapplicationgroup)
-   [<span data-ttu-id="b2d0f-116">**Delete (método)**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-116">**Delete Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-delete)
-   [<span data-ttu-id="b2d0f-117">**Método DeleteApplication**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-117">**DeleteApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deleteapplication)
-   [<span data-ttu-id="b2d0f-118">**Método DeleteApplicationGroup**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-118">**DeleteApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deleteapplicationgroup)
-   [<span data-ttu-id="b2d0f-119">**Método DeleteDelegatedPolicyUser**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-119">**DeleteDelegatedPolicyUser Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletedelegatedpolicyuser)
-   [<span data-ttu-id="b2d0f-120">**Método DeleteDelegatedPolicyUserName**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-120">**DeleteDelegatedPolicyUserName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletedelegatedpolicyusername)
-   [<span data-ttu-id="b2d0f-121">**Método DeletePolicyAdministrator**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-121">**DeletePolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyadministrator)
-   [<span data-ttu-id="b2d0f-122">**Método DeletePolicyAdministratorName**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-122">**DeletePolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyadministratorname)
-   [<span data-ttu-id="b2d0f-123">**Método DeletePolicyReader**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-123">**DeletePolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyreader)
-   [<span data-ttu-id="b2d0f-124">**Método DeletePolicyReaderName**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-124">**DeletePolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyreadername)
-   [<span data-ttu-id="b2d0f-125">**Método DeletePropertyItem**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-125">**DeletePropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepropertyitem)
-   [<span data-ttu-id="b2d0f-126">**GetProperty (método)**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-126">**GetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-getproperty)
-   [<span data-ttu-id="b2d0f-127">**Método Initialize**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-127">**Initialize Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize)
-   [<span data-ttu-id="b2d0f-128">**Método OpenApplication**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-128">**OpenApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-openapplication)
-   [<span data-ttu-id="b2d0f-129">**Método OpenApplicationGroup**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-129">**OpenApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-openapplicationgroup)
-   [<span data-ttu-id="b2d0f-130">**Método SetProperty**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-130">**SetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-setproperty)
-   [<span data-ttu-id="b2d0f-131">**Submit (método)**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-131">**Submit Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-submit)
-   [<span data-ttu-id="b2d0f-132">**Método UpdateCache**</span><span class="sxs-lookup"><span data-stu-id="b2d0f-132">**UpdateCache Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-updatecache)

 

 



