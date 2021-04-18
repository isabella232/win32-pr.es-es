---
description: 'El método GetDuration recupera la duración de la secuencia. Este método implementa el método IMediaSeeking:: GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Método CPosPassThru. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660126"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="249c1-104">CPosPassThru. GetDuration, método</span><span class="sxs-lookup"><span data-stu-id="249c1-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="249c1-105">El `GetDuration` método recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="249c1-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="249c1-106">Este método implementa el método [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="249c1-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="249c1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="249c1-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="249c1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="249c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="249c1-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="249c1-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="249c1-110">Puntero a una variable que recibe la duración, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="249c1-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="249c1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="249c1-111">Return value</span></span>

<span data-ttu-id="249c1-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="249c1-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="249c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="249c1-113">Requirements</span></span>



| <span data-ttu-id="249c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="249c1-114">Requirement</span></span> | <span data-ttu-id="249c1-115">Value</span><span class="sxs-lookup"><span data-stu-id="249c1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="249c1-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="249c1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="249c1-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="249c1-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="249c1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="249c1-118">Library</span></span><br/> | <dl> <span data-ttu-id="249c1-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="249c1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="249c1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="249c1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249c1-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="249c1-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




