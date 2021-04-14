---
description: La interfaz IWbemClassObject expone los métodos siguientes.
ms.assetid: 20BF7775-89D9-4851-8561-EEBA398A0584
ms.tgt_platform: multiple
title: Métodos IWbemClassObject
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825b3f15f17dca6dd0871bbcae3f531a90c90f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361616"
---
# <a name="iwbemclassobject-methods"></a><span data-ttu-id="7bbf7-103">Métodos IWbemClassObject</span><span class="sxs-lookup"><span data-stu-id="7bbf7-103">IWbemClassObject Methods</span></span>

<span data-ttu-id="7bbf7-104">La interfaz [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-104">The [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7bbf7-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7bbf7-105">In this section</span></span>

-   [<span data-ttu-id="7bbf7-106">**Método BeginEnumeration**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-106">**BeginEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)
-   [<span data-ttu-id="7bbf7-107">**Método BeginMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-107">**BeginMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginmethodenumeration)
-   [<span data-ttu-id="7bbf7-108">**Clone (método)**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-108">**Clone method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)
-   [<span data-ttu-id="7bbf7-109">**CompareTo (método)**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-109">**CompareTo method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-compareto)
-   [<span data-ttu-id="7bbf7-110">**Delete (método)**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-110">**Delete method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)
-   [<span data-ttu-id="7bbf7-111">**Método DeleteMethod**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-111">**DeleteMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-deletemethod)
-   [<span data-ttu-id="7bbf7-112">**Método EndEnumeration**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-112">**EndEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration)
-   [<span data-ttu-id="7bbf7-113">**Método EndMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-113">**EndMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endmethodenumeration)
-   [<span data-ttu-id="7bbf7-114">**Get (método)**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-114">**Get method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)
-   [<span data-ttu-id="7bbf7-115">**GetMethod (método)**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-115">**GetMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)
-   [<span data-ttu-id="7bbf7-116">**Método GetMethodOrigin**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-116">**GetMethodOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodorigin)
-   [<span data-ttu-id="7bbf7-117">**Método GetMethodQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-117">**GetMethodQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)
-   [<span data-ttu-id="7bbf7-118">**GetNames (método)**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-118">**GetNames method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getnames)
-   [<span data-ttu-id="7bbf7-119">**Método GetObjectText**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-119">**GetObjectText method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   [<span data-ttu-id="7bbf7-120">**Método GetPropertyOrigin**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-120">**GetPropertyOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyorigin)
-   [<span data-ttu-id="7bbf7-121">**Método GetPropertyQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-121">**GetPropertyQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)
-   [<span data-ttu-id="7bbf7-122">**Método GetQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-122">**GetQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)
-   [<span data-ttu-id="7bbf7-123">**Método InheritsFrom**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-123">**InheritsFrom method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-inheritsfrom)
-   [<span data-ttu-id="7bbf7-124">**Método Next**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-124">**Next method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-next)
-   [<span data-ttu-id="7bbf7-125">**Método NextMethod**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-125">**NextMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-nextmethod)
-   [<span data-ttu-id="7bbf7-126">**Put (método)**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-126">**Put method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
-   [<span data-ttu-id="7bbf7-127">**Método PutMethod**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-127">**PutMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)
-   [<span data-ttu-id="7bbf7-128">**Método SpawnDerivedClass**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-128">**SpawnDerivedClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)
-   [<span data-ttu-id="7bbf7-129">**Método SpawnInstance**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-129">**SpawnInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

 

 



