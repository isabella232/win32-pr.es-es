---
description: Puede utilizar las siguientes funciones para trabajar con datos de rendimiento en Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Funciones de contadores de rendimiento para Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909721"
---
# <a name="performance-counters-functions-for-visual-basic"></a><span data-ttu-id="31e07-103">Funciones de contadores de rendimiento para Visual Basic</span><span class="sxs-lookup"><span data-stu-id="31e07-103">Performance Counters Functions for Visual Basic</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31e07-104">Las funciones que se describen en este tema pueden modificarse o no estar disponibles en el futuro.</span><span class="sxs-lookup"><span data-stu-id="31e07-104">The functions that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="31e07-105">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="31e07-105">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="31e07-106">Puede utilizar las siguientes funciones para trabajar con datos de rendimiento en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="31e07-106">You can use the following functions to work with performance data in Visual Basic.</span></span>

- [<span data-ttu-id="31e07-107">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="31e07-107">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="31e07-108">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="31e07-108">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="31e07-109">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="31e07-109">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="31e07-110">**PdhVbAddCounter**</span><span class="sxs-lookup"><span data-stu-id="31e07-110">**PdhVbAddCounter**</span></span>](pdhvbaddcounter.md)
- [<span data-ttu-id="31e07-111">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="31e07-111">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
- [<span data-ttu-id="31e07-112">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="31e07-112">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
- [<span data-ttu-id="31e07-113">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="31e07-113">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
- [<span data-ttu-id="31e07-114">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="31e07-114">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
- [<span data-ttu-id="31e07-115">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="31e07-115">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
- [<span data-ttu-id="31e07-116">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="31e07-116">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
- [<span data-ttu-id="31e07-117">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="31e07-117">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
- [<span data-ttu-id="31e07-118">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="31e07-118">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
- [<span data-ttu-id="31e07-119">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="31e07-119">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
- [<span data-ttu-id="31e07-120">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="31e07-120">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)

> [!NOTE]
> <span data-ttu-id="31e07-121">Las `PdhVb***` funciones funcionan en una sesión por proceso y no son seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="31e07-121">The `PdhVb***` functions work on a per-process session and are not thread-safe.</span></span> <span data-ttu-id="31e07-122">Estas funciones solo deben usarse desde aplicaciones sencillas de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="31e07-122">These functions should only be used from simple single-threaded applications.</span></span>
