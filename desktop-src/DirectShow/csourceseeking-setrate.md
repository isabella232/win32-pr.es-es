---
description: 'El método SetRate establece la velocidad de reproducción. Este método implementa el método IMediaSeeking:: SetRate.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Método CSourceSeeking. SetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690466"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="d0f6f-104">CSourceSeeking. SetRate, método</span><span class="sxs-lookup"><span data-stu-id="d0f6f-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="d0f6f-105">El `SetRate` método establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d0f6f-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="d0f6f-106">Este método implementa el método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="d0f6f-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f6f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0f6f-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="d0f6f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0f6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f6f-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="d0f6f-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d0f6f-110">Velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d0f6f-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f6f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0f6f-111">Return value</span></span>

<span data-ttu-id="d0f6f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0f6f-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f6f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0f6f-113">Remarks</span></span>

<span data-ttu-id="d0f6f-114">Este método actualiza el valor de la variable miembro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) y, a continuación, llama al método virtual puro [**CSourceSeeking:: ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="d0f6f-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="d0f6f-115">El método no valida el parámetro *dRate* .</span><span class="sxs-lookup"><span data-stu-id="d0f6f-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f6f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0f6f-116">Requirements</span></span>



| <span data-ttu-id="d0f6f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f6f-117">Requirement</span></span> | <span data-ttu-id="d0f6f-118">Value</span><span class="sxs-lookup"><span data-stu-id="d0f6f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f6f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0f6f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d0f6f-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0f6f-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0f6f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0f6f-121">Library</span></span><br/> | <dl> <span data-ttu-id="d0f6f-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d0f6f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f6f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0f6f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f6f-124">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="d0f6f-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




