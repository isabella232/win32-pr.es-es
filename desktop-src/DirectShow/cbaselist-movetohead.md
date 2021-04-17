---
description: El método MoveToHead divide la lista e inserta la parte del final en el encabezado de otra lista.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Método CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670928"
---
# <a name="cbaselistmovetohead-method"></a><span data-ttu-id="047f6-103">CBaseList. MoveToHead, método</span><span class="sxs-lookup"><span data-stu-id="047f6-103">CBaseList.MoveToHead method</span></span>

<span data-ttu-id="047f6-104">El `MoveToHead` método divide la lista e inserta la parte del final en el encabezado de otra lista.</span><span class="sxs-lookup"><span data-stu-id="047f6-104">The `MoveToHead` method splits the list and inserts the tail portion at the head of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="047f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="047f6-105">Syntax</span></span>


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="047f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="047f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="047f6-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="047f6-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="047f6-108">Indicador de posición que marca la división en la lista.</span><span class="sxs-lookup"><span data-stu-id="047f6-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="047f6-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="047f6-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="047f6-110">Puntero a otra lista.</span><span class="sxs-lookup"><span data-stu-id="047f6-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="047f6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="047f6-111">Return value</span></span>

<span data-ttu-id="047f6-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="047f6-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="047f6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="047f6-113">Remarks</span></span>

<span data-ttu-id="047f6-114">Este método divide la lista antes de la posición especificada por el parámetro *pos* .</span><span class="sxs-lookup"><span data-stu-id="047f6-114">This method splits the list before the position specified by the *pos* parameter.</span></span> <span data-ttu-id="047f6-115">La parte del encabezado permanece en la lista.</span><span class="sxs-lookup"><span data-stu-id="047f6-115">The head portion remains in the list.</span></span> <span data-ttu-id="047f6-116">La parte del final se inserta en el encabezado de la otra lista.</span><span class="sxs-lookup"><span data-stu-id="047f6-116">The tail portion is inserted at the head of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="047f6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="047f6-117">Requirements</span></span>



| <span data-ttu-id="047f6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="047f6-118">Requirement</span></span> | <span data-ttu-id="047f6-119">Value</span><span class="sxs-lookup"><span data-stu-id="047f6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047f6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="047f6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="047f6-121"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="047f6-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="047f6-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="047f6-122">Library</span></span><br/> | <dl> <span data-ttu-id="047f6-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="047f6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047f6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="047f6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047f6-125">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="047f6-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




