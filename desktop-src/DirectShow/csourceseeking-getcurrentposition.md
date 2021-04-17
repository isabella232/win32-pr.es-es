---
description: El método GetCurrentPosition recupera la posición actual, en relación con la duración total de la secuencia. Sin implementar.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Método CSourceSeeking. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660784"
---
# <a name="csourceseekinggetcurrentposition-method"></a><span data-ttu-id="8797b-104">CSourceSeeking. GetCurrentPosition, método</span><span class="sxs-lookup"><span data-stu-id="8797b-104">CSourceSeeking.GetCurrentPosition method</span></span>

<span data-ttu-id="8797b-105">El `GetCurrentPosition` método recupera la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8797b-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="8797b-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="8797b-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="8797b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8797b-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="8797b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8797b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8797b-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="8797b-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="8797b-110">Puntero a una variable que recibe la posición actual, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="8797b-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8797b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8797b-111">Return value</span></span>

<span data-ttu-id="8797b-112">Devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="8797b-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8797b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8797b-113">Remarks</span></span>

<span data-ttu-id="8797b-114">Normalmente, los filtros de origen no admiten este método.</span><span class="sxs-lookup"><span data-stu-id="8797b-114">Source filters typically do not support this method.</span></span> <span data-ttu-id="8797b-115">En su lugar, los filtros de representador notifican la posición actual a través de la clase [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="8797b-115">Instead, renderer filters report the current position through the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="8797b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8797b-116">Requirements</span></span>



| <span data-ttu-id="8797b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8797b-117">Requirement</span></span> | <span data-ttu-id="8797b-118">Value</span><span class="sxs-lookup"><span data-stu-id="8797b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8797b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8797b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8797b-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8797b-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8797b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8797b-121">Library</span></span><br/> | <dl> <span data-ttu-id="8797b-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8797b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8797b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8797b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8797b-124">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="8797b-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




