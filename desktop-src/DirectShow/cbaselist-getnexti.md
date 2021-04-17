---
description: El método GetNextI recupera el elemento en la posición especificada y hace avanzar la posición.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Método CBaseList. GetNextI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670933"
---
# <a name="cbaselistgetnexti-method"></a><span data-ttu-id="7f666-103">CBaseList. GetNextI, método</span><span class="sxs-lookup"><span data-stu-id="7f666-103">CBaseList.GetNextI method</span></span>

<span data-ttu-id="7f666-104">El `GetNextI` método recupera el elemento en la posición especificada y hace avanzar la posición.</span><span class="sxs-lookup"><span data-stu-id="7f666-104">The `GetNextI` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f666-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f666-105">Syntax</span></span>


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="7f666-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f666-107">*RP* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="7f666-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7f666-108">Referencia a un valor de posición.</span><span class="sxs-lookup"><span data-stu-id="7f666-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f666-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f666-109">Return value</span></span>

<span data-ttu-id="7f666-110">Devuelve un puntero al elemento.</span><span class="sxs-lookup"><span data-stu-id="7f666-110">Returns a pointer to the item.</span></span> <span data-ttu-id="7f666-111">Si *RP* es **null**, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="7f666-111">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f666-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f666-112">Remarks</span></span>

<span data-ttu-id="7f666-113">Este método avanza el indicador de posición hasta la posición siguiente.</span><span class="sxs-lookup"><span data-stu-id="7f666-113">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="7f666-114">Si el indicador de posición se desplaza más allá del final de la lista, el método lo establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="7f666-114">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f666-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f666-115">Requirements</span></span>



| <span data-ttu-id="7f666-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f666-116">Requirement</span></span> | <span data-ttu-id="7f666-117">Value</span><span class="sxs-lookup"><span data-stu-id="7f666-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f666-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f666-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7f666-119"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f666-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7f666-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f666-120">Library</span></span><br/> | <dl> <span data-ttu-id="7f666-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7f666-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f666-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f666-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f666-123">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="7f666-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




