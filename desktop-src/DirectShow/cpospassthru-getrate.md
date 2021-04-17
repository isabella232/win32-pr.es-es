---
description: 'El método GetRate recupera la velocidad de reproducción. Este método implementa el método IMediaSeeking:: GetRate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Método CPosPassThru. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660281"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="ad7e8-104">CPosPassThru. GetRate, método</span><span class="sxs-lookup"><span data-stu-id="ad7e8-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="ad7e8-105">El `GetRate` método recupera la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="ad7e8-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="ad7e8-106">Este método implementa el método [**IMediaSeeking:: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="ad7e8-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7e8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad7e8-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="ad7e8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad7e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad7e8-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="ad7e8-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="ad7e8-110">Puntero a una variable que recibe la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="ad7e8-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad7e8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad7e8-111">Return value</span></span>

<span data-ttu-id="ad7e8-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="ad7e8-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7e8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad7e8-113">Requirements</span></span>



| <span data-ttu-id="ad7e8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad7e8-114">Requirement</span></span> | <span data-ttu-id="ad7e8-115">Value</span><span class="sxs-lookup"><span data-stu-id="ad7e8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7e8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad7e8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ad7e8-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad7e8-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad7e8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad7e8-118">Library</span></span><br/> | <dl> <span data-ttu-id="ad7e8-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ad7e8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad7e8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad7e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7e8-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="ad7e8-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




