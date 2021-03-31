---
description: Las secuencias de acción sugeridas para una tabla AdminUISequence básica en una base de datos Windows Installer.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: AdminUISequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812698"
---
# <a name="suggested-adminuisequence"></a><span data-ttu-id="77279-103">AdminUISequence sugerido</span><span class="sxs-lookup"><span data-stu-id="77279-103">Suggested AdminUISequence</span></span>



| <span data-ttu-id="77279-104">Acción</span><span class="sxs-lookup"><span data-stu-id="77279-104">Action</span></span>                                      | <span data-ttu-id="77279-105">Condición</span><span class="sxs-lookup"><span data-stu-id="77279-105">Condition</span></span> | <span data-ttu-id="77279-106">Secuencia</span><span class="sxs-lookup"><span data-stu-id="77279-106">Sequence</span></span> |
|---------------------------------------------|-----------|----------|
| <span data-ttu-id="77279-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="77279-107">FatalErrorDlg</span></span>                               |           | <span data-ttu-id="77279-108">-3</span><span class="sxs-lookup"><span data-stu-id="77279-108">-3</span></span>       |
| <span data-ttu-id="77279-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="77279-109">UserExitDlg</span></span>                                 |           | <span data-ttu-id="77279-110">-2</span><span class="sxs-lookup"><span data-stu-id="77279-110">-2</span></span>       |
| <span data-ttu-id="77279-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="77279-111">ExitDlg</span></span>                                     |           | <span data-ttu-id="77279-112">-1</span><span class="sxs-lookup"><span data-stu-id="77279-112">-1</span></span>       |
| <span data-ttu-id="77279-113">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="77279-113">PrepareDlg</span></span>                                  |           | <span data-ttu-id="77279-114">140</span><span class="sxs-lookup"><span data-stu-id="77279-114">140</span></span>      |
| [<span data-ttu-id="77279-115">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="77279-115">CostInitialize</span></span>](costinitialize-action.md) |           | <span data-ttu-id="77279-116">800</span><span class="sxs-lookup"><span data-stu-id="77279-116">800</span></span>      |
| [<span data-ttu-id="77279-117">FileCost</span><span class="sxs-lookup"><span data-stu-id="77279-117">FileCost</span></span>](filecost-action.md)             |           | <span data-ttu-id="77279-118">900</span><span class="sxs-lookup"><span data-stu-id="77279-118">900</span></span>      |
| [<span data-ttu-id="77279-119">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="77279-119">CostFinalize</span></span>](costfinalize-action.md)     |           | <span data-ttu-id="77279-120">1000</span><span class="sxs-lookup"><span data-stu-id="77279-120">1000</span></span>     |
| <span data-ttu-id="77279-121">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="77279-121">AdminWelcomeDlg</span></span>                             |           | <span data-ttu-id="77279-122">1230</span><span class="sxs-lookup"><span data-stu-id="77279-122">1230</span></span>     |
| <span data-ttu-id="77279-123">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="77279-123">ProgressDlg</span></span>                                 |           | <span data-ttu-id="77279-124">1280</span><span class="sxs-lookup"><span data-stu-id="77279-124">1280</span></span>     |
| [<span data-ttu-id="77279-125">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="77279-125">ExecuteAction</span></span>](executeaction-action.md)   |           | <span data-ttu-id="77279-126">1300</span><span class="sxs-lookup"><span data-stu-id="77279-126">1300</span></span>     |



 

 

 



