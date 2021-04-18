---
description: La estructura ANDEXP contiene una matriz de coincidencias de patrones que se usan para evaluar los datos de fotogramas.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Estructura ANDEXP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360966"
---
# <a name="andexp-structure"></a><span data-ttu-id="99862-103">Estructura ANDEXP</span><span class="sxs-lookup"><span data-stu-id="99862-103">ANDEXP structure</span></span>

<span data-ttu-id="99862-104">La estructura **ANDEXP** contiene una matriz de coincidencias de patrones que se usan para evaluar los datos de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="99862-104">The **ANDEXP** structure contains an array of pattern matches used to evaluate frame data.</span></span>

## <a name="syntax"></a><span data-ttu-id="99862-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99862-105">Syntax</span></span>


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a><span data-ttu-id="99862-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="99862-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="99862-107">**nPatternMatches**</span><span class="sxs-lookup"><span data-stu-id="99862-107">**nPatternMatches**</span></span>
</dt> <dd>

<span data-ttu-id="99862-108">Número de coincidencias de patrones.</span><span class="sxs-lookup"><span data-stu-id="99862-108">Number of pattern matches.</span></span>

</dd> <dt>

<span data-ttu-id="99862-109">**PatternMatch**</span><span class="sxs-lookup"><span data-stu-id="99862-109">**PatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="99862-110">Matriz de elementos de coincidencia de patrones.</span><span class="sxs-lookup"><span data-stu-id="99862-110">Array of pattern match elements.</span></span> <span data-ttu-id="99862-111">Tenga en cuenta que cada estructura **ANDEXP** puede contener hasta cuatro elementos de coincidencia de patrones.</span><span class="sxs-lookup"><span data-stu-id="99862-111">Note that each **ANDEXP** structure can contain up to four pattern match elements.</span></span> <span data-ttu-id="99862-112">Para obtener más información acerca de este miembro, vea [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="99862-112">For more information about this member, see [Capture Filters](capture-filters.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99862-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99862-113">Remarks</span></span>

<span data-ttu-id="99862-114">Los patrones de la matriz **PatternMatch** \[ Max \_ Patterns \] se unen como elementos del mismo nivel en instrucciones or lógicas con el formato</span><span class="sxs-lookup"><span data-stu-id="99862-114">The patterns in the **PatternMatch**\[MAX\_PATTERNS\] array are joined as peers in logical OR statements in the format</span></span>

<span data-ttu-id="99862-115">(Patrón 1 \| \| Patrón 2 patrón \| \| 3).</span><span class="sxs-lookup"><span data-stu-id="99862-115">(Pattern 1 \|\| Pattern 2 \|\| Pattern 3).</span></span>

<span data-ttu-id="99862-116">Para obtener más información sobre la implementación de esta estructura, vea [Capture filters](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="99862-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md) .</span></span>

## <a name="requirements"></a><span data-ttu-id="99862-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99862-117">Requirements</span></span>



| <span data-ttu-id="99862-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="99862-118">Requirement</span></span> | <span data-ttu-id="99862-119">Value</span><span class="sxs-lookup"><span data-stu-id="99862-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99862-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99862-120">Minimum supported client</span></span><br/> | <span data-ttu-id="99862-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="99862-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="99862-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99862-122">Minimum supported server</span></span><br/> | <span data-ttu-id="99862-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99862-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="99862-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99862-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="99862-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="99862-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99862-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="99862-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99862-127">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="99862-127">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




