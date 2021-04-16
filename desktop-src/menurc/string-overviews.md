---
title: Funciones strsafe
description: .
ms.assetid: 3590dd8d-3a88-4dde-a5fe-f10e12354919
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b31824788b68a7ec789c6d274b2a368eda1cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665811"
---
# <a name="strsafe-functions"></a><span data-ttu-id="0d3d3-103">Funciones strsafe</span><span class="sxs-lookup"><span data-stu-id="0d3d3-103">Strsafe Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0d3d3-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0d3d3-104">In this section</span></span>

-   [<span data-ttu-id="0d3d3-105">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-105">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)
-   [<span data-ttu-id="0d3d3-106">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-106">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)
-   [<span data-ttu-id="0d3d3-107">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-107">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)
-   [<span data-ttu-id="0d3d3-108">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-108">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)
-   [<span data-ttu-id="0d3d3-109">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-109">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)
-   [<span data-ttu-id="0d3d3-110">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-110">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)
-   [<span data-ttu-id="0d3d3-111">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-111">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)
-   [<span data-ttu-id="0d3d3-112">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-112">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)
-   [<span data-ttu-id="0d3d3-113">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-113">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)
-   [<span data-ttu-id="0d3d3-114">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-114">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)
-   [<span data-ttu-id="0d3d3-115">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-115">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)
-   [<span data-ttu-id="0d3d3-116">**StringCbPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-116">**StringCbPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_la)
-   [<span data-ttu-id="0d3d3-117">**\_Lex StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-117">**StringCbPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_lexa)
-   [<span data-ttu-id="0d3d3-118">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-118">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)
-   [<span data-ttu-id="0d3d3-119">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-119">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)
-   [<span data-ttu-id="0d3d3-120">**StringCbVPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-120">**StringCbVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_la)
-   [<span data-ttu-id="0d3d3-121">**\_Lex StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-121">**StringCbVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_lexa)
-   [<span data-ttu-id="0d3d3-122">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-122">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)
-   [<span data-ttu-id="0d3d3-123">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-123">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)
-   [<span data-ttu-id="0d3d3-124">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-124">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)
-   [<span data-ttu-id="0d3d3-125">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-125">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)
-   [<span data-ttu-id="0d3d3-126">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-126">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)
-   [<span data-ttu-id="0d3d3-127">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-127">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)
-   [<span data-ttu-id="0d3d3-128">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-128">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)
-   [<span data-ttu-id="0d3d3-129">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-129">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)
-   [<span data-ttu-id="0d3d3-130">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-130">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)
-   [<span data-ttu-id="0d3d3-131">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-131">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)
-   [<span data-ttu-id="0d3d3-132">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-132">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)
-   [<span data-ttu-id="0d3d3-133">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-133">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)
-   [<span data-ttu-id="0d3d3-134">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-134">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)
-   [<span data-ttu-id="0d3d3-135">**StringCchPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-135">**StringCchPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_la)
-   [<span data-ttu-id="0d3d3-136">**\_Lex StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-136">**StringCchPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_lexa)
-   [<span data-ttu-id="0d3d3-137">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-137">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)
-   [<span data-ttu-id="0d3d3-138">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-138">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)
-   [<span data-ttu-id="0d3d3-139">**StringCchVPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-139">**StringCchVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_la)
-   [<span data-ttu-id="0d3d3-140">**\_Lex StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-140">**StringCchVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_lexa)
-   [<span data-ttu-id="0d3d3-141">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-141">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)
-   [<span data-ttu-id="0d3d3-142">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="0d3d3-142">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)
-   <span data-ttu-id="0d3d3-143">[**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d3d3-143">[**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span></span>
-   <span data-ttu-id="0d3d3-144">[**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d3d3-144">[**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span></span>

 

 