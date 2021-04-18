---
description: El método AddBeforeI inserta un elemento antes de la posición especificada.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Método CBaseList. AddBeforeI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670945"
---
# <a name="cbaselistaddbeforei-method"></a><span data-ttu-id="c1ac1-103">CBaseList. AddBeforeI, método</span><span class="sxs-lookup"><span data-stu-id="c1ac1-103">CBaseList.AddBeforeI method</span></span>

<span data-ttu-id="c1ac1-104">El `AddBeforeI` método inserta un elemento antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="c1ac1-104">The `AddBeforeI` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ac1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1ac1-105">Syntax</span></span>


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="c1ac1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1ac1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ac1-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="c1ac1-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ac1-108">Posición antes de la que se va a agregar el elemento.</span><span class="sxs-lookup"><span data-stu-id="c1ac1-108">Position before which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="c1ac1-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="c1ac1-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ac1-110">Puntero al elemento.</span><span class="sxs-lookup"><span data-stu-id="c1ac1-110">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1ac1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1ac1-111">Return value</span></span>

<span data-ttu-id="c1ac1-112">Devuelve el indicador de posición del elemento insertado.</span><span class="sxs-lookup"><span data-stu-id="c1ac1-112">Returns the position indicator for the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1ac1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1ac1-113">Remarks</span></span>

<span data-ttu-id="c1ac1-114">Si *pos* es **null**, este método agrega el elemento al final de la lista (equivalente a llamar al método [**CBaseList:: AddTailI**](cbaselist-addtaili.md) ).</span><span class="sxs-lookup"><span data-stu-id="c1ac1-114">If *pos* is **NULL**, this method adds the item to the tail of the list (equivalent to calling the [**CBaseList::AddTailI**](cbaselist-addtaili.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1ac1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1ac1-115">Requirements</span></span>



| <span data-ttu-id="c1ac1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1ac1-116">Requirement</span></span> | <span data-ttu-id="c1ac1-117">Value</span><span class="sxs-lookup"><span data-stu-id="c1ac1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ac1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1ac1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c1ac1-119"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1ac1-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c1ac1-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1ac1-120">Library</span></span><br/> | <dl> <span data-ttu-id="c1ac1-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c1ac1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1ac1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1ac1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ac1-123">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="c1ac1-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




