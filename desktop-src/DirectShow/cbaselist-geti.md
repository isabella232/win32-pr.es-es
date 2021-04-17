---
description: El método GetI recupera el elemento en la posición especificada.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Método CBaseList. GetI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660671"
---
# <a name="cbaselistgeti-method"></a><span data-ttu-id="69664-103">CBaseList. GetI, método</span><span class="sxs-lookup"><span data-stu-id="69664-103">CBaseList.GetI method</span></span>

<span data-ttu-id="69664-104">El `GetI` método recupera el elemento en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="69664-104">The `GetI` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="69664-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69664-105">Syntax</span></span>


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="69664-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69664-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69664-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="69664-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="69664-108">Indicador de posición del elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="69664-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69664-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69664-109">Return value</span></span>

<span data-ttu-id="69664-110">Devuelve un puntero al elemento.</span><span class="sxs-lookup"><span data-stu-id="69664-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="69664-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69664-111">Remarks</span></span>

<span data-ttu-id="69664-112">Si *pos* es **null**, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="69664-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="69664-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69664-113">Requirements</span></span>



| <span data-ttu-id="69664-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="69664-114">Requirement</span></span> | <span data-ttu-id="69664-115">Value</span><span class="sxs-lookup"><span data-stu-id="69664-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69664-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69664-116">Header</span></span><br/>  | <dl> <span data-ttu-id="69664-117"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69664-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="69664-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69664-118">Library</span></span><br/> | <dl> <span data-ttu-id="69664-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="69664-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69664-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="69664-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69664-121">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="69664-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




