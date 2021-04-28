---
description: 'Método CSourceSeeking.SetRate: el método SetRate establece la velocidad de reproducción. Este método implementa el método IMediaSeeking::SetRate.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Método CSourceSeeking.SetRate (Ctlutil.h)
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
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098743"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="352ba-104">Método CSourceSeeking.SetRate</span><span class="sxs-lookup"><span data-stu-id="352ba-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="352ba-105">El `SetRate` método establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="352ba-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="352ba-106">Este método implementa el [**método IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)</span><span class="sxs-lookup"><span data-stu-id="352ba-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="352ba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="352ba-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="352ba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="352ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352ba-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="352ba-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="352ba-110">Velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="352ba-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352ba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="352ba-111">Return value</span></span>

<span data-ttu-id="352ba-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="352ba-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="352ba-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="352ba-113">Remarks</span></span>

<span data-ttu-id="352ba-114">Este método actualiza el valor de la variable miembro [**CSourceSeeking::m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) y, a continuación, llama al método virtual [**puro CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="352ba-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="352ba-115">El método no valida el *parámetro dRate.*</span><span class="sxs-lookup"><span data-stu-id="352ba-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="352ba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="352ba-116">Requirements</span></span>



| <span data-ttu-id="352ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="352ba-117">Requirement</span></span> | <span data-ttu-id="352ba-118">Value</span><span class="sxs-lookup"><span data-stu-id="352ba-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="352ba-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="352ba-119">Header</span></span><br/>  | <dl> <span data-ttu-id="352ba-120"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="352ba-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="352ba-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="352ba-121">Library</span></span><br/> | <dl> <span data-ttu-id="352ba-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="352ba-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="352ba-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="352ba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352ba-124">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="352ba-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




