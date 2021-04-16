---
description: Contiene un grupo de matrices ANDEXP evaluadas como pares.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Estructura de expresión (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666293"
---
# <a name="expression-structure"></a><span data-ttu-id="e3397-103">Estructura de expresión</span><span class="sxs-lookup"><span data-stu-id="e3397-103">EXPRESSION structure</span></span>

<span data-ttu-id="e3397-104">La estructura **Expression** contiene un grupo de matrices **ANDEXP** evaluadas como elementos del mismo nivel en expresiones y lógicas, que tienen el formato</span><span class="sxs-lookup"><span data-stu-id="e3397-104">The **EXPRESSION** structure contains a group of **ANDEXP** arrays evaluated as peers in logical AND expressions, which have the format</span></span>

<span data-ttu-id="e3397-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span><span class="sxs-lookup"><span data-stu-id="e3397-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3397-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3397-106">Syntax</span></span>


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a><span data-ttu-id="e3397-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3397-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3397-108">**nAndExps**</span><span class="sxs-lookup"><span data-stu-id="e3397-108">**nAndExps**</span></span>
</dt> <dd>

<span data-ttu-id="e3397-109">Número de patrones de **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="e3397-109">Number of **ANDEXP** patterns.</span></span>

</dd> <dt>

<span data-ttu-id="e3397-110">**AndExp**</span><span class="sxs-lookup"><span data-stu-id="e3397-110">**AndExp**</span></span>
</dt> <dd>

<span data-ttu-id="e3397-111">Matriz de patrones de **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="e3397-111">Array of **ANDEXP** patterns.</span></span> <span data-ttu-id="e3397-112">El filtro de captura organiza todas las filas de esta matriz como instrucciones y lógicas.</span><span class="sxs-lookup"><span data-stu-id="e3397-112">The capture filter arranges all rows of this array as logical AND statements.</span></span> <span data-ttu-id="e3397-113">Tenga en cuenta que cada estructura de expresión puede contener un máximo de cuatro patrones **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="e3397-113">Be aware that each EXPRESSION structure can contain a maximum of four **ANDEXP** patterns.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3397-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3397-114">Remarks</span></span>

<span data-ttu-id="e3397-115">Para obtener más información sobre la implementación de esta estructura como parte de un filtro de captura, vea [capturar filtros](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e3397-115">For more information about implementing this structure as part of a capture filter, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3397-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3397-116">Requirements</span></span>



| <span data-ttu-id="e3397-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3397-117">Requirement</span></span> | <span data-ttu-id="e3397-118">Value</span><span class="sxs-lookup"><span data-stu-id="e3397-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e3397-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3397-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3397-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e3397-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e3397-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3397-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3397-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3397-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e3397-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3397-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3397-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3397-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3397-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3397-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3397-126">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="e3397-126">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="e3397-127">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="e3397-127">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




