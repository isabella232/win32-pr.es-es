---
description: Funciones de ruta de acceso
ms.assetid: 0105FC65-332B-4F99-9629-F3DFEAD97535
title: Funciones de ruta de acceso (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12265e9b1dd51f8e2ea5bc0cc384bf227b8cd041
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985642"
---
# <a name="path-functions-the-windows-shell"></a><span data-ttu-id="adf3e-103">Funciones de ruta de acceso (Shell de Windows)</span><span class="sxs-lookup"><span data-stu-id="adf3e-103">Path Functions (The Windows Shell)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="adf3e-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="adf3e-104">In this section</span></span>

-   [<span data-ttu-id="adf3e-105">**PathAllocCanonicalize**</span><span class="sxs-lookup"><span data-stu-id="adf3e-105">**PathAllocCanonicalize**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathalloccanonicalize)
-   [<span data-ttu-id="adf3e-106">**PathAllocCombine**</span><span class="sxs-lookup"><span data-stu-id="adf3e-106">**PathAllocCombine**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathalloccombine)
-   [<span data-ttu-id="adf3e-107">**PathCchAddBackslash**</span><span class="sxs-lookup"><span data-stu-id="adf3e-107">**PathCchAddBackslash**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash)
-   [<span data-ttu-id="adf3e-108">**PathCchAddBackslashEx**</span><span class="sxs-lookup"><span data-stu-id="adf3e-108">**PathCchAddBackslashEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex)
-   [<span data-ttu-id="adf3e-109">**PathCchAddExtension**</span><span class="sxs-lookup"><span data-stu-id="adf3e-109">**PathCchAddExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension)
-   [<span data-ttu-id="adf3e-110">**PathCchAppend**</span><span class="sxs-lookup"><span data-stu-id="adf3e-110">**PathCchAppend**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchappend)
-   [<span data-ttu-id="adf3e-111">**PathCchAppendEx**</span><span class="sxs-lookup"><span data-stu-id="adf3e-111">**PathCchAppendEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex)
-   [<span data-ttu-id="adf3e-112">**PathCchCanonicalize**</span><span class="sxs-lookup"><span data-stu-id="adf3e-112">**PathCchCanonicalize**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize)
-   [<span data-ttu-id="adf3e-113">**PathCchCanonicalizeEx**</span><span class="sxs-lookup"><span data-stu-id="adf3e-113">**PathCchCanonicalizeEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex)
-   [<span data-ttu-id="adf3e-114">**PathCchCombine**</span><span class="sxs-lookup"><span data-stu-id="adf3e-114">**PathCchCombine**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine)
-   [<span data-ttu-id="adf3e-115">**PathCchCombineEx**</span><span class="sxs-lookup"><span data-stu-id="adf3e-115">**PathCchCombineEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex)
-   [<span data-ttu-id="adf3e-116">**PathCchFindExtension**</span><span class="sxs-lookup"><span data-stu-id="adf3e-116">**PathCchFindExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchfindextension)
-   [<span data-ttu-id="adf3e-117">**PathCchIsRoot**</span><span class="sxs-lookup"><span data-stu-id="adf3e-117">**PathCchIsRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchisroot)
-   [<span data-ttu-id="adf3e-118">**PathCchRemoveBackslash**</span><span class="sxs-lookup"><span data-stu-id="adf3e-118">**PathCchRemoveBackslash**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash)
-   [<span data-ttu-id="adf3e-119">**PathCchRemoveBackslashEx**</span><span class="sxs-lookup"><span data-stu-id="adf3e-119">**PathCchRemoveBackslashEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex)
-   [<span data-ttu-id="adf3e-120">**PathCchRemoveExtension**</span><span class="sxs-lookup"><span data-stu-id="adf3e-120">**PathCchRemoveExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension)
-   [<span data-ttu-id="adf3e-121">**PathCchRemoveFileSpec**</span><span class="sxs-lookup"><span data-stu-id="adf3e-121">**PathCchRemoveFileSpec**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec)
-   [<span data-ttu-id="adf3e-122">**PathCchRenameExtension**</span><span class="sxs-lookup"><span data-stu-id="adf3e-122">**PathCchRenameExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension)
-   [<span data-ttu-id="adf3e-123">**PathCchSkipRoot**</span><span class="sxs-lookup"><span data-stu-id="adf3e-123">**PathCchSkipRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchskiproot)
-   [<span data-ttu-id="adf3e-124">**PathCchStripPrefix**</span><span class="sxs-lookup"><span data-stu-id="adf3e-124">**PathCchStripPrefix**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchstripprefix)
-   [<span data-ttu-id="adf3e-125">**PathCchStripToRoot**</span><span class="sxs-lookup"><span data-stu-id="adf3e-125">**PathCchStripToRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot)
-   [<span data-ttu-id="adf3e-126">**PathIsUNCEx**</span><span class="sxs-lookup"><span data-stu-id="adf3e-126">**PathIsUNCEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathisuncex)

 

 



