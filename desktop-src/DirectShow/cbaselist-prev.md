---
description: El método Prev recupera la posición anterior en la lista.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Método CBaseList. PREV (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660664"
---
# <a name="cbaselistprev-method"></a><span data-ttu-id="97137-103">CBaseList. PREV (método)</span><span class="sxs-lookup"><span data-stu-id="97137-103">CBaseList.Prev method</span></span>

<span data-ttu-id="97137-104">El `Prev` método recupera la posición anterior en la lista.</span><span class="sxs-lookup"><span data-stu-id="97137-104">The `Prev` method retrieves the previous position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="97137-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97137-105">Syntax</span></span>


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="97137-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97137-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="97137-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="97137-108">Valor de posición.</span><span class="sxs-lookup"><span data-stu-id="97137-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97137-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97137-109">Return value</span></span>

<span data-ttu-id="97137-110">Devuelve el indicador de posición anterior a la posición especificada en *pos*.</span><span class="sxs-lookup"><span data-stu-id="97137-110">Returns the position indicator that is previous to the position specified in *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="97137-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97137-111">Remarks</span></span>

<span data-ttu-id="97137-112">Si *pos* es la primera posición de la lista, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="97137-112">If *pos* is the first position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="97137-113">Si *pos* es **null**, el método devuelve la última posición de la lista.</span><span class="sxs-lookup"><span data-stu-id="97137-113">If *pos* is **NULL**, the method returns the last position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="97137-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97137-114">Requirements</span></span>



| <span data-ttu-id="97137-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="97137-115">Requirement</span></span> | <span data-ttu-id="97137-116">Value</span><span class="sxs-lookup"><span data-stu-id="97137-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97137-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97137-117">Header</span></span><br/>  | <dl> <span data-ttu-id="97137-118"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97137-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="97137-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97137-119">Library</span></span><br/> | <dl> <span data-ttu-id="97137-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="97137-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97137-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="97137-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97137-122">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="97137-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




