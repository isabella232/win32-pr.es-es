---
description: Las secuencias de acción sugeridas para una tabla AdminExecuteSequence básica en una base de datos Windows Installer.
ms.assetid: c54181d3-a16a-4007-a9ac-03ace98b637e
title: AdminExecuteSequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ead890630b397062c6b8e645385b2810fa39d95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542726"
---
# <a name="suggested-adminexecutesequence"></a><span data-ttu-id="60dd2-103">AdminExecuteSequence sugerido</span><span class="sxs-lookup"><span data-stu-id="60dd2-103">Suggested AdminExecuteSequence</span></span>



| <span data-ttu-id="60dd2-104">Acción</span><span class="sxs-lookup"><span data-stu-id="60dd2-104">Action</span></span>                                                | <span data-ttu-id="60dd2-105">Condición</span><span class="sxs-lookup"><span data-stu-id="60dd2-105">Condition</span></span> | <span data-ttu-id="60dd2-106">Secuencia</span><span class="sxs-lookup"><span data-stu-id="60dd2-106">Sequence</span></span> |
|-------------------------------------------------------|-----------|----------|
| [<span data-ttu-id="60dd2-107">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="60dd2-107">CostInitialize</span></span>](costinitialize-action.md)           |           | <span data-ttu-id="60dd2-108">800</span><span class="sxs-lookup"><span data-stu-id="60dd2-108">800</span></span>      |
| [<span data-ttu-id="60dd2-109">FileCost</span><span class="sxs-lookup"><span data-stu-id="60dd2-109">FileCost</span></span>](filecost-action.md)                       |           | <span data-ttu-id="60dd2-110">900</span><span class="sxs-lookup"><span data-stu-id="60dd2-110">900</span></span>      |
| [<span data-ttu-id="60dd2-111">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="60dd2-111">CostFinalize</span></span>](costfinalize-action.md)               |           | <span data-ttu-id="60dd2-112">1000</span><span class="sxs-lookup"><span data-stu-id="60dd2-112">1000</span></span>     |
| [<span data-ttu-id="60dd2-113">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="60dd2-113">InstallValidate</span></span>](installvalidate-action.md)         |           | <span data-ttu-id="60dd2-114">1400</span><span class="sxs-lookup"><span data-stu-id="60dd2-114">1400</span></span>     |
| [<span data-ttu-id="60dd2-115">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="60dd2-115">InstallInitialize</span></span>](installinitialize-action.md)     |           | <span data-ttu-id="60dd2-116">1.500</span><span class="sxs-lookup"><span data-stu-id="60dd2-116">1500</span></span>     |
| [<span data-ttu-id="60dd2-117">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="60dd2-117">InstallAdminPackage</span></span>](installadminpackage-action.md) |           | <span data-ttu-id="60dd2-118">3900</span><span class="sxs-lookup"><span data-stu-id="60dd2-118">3900</span></span>     |
| [<span data-ttu-id="60dd2-119">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="60dd2-119">InstallFiles</span></span>](installfiles-action.md)               |           | <span data-ttu-id="60dd2-120">4000</span><span class="sxs-lookup"><span data-stu-id="60dd2-120">4000</span></span>     |
| [<span data-ttu-id="60dd2-121">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="60dd2-121">InstallFinalize</span></span>](installfinalize-action.md)         |           | <span data-ttu-id="60dd2-122">6600</span><span class="sxs-lookup"><span data-stu-id="60dd2-122">6600</span></span>     |



 

 

 



