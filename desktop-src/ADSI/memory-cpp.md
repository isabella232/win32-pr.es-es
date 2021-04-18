---
title: Memoria. CPP
description: En el componente de proveedor de ejemplo, un ejemplo de código que muestra la asignación y liberación de memoria se encuentra en Memory. cpp. En la tabla siguiente se enumeran las rutinas admitidas.
ms.assetid: dc5b3559-02fc-45e8-bbd0-482e4e3a7f8a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9add77dcdbbfc0ddab547cd537b352c9a68bdaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656163"
---
# <a name="memorycpp"></a><span data-ttu-id="05475-104">Memoria. CPP</span><span class="sxs-lookup"><span data-stu-id="05475-104">MEMORY.CPP</span></span>

<span data-ttu-id="05475-105">En el componente de proveedor de ejemplo, un ejemplo de código que muestra la asignación y liberación de memoria se encuentra en Memory. cpp.</span><span class="sxs-lookup"><span data-stu-id="05475-105">In the example provider component, a code example showing memory allocation and freeing is in memory.cpp.</span></span> <span data-ttu-id="05475-106">En la tabla siguiente se enumeran las rutinas admitidas.</span><span class="sxs-lookup"><span data-stu-id="05475-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="05475-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="05475-107">Item</span></span>                | <span data-ttu-id="05475-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="05475-108">Description</span></span>                                                           |
|---------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="05475-109">**AllocProvMem**</span><span class="sxs-lookup"><span data-stu-id="05475-109">**AllocProvMem**</span></span>    | <span data-ttu-id="05475-110">Asigna la memoria especificada.</span><span class="sxs-lookup"><span data-stu-id="05475-110">Allocate specified memory.</span></span>                                            |
| <span data-ttu-id="05475-111">**FreeProvMem**</span><span class="sxs-lookup"><span data-stu-id="05475-111">**FreeProvMem**</span></span>     | <span data-ttu-id="05475-112">Memoria libre indicada.</span><span class="sxs-lookup"><span data-stu-id="05475-112">Free memory indicated.</span></span>                                                |
| <span data-ttu-id="05475-113">**ReallocProvMem**</span><span class="sxs-lookup"><span data-stu-id="05475-113">**ReallocProvMem**</span></span>  | <span data-ttu-id="05475-114">Asigne memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="05475-114">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="05475-115">**AllocProvStr**</span><span class="sxs-lookup"><span data-stu-id="05475-115">**AllocProvStr**</span></span>    | <span data-ttu-id="05475-116">Asigne una cadena LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="05475-116">Allocate an LPWSTR string.</span></span>                                            |
| <span data-ttu-id="05475-117">**FreeProvStr**</span><span class="sxs-lookup"><span data-stu-id="05475-117">**FreeProvStr**</span></span>     | <span data-ttu-id="05475-118">Cadena libre si aún no se ha liberado.</span><span class="sxs-lookup"><span data-stu-id="05475-118">Free string if not already freed.</span></span>                                     |
| <span data-ttu-id="05475-119">**ReallocProvStr**</span><span class="sxs-lookup"><span data-stu-id="05475-119">**ReallocProvStr**</span></span>  | <span data-ttu-id="05475-120">Asigne memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="05475-120">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="05475-121">**ProvAllocString**</span><span class="sxs-lookup"><span data-stu-id="05475-121">**ProvAllocString**</span></span> | <span data-ttu-id="05475-122">Comprueba la cadena y el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="05475-122">Verifies string and first parameter.</span></span> <span data-ttu-id="05475-123">Si es correcto, realiza la asignación.</span><span class="sxs-lookup"><span data-stu-id="05475-123">If OK, then performs allocation.</span></span> |



 

 

 




