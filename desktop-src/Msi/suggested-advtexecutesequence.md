---
description: Las secuencias de acción sugeridas para una tabla AdvtExecuteSequence básica en una base de datos Windows Installer.
ms.assetid: 42a55f8f-582a-499b-8a6b-c893da62a4d4
title: AdvtExecuteSequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a672579a174a0cc242ac503225d81976de60d9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678594"
---
# <a name="suggested-advtexecutesequence"></a><span data-ttu-id="ba519-103">AdvtExecuteSequence sugerido</span><span class="sxs-lookup"><span data-stu-id="ba519-103">Suggested AdvtExecuteSequence</span></span>



| <span data-ttu-id="ba519-104">Acción</span><span class="sxs-lookup"><span data-stu-id="ba519-104">Action</span></span>                                                    | <span data-ttu-id="ba519-105">Condición</span><span class="sxs-lookup"><span data-stu-id="ba519-105">Condition</span></span> | <span data-ttu-id="ba519-106">Secuencia</span><span class="sxs-lookup"><span data-stu-id="ba519-106">Sequence</span></span> |
|-----------------------------------------------------------|-----------|----------|
| [<span data-ttu-id="ba519-107">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="ba519-107">CostInitialize</span></span>](costinitialize-action.md)               |           | <span data-ttu-id="ba519-108">800</span><span class="sxs-lookup"><span data-stu-id="ba519-108">800</span></span>      |
| [<span data-ttu-id="ba519-109">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="ba519-109">CostFinalize</span></span>](costfinalize-action.md)                   |           | <span data-ttu-id="ba519-110">1000</span><span class="sxs-lookup"><span data-stu-id="ba519-110">1000</span></span>     |
| [<span data-ttu-id="ba519-111">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="ba519-111">InstallValidate</span></span>](installvalidate-action.md)             |           | <span data-ttu-id="ba519-112">1400</span><span class="sxs-lookup"><span data-stu-id="ba519-112">1400</span></span>     |
| [<span data-ttu-id="ba519-113">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="ba519-113">InstallInitialize</span></span>](installinitialize-action.md)         |           | <span data-ttu-id="ba519-114">1.500</span><span class="sxs-lookup"><span data-stu-id="ba519-114">1500</span></span>     |
| [<span data-ttu-id="ba519-115">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="ba519-115">CreateShortcuts</span></span>](createshortcuts-action.md)             |           | <span data-ttu-id="ba519-116">4500</span><span class="sxs-lookup"><span data-stu-id="ba519-116">4500</span></span>     |
| [<span data-ttu-id="ba519-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ba519-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)         |           | <span data-ttu-id="ba519-118">4600</span><span class="sxs-lookup"><span data-stu-id="ba519-118">4600</span></span>     |
| [<span data-ttu-id="ba519-119">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="ba519-119">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md) |           | <span data-ttu-id="ba519-120">4700</span><span class="sxs-lookup"><span data-stu-id="ba519-120">4700</span></span>     |
| [<span data-ttu-id="ba519-121">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="ba519-121">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)       |           | <span data-ttu-id="ba519-122">4800</span><span class="sxs-lookup"><span data-stu-id="ba519-122">4800</span></span>     |
| [<span data-ttu-id="ba519-123">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="ba519-123">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)           |           | <span data-ttu-id="ba519-124">4900</span><span class="sxs-lookup"><span data-stu-id="ba519-124">4900</span></span>     |
| [<span data-ttu-id="ba519-125">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="ba519-125">PublishComponents</span></span>](publishcomponents-action.md)         |           | <span data-ttu-id="ba519-126">6200</span><span class="sxs-lookup"><span data-stu-id="ba519-126">6200</span></span>     |
| [<span data-ttu-id="ba519-127">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="ba519-127">PublishFeatures</span></span>](publishfeatures-action.md)             |           | <span data-ttu-id="ba519-128">6300</span><span class="sxs-lookup"><span data-stu-id="ba519-128">6300</span></span>     |
| [<span data-ttu-id="ba519-129">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="ba519-129">PublishProduct</span></span>](publishproduct-action.md)               |           | <span data-ttu-id="ba519-130">6400</span><span class="sxs-lookup"><span data-stu-id="ba519-130">6400</span></span>     |
| [<span data-ttu-id="ba519-131">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="ba519-131">InstallFinalize</span></span>](installfinalize-action.md)             |           | <span data-ttu-id="ba519-132">6600</span><span class="sxs-lookup"><span data-stu-id="ba519-132">6600</span></span>     |



 

 

 



