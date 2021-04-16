---
description: La \_ variable miembro m pAlloc es un puntero a la interfaz IMemAllocator del asignador de memoria.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Miembro CPullPin:: m_pAlloc (Pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671383"
---
# <a name="cpullpinm_palloc-member"></a><span data-ttu-id="4d957-103">Miembro pAlloc CPullPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="4d957-103">CPullPin::m\_pAlloc member</span></span>

<span data-ttu-id="4d957-104">La `m_pAlloc` variable miembro es un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="4d957-104">The `m_pAlloc` member variable is a pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d957-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d957-105">Syntax</span></span>


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a><span data-ttu-id="4d957-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d957-106">Remarks</span></span>

<span data-ttu-id="4d957-107">El método [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) establece esta variable miembro.</span><span class="sxs-lookup"><span data-stu-id="4d957-107">The [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) method sets this member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d957-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d957-108">Requirements</span></span>



| <span data-ttu-id="4d957-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d957-109">Requirement</span></span> | <span data-ttu-id="4d957-110">Value</span><span class="sxs-lookup"><span data-stu-id="4d957-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d957-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d957-111">Header</span></span><br/>  | <dl> <span data-ttu-id="4d957-112"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d957-112"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="4d957-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d957-113">Library</span></span><br/> | <dl> <span data-ttu-id="4d957-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4d957-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d957-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d957-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d957-116">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="4d957-116">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




