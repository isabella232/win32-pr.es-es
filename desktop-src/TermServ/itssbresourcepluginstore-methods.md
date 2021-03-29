---
title: Métodos ITsSbResourcePluginStore
description: La interfaz ITsSbResourcePluginStore expone los métodos siguientes.
ms.assetid: D3D59244-E319-47C8-A931-72679C11AC40
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c56d403bc681152a5076d6c219790b452bd749d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903605"
---
# <a name="itssbresourcepluginstore-methods"></a><span data-ttu-id="472ae-103">Métodos ITsSbResourcePluginStore</span><span class="sxs-lookup"><span data-stu-id="472ae-103">ITsSbResourcePluginStore Methods</span></span>

<span data-ttu-id="472ae-104">La interfaz [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="472ae-104">The [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="472ae-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="472ae-105">In this section</span></span>

-   [<span data-ttu-id="472ae-106">**Método AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="472ae-106">**AcquireTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)
-   [<span data-ttu-id="472ae-107">**Método AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="472ae-107">**AddEnvironmentToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)
-   [<span data-ttu-id="472ae-108">**Método AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="472ae-108">**AddSessionToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)
-   [<span data-ttu-id="472ae-109">**Método AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="472ae-109">**AddTargetToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)
-   [<span data-ttu-id="472ae-110">**Método DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="472ae-110">**DeleteTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)
-   [<span data-ttu-id="472ae-111">**Método EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="472ae-111">**EnumerateEnvironments method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)
-   [<span data-ttu-id="472ae-112">**Método EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="472ae-112">**EnumerateFarms method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)
-   [<span data-ttu-id="472ae-113">**Método EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="472ae-113">**EnumerateSessions method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)
-   [<span data-ttu-id="472ae-114">**Método EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="472ae-114">**EnumerateTargets method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)
-   [<span data-ttu-id="472ae-115">**Método GetFarmProperty**</span><span class="sxs-lookup"><span data-stu-id="472ae-115">**GetFarmProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)
-   [<span data-ttu-id="472ae-116">**Método GetServerState**</span><span class="sxs-lookup"><span data-stu-id="472ae-116">**GetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getserverstate)
-   [<span data-ttu-id="472ae-117">**Método QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="472ae-117">**QueryEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)
-   [<span data-ttu-id="472ae-118">**Método QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="472ae-118">**QuerySessionBySessionId method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)
-   [<span data-ttu-id="472ae-119">**Método QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="472ae-119">**QueryTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)
-   [<span data-ttu-id="472ae-120">**Método ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="472ae-120">**ReleaseTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)
-   [<span data-ttu-id="472ae-121">**Método RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="472ae-121">**RemoveEnvironmentFromStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)
-   [<span data-ttu-id="472ae-122">**Método SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="472ae-122">**SaveEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)
-   [<span data-ttu-id="472ae-123">**Método SaveSession**</span><span class="sxs-lookup"><span data-stu-id="472ae-123">**SaveSession method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)
-   [<span data-ttu-id="472ae-124">**Método SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="472ae-124">**SaveTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)
-   [<span data-ttu-id="472ae-125">**Método SetEnvironmentProperty**</span><span class="sxs-lookup"><span data-stu-id="472ae-125">**SetEnvironmentProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)
-   [<span data-ttu-id="472ae-126">**Método SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="472ae-126">**SetEnvironmentPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck)
-   [<span data-ttu-id="472ae-127">**Método SetServerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="472ae-127">**SetServerDrainMode method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverdrainmode)
-   [<span data-ttu-id="472ae-128">**Método SetServerWaitingToStart**</span><span class="sxs-lookup"><span data-stu-id="472ae-128">**SetServerWaitingToStart method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverwaitingtostart)
-   [<span data-ttu-id="472ae-129">**Método SetSessionState**</span><span class="sxs-lookup"><span data-stu-id="472ae-129">**SetSessionState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)
-   [<span data-ttu-id="472ae-130">**Método SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="472ae-130">**SetTargetProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)
-   [<span data-ttu-id="472ae-131">**Método SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="472ae-131">**SetTargetPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)
-   [<span data-ttu-id="472ae-132">**Método SetTargetState**</span><span class="sxs-lookup"><span data-stu-id="472ae-132">**SetTargetState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)
-   [<span data-ttu-id="472ae-133">**Método TestAndSetServerState**</span><span class="sxs-lookup"><span data-stu-id="472ae-133">**TestAndSetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-testandsetserverstate)

 

 




