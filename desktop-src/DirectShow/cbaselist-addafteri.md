---
description: El método AddAfterI inserta un elemento después de la posición especificada.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Método CBaseList. AddAfterI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670949"
---
# <a name="cbaselistaddafteri-method"></a><span data-ttu-id="83065-103">CBaseList. AddAfterI, método</span><span class="sxs-lookup"><span data-stu-id="83065-103">CBaseList.AddAfterI method</span></span>

<span data-ttu-id="83065-104">El `AddAfterI` método inserta un elemento después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="83065-104">The `AddAfterI` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="83065-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83065-105">Syntax</span></span>


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="83065-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83065-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="83065-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="83065-108">Posición detrás de la que se va a agregar el elemento.</span><span class="sxs-lookup"><span data-stu-id="83065-108">Position after which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="83065-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="83065-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="83065-110">Puntero al elemento que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="83065-110">Pointer to the item to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83065-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83065-111">Return value</span></span>

<span data-ttu-id="83065-112">Devuelve el indicador de posición del elemento insertado.</span><span class="sxs-lookup"><span data-stu-id="83065-112">Returns the position indicator of the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="83065-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83065-113">Remarks</span></span>

<span data-ttu-id="83065-114">Si *pos* es **null**, este método agrega el elemento al encabezado de la lista (equivalente a llamar al método [**CBaseList:: AddHeadI**](cbaselist-addheadi.md) ).</span><span class="sxs-lookup"><span data-stu-id="83065-114">If *pos* is **NULL**, this method adds the item to the head of the list (equivalent to calling the [**CBaseList::AddHeadI**](cbaselist-addheadi.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="83065-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83065-115">Requirements</span></span>



| <span data-ttu-id="83065-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="83065-116">Requirement</span></span> | <span data-ttu-id="83065-117">Value</span><span class="sxs-lookup"><span data-stu-id="83065-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83065-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83065-118">Header</span></span><br/>  | <dl> <span data-ttu-id="83065-119"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83065-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="83065-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83065-120">Library</span></span><br/> | <dl> <span data-ttu-id="83065-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="83065-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83065-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="83065-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83065-123">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="83065-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




