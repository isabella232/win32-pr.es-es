---
description: 'El método Run notifica al pin que el filtro se está ejecutando ahora. Este método invalida el método CBasePin:: Run.'
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Método CRenderedInputPin. Run (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660696"
---
# <a name="crenderedinputpinrun-method"></a><span data-ttu-id="c597e-104">CRenderedInputPin. Run (método)</span><span class="sxs-lookup"><span data-stu-id="c597e-104">CRenderedInputPin.Run method</span></span>

<span data-ttu-id="c597e-105">El `Run` método notifica al pin que el filtro se está ejecutando ahora.</span><span class="sxs-lookup"><span data-stu-id="c597e-105">The `Run` method notifies the pin that the filter is now running.</span></span> <span data-ttu-id="c597e-106">Este método invalida el método [**CBasePin:: Run**](cbasepin-run.md) .</span><span class="sxs-lookup"><span data-stu-id="c597e-106">This method overrides the [**CBasePin::Run**](cbasepin-run.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c597e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c597e-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="c597e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c597e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c597e-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="c597e-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c597e-110">La hora de inicio que se pasó al método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) del filtro.</span><span class="sxs-lookup"><span data-stu-id="c597e-110">The start time that was passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c597e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c597e-111">Return value</span></span>

<span data-ttu-id="c597e-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c597e-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c597e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c597e-113">Requirements</span></span>



| <span data-ttu-id="c597e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c597e-114">Requirement</span></span> | <span data-ttu-id="c597e-115">Value</span><span class="sxs-lookup"><span data-stu-id="c597e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c597e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c597e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c597e-117"><dt>Amextra. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-117"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c597e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c597e-118">Library</span></span><br/> | <dl> <span data-ttu-id="c597e-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c597e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c597e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c597e-121">**Clase CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="c597e-121">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




