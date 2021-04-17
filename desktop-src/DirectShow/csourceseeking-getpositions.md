---
description: 'El método GetPositions recupera la posición actual y la posición de detención. Este método implementa el método IMediaSeeking:: GetPositions.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Método CSourceSeeking. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660780"
---
# <a name="csourceseekinggetpositions-method"></a><span data-ttu-id="72538-104">CSourceSeeking. GetPositions, método</span><span class="sxs-lookup"><span data-stu-id="72538-104">CSourceSeeking.GetPositions method</span></span>

<span data-ttu-id="72538-105">El `GetPositions` método recupera la posición actual y la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="72538-105">The `GetPositions` method retrieves the current position and the stop position.</span></span> <span data-ttu-id="72538-106">Este método implementa el método [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="72538-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72538-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72538-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="72538-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72538-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72538-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="72538-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="72538-110">Puntero a una variable que recibe la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="72538-110">Pointer to a variable that receives the start position.</span></span>

</dd> <dt>

<span data-ttu-id="72538-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="72538-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="72538-112">Puntero a una variable que recibe la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="72538-112">Pointer to a variable that receives the stop position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72538-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72538-113">Return value</span></span>

<span data-ttu-id="72538-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="72538-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="72538-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72538-115">Remarks</span></span>

<span data-ttu-id="72538-116">Para el parámetro *pCurrent* , este método devuelve el valor de la variable miembro [**CSourceSeeking:: m \_ rtStart**](csourceseeking-m-rtstart.md) , que representa el tiempo de búsqueda más reciente, no la posición de streaming actual.</span><span class="sxs-lookup"><span data-stu-id="72538-116">For the *pCurrent* parameter, this method returns the value of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) member variable, which represents the latest seek time, not the current streaming position.</span></span> <span data-ttu-id="72538-117">Sin embargo, cuando una aplicación llama a **IMediaSeeking:: GetPositions** a través del administrador de gráficos de filtro, los valores suelen provienen de un filtro de representador, no de un filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="72538-117">However, when an application calls **IMediaSeeking::GetPositions** through the filter graph manager, the values typically come from a renderer filter, not a source filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="72538-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72538-118">Requirements</span></span>



| <span data-ttu-id="72538-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="72538-119">Requirement</span></span> | <span data-ttu-id="72538-120">Value</span><span class="sxs-lookup"><span data-stu-id="72538-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72538-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72538-121">Header</span></span><br/>  | <dl> <span data-ttu-id="72538-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72538-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72538-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72538-123">Library</span></span><br/> | <dl> <span data-ttu-id="72538-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="72538-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72538-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="72538-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72538-126">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="72538-126">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




