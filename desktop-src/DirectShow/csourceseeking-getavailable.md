---
description: 'El método GetAvailable recupera el intervalo de veces que la búsqueda es eficaz. Este método implementa el método IMediaSeeking:: GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Método CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690513"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="26301-104">CSourceSeeking. GetAvailable, método</span><span class="sxs-lookup"><span data-stu-id="26301-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="26301-105">El `GetAvailable` método recupera el intervalo de veces que la búsqueda es eficaz.</span><span class="sxs-lookup"><span data-stu-id="26301-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="26301-106">Este método implementa el método [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="26301-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="26301-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26301-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="26301-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26301-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26301-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="26301-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="26301-110">Puntero a una variable que recibe la hora más temprana para una búsqueda eficaz.</span><span class="sxs-lookup"><span data-stu-id="26301-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="26301-111">La variable se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="26301-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="26301-112">*Planchas*</span><span class="sxs-lookup"><span data-stu-id="26301-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="26301-113">Puntero a una variable que recibe la hora más reciente para una búsqueda eficaz.</span><span class="sxs-lookup"><span data-stu-id="26301-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="26301-114">La variable se establece en el valor de la variable miembro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="26301-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26301-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26301-115">Return value</span></span>

<span data-ttu-id="26301-116">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="26301-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="26301-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26301-117">Requirements</span></span>



| <span data-ttu-id="26301-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="26301-118">Requirement</span></span> | <span data-ttu-id="26301-119">Value</span><span class="sxs-lookup"><span data-stu-id="26301-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26301-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26301-120">Header</span></span><br/>  | <dl> <span data-ttu-id="26301-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26301-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26301-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26301-122">Library</span></span><br/> | <dl> <span data-ttu-id="26301-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="26301-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26301-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="26301-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26301-125">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="26301-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




