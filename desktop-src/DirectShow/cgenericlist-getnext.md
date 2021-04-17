---
description: El método GetNext recupera el elemento en la posición especificada y hace avanzar la posición.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Método CGenericList. GetNext (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671138"
---
# <a name="cgenericlistgetnext-method"></a><span data-ttu-id="d5809-103">CGenericList. GetNext (método)</span><span class="sxs-lookup"><span data-stu-id="d5809-103">CGenericList.GetNext method</span></span>

<span data-ttu-id="d5809-104">El `GetNext` método recupera el elemento en la posición especificada y hace avanzar la posición.</span><span class="sxs-lookup"><span data-stu-id="d5809-104">The `GetNext` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5809-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5809-105">Syntax</span></span>


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="d5809-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5809-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5809-107">*RP* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="d5809-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d5809-108">Referencia a un valor de posición.</span><span class="sxs-lookup"><span data-stu-id="d5809-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5809-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5809-109">Return value</span></span>

<span data-ttu-id="d5809-110">Devuelve un puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="d5809-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5809-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5809-111">Remarks</span></span>

<span data-ttu-id="d5809-112">Este método avanza el indicador de posición hasta la posición siguiente.</span><span class="sxs-lookup"><span data-stu-id="d5809-112">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="d5809-113">Si el indicador de posición se desplaza más allá del final de la lista, el método lo establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="d5809-113">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

<span data-ttu-id="d5809-114">Si *RP* es **null**, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="d5809-114">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5809-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5809-115">Requirements</span></span>



| <span data-ttu-id="d5809-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5809-116">Requirement</span></span> | <span data-ttu-id="d5809-117">Value</span><span class="sxs-lookup"><span data-stu-id="d5809-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5809-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5809-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d5809-119"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5809-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d5809-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5809-120">Library</span></span><br/> | <dl> <span data-ttu-id="d5809-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d5809-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5809-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5809-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5809-123">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="d5809-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




