---
description: El método AddHeadI agrega un elemento al principio de la lista.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Método CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670941"
---
# <a name="cbaselistaddheadi-method"></a><span data-ttu-id="e7d7f-103">CBaseList. AddHeadI, método</span><span class="sxs-lookup"><span data-stu-id="e7d7f-103">CBaseList.AddHeadI method</span></span>

<span data-ttu-id="e7d7f-104">El `AddHeadI` método agrega un elemento al principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="e7d7f-104">The `AddHeadI` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7d7f-105">Syntax</span></span>


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="e7d7f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7d7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d7f-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="e7d7f-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="e7d7f-108">Puntero al elemento.</span><span class="sxs-lookup"><span data-stu-id="e7d7f-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d7f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7d7f-109">Return value</span></span>

<span data-ttu-id="e7d7f-110">Devuelve un valor de posición que indica la nueva posición del encabezado.</span><span class="sxs-lookup"><span data-stu-id="e7d7f-110">Returns a POSITION value indicating the new head position.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d7f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7d7f-111">Remarks</span></span>

<span data-ttu-id="e7d7f-112">Si se produce un error en el método, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="e7d7f-112">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d7f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7d7f-113">Requirements</span></span>



| <span data-ttu-id="e7d7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7d7f-114">Requirement</span></span> | <span data-ttu-id="e7d7f-115">Value</span><span class="sxs-lookup"><span data-stu-id="e7d7f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d7f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7d7f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e7d7f-117"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7d7f-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e7d7f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7d7f-118">Library</span></span><br/> | <dl> <span data-ttu-id="e7d7f-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e7d7f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d7f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7d7f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d7f-121">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="e7d7f-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




