---
description: El método GetCurrentSample recupera el ejemplo actual.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Método CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660753"
---
# <a name="cbaserenderergetcurrentsample-method"></a><span data-ttu-id="1b67f-103">CBaseRenderer. GetCurrentSample, método</span><span class="sxs-lookup"><span data-stu-id="1b67f-103">CBaseRenderer.GetCurrentSample method</span></span>

<span data-ttu-id="1b67f-104">El `GetCurrentSample` método recupera el ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="1b67f-104">The `GetCurrentSample` method retrieves the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b67f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b67f-105">Syntax</span></span>


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a><span data-ttu-id="1b67f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b67f-106">Parameters</span></span>

<span data-ttu-id="1b67f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1b67f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b67f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b67f-108">Return value</span></span>

<span data-ttu-id="1b67f-109">Devuelve un puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo, o **null** si no hay ningún ejemplo disponible.</span><span class="sxs-lookup"><span data-stu-id="1b67f-109">Returns a pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface, or **NULL** if no sample is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b67f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b67f-110">Remarks</span></span>

<span data-ttu-id="1b67f-111">A menos que el método devuelva **null**, el método llama a **AddRef** en el puntero [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="1b67f-111">Unless the method returns **NULL**, the method calls **AddRef** on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer before returning it.</span></span> <span data-ttu-id="1b67f-112">El llamador debe liberar el puntero.</span><span class="sxs-lookup"><span data-stu-id="1b67f-112">The caller must release the pointer.</span></span> <span data-ttu-id="1b67f-113">(Por implicación, debe asignar el valor devuelto a una variable para poder publicarlo más adelante).</span><span class="sxs-lookup"><span data-stu-id="1b67f-113">(By implication, you must assign the return value to a variable, so that you can release it later.)</span></span>

## <a name="requirements"></a><span data-ttu-id="1b67f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b67f-114">Requirements</span></span>



| <span data-ttu-id="1b67f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b67f-115">Requirement</span></span> | <span data-ttu-id="1b67f-116">Value</span><span class="sxs-lookup"><span data-stu-id="1b67f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b67f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b67f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1b67f-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b67f-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1b67f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b67f-119">Library</span></span><br/> | <dl> <span data-ttu-id="1b67f-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1b67f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b67f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b67f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b67f-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="1b67f-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




