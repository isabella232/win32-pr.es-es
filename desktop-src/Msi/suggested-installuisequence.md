---
description: Las secuencias de acción sugeridas para una tabla InstalUISequence básica en una base de datos Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652734"
---
# <a name="suggested-installuisequence"></a><span data-ttu-id="0f5b9-103">InstallUISequence sugerido</span><span class="sxs-lookup"><span data-stu-id="0f5b9-103">Suggested InstallUISequence</span></span>



| <span data-ttu-id="0f5b9-104">Acción</span><span class="sxs-lookup"><span data-stu-id="0f5b9-104">Action</span></span>                                          | <span data-ttu-id="0f5b9-105">Condición</span><span class="sxs-lookup"><span data-stu-id="0f5b9-105">Condition</span></span>                                                                                                  | <span data-ttu-id="0f5b9-106">Secuencia</span><span class="sxs-lookup"><span data-stu-id="0f5b9-106">Sequence</span></span> |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="0f5b9-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-107">FatalErrorDlg</span></span>                                   |                                                                                                            | <span data-ttu-id="0f5b9-108">-3</span><span class="sxs-lookup"><span data-stu-id="0f5b9-108">-3</span></span>       |
| <span data-ttu-id="0f5b9-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-109">UserExitDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="0f5b9-110">-2</span><span class="sxs-lookup"><span data-stu-id="0f5b9-110">-2</span></span>       |
| <span data-ttu-id="0f5b9-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-111">ExitDlg</span></span>                                         |                                                                                                            | <span data-ttu-id="0f5b9-112">-1</span><span class="sxs-lookup"><span data-stu-id="0f5b9-112">-1</span></span>       |
| [<span data-ttu-id="0f5b9-113">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="0f5b9-113">LaunchConditions</span></span>](launchconditions-action.md) |                                                                                                            | <span data-ttu-id="0f5b9-114">100</span><span class="sxs-lookup"><span data-stu-id="0f5b9-114">100</span></span>      |
| <span data-ttu-id="0f5b9-115">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-115">PrepareDlg</span></span>                                      |                                                                                                            | <span data-ttu-id="0f5b9-116">140</span><span class="sxs-lookup"><span data-stu-id="0f5b9-116">140</span></span>      |
| [<span data-ttu-id="0f5b9-117">AppSearch</span><span class="sxs-lookup"><span data-stu-id="0f5b9-117">AppSearch</span></span>](appsearch-action.md)               |                                                                                                            | <span data-ttu-id="0f5b9-118">400</span><span class="sxs-lookup"><span data-stu-id="0f5b9-118">400</span></span>      |
| [<span data-ttu-id="0f5b9-119">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="0f5b9-119">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="0f5b9-120">NO [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="0f5b9-120">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="0f5b9-121">500</span><span class="sxs-lookup"><span data-stu-id="0f5b9-121">500</span></span>      |
| [<span data-ttu-id="0f5b9-122">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="0f5b9-122">RMCCPSearch</span></span>](rmccpsearch-action.md)           | <span data-ttu-id="0f5b9-123">NO [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="0f5b9-123">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="0f5b9-124">600</span><span class="sxs-lookup"><span data-stu-id="0f5b9-124">600</span></span>      |
| [<span data-ttu-id="0f5b9-125">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="0f5b9-125">CostInitialize</span></span>](costinitialize-action.md)     |                                                                                                            | <span data-ttu-id="0f5b9-126">800</span><span class="sxs-lookup"><span data-stu-id="0f5b9-126">800</span></span>      |
| [<span data-ttu-id="0f5b9-127">FileCost</span><span class="sxs-lookup"><span data-stu-id="0f5b9-127">FileCost</span></span>](filecost-action.md)                 |                                                                                                            | <span data-ttu-id="0f5b9-128">900</span><span class="sxs-lookup"><span data-stu-id="0f5b9-128">900</span></span>      |
| [<span data-ttu-id="0f5b9-129">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="0f5b9-129">CostFinalize</span></span>](costfinalize-action.md)         |                                                                                                            | <span data-ttu-id="0f5b9-130">1000</span><span class="sxs-lookup"><span data-stu-id="0f5b9-130">1000</span></span>     |
| <span data-ttu-id="0f5b9-131">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-131">WelcomeDlg</span></span>                                      | <span data-ttu-id="0f5b9-132">NO [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="0f5b9-132">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="0f5b9-133">1230</span><span class="sxs-lookup"><span data-stu-id="0f5b9-133">1230</span></span>     |
| <span data-ttu-id="0f5b9-134">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-134">ResumeDlg</span></span>                                       | <span data-ttu-id="0f5b9-135">[**Instalado**](installed.md) Y ( [**reanudar**](resume.md) o [**preseleccionar**](preselected.md))</span><span class="sxs-lookup"><span data-stu-id="0f5b9-135">[**Installed**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))</span></span>       | <span data-ttu-id="0f5b9-136">1240</span><span class="sxs-lookup"><span data-stu-id="0f5b9-136">1240</span></span>     |
| <span data-ttu-id="0f5b9-137">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-137">MaintenanceWelcomeDlg</span></span>                           | <span data-ttu-id="0f5b9-138">[**Instalado**](installed.md) Y no se [**reanudan**](resume.md) y no se [**preseleccionan**](preselected.md)</span><span class="sxs-lookup"><span data-stu-id="0f5b9-138">[**Installed**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md)</span></span> | <span data-ttu-id="0f5b9-139">1250</span><span class="sxs-lookup"><span data-stu-id="0f5b9-139">1250</span></span>     |
| <span data-ttu-id="0f5b9-140">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="0f5b9-140">ProgressDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="0f5b9-141">1280</span><span class="sxs-lookup"><span data-stu-id="0f5b9-141">1280</span></span>     |
| [<span data-ttu-id="0f5b9-142">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="0f5b9-142">ExecuteAction</span></span>](executeaction-action.md)       |                                                                                                            | <span data-ttu-id="0f5b9-143">1300</span><span class="sxs-lookup"><span data-stu-id="0f5b9-143">1300</span></span>     |



 

 

 



