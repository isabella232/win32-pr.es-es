---
description: 'El método SetDiscontinuity especifica si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el método IMediaSample:: SetDiscontinuity.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Método CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679080"
---
# <a name="cmediasamplesetdiscontinuity-method"></a><span data-ttu-id="7f947-104">CMediaSample. SetDiscontinuity, método</span><span class="sxs-lookup"><span data-stu-id="7f947-104">CMediaSample.SetDiscontinuity method</span></span>

<span data-ttu-id="7f947-105">El `SetDiscontinuity` método especifica si este ejemplo representa una interrupción en el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="7f947-105">The `SetDiscontinuity` method specifies whether this sample represents a break in the data stream.</span></span> <span data-ttu-id="7f947-106">Este método implementa el método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="7f947-106">This method implements the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f947-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f947-107">Syntax</span></span>


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a><span data-ttu-id="7f947-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f947-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f947-109">*bDiscont*</span><span class="sxs-lookup"><span data-stu-id="7f947-109">*bDiscont*</span></span> 
</dt> <dd>

<span data-ttu-id="7f947-110">Valor booleano que especifica si este ejemplo es una discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="7f947-110">Boolean value that specifies whether this sample is a discontinuity.</span></span> <span data-ttu-id="7f947-111">Si es **true**, el ejemplo multimedia es discontinuo con el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="7f947-111">If **TRUE**, the media sample is discontinuous with the previous sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f947-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f947-112">Return value</span></span>

<span data-ttu-id="7f947-113">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="7f947-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f947-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f947-114">Remarks</span></span>

<span data-ttu-id="7f947-115">Este método actualiza la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica la propiedad discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="7f947-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the discontinuity property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f947-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f947-116">Requirements</span></span>



| <span data-ttu-id="7f947-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f947-117">Requirement</span></span> | <span data-ttu-id="7f947-118">Value</span><span class="sxs-lookup"><span data-stu-id="7f947-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f947-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f947-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7f947-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f947-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7f947-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f947-121">Library</span></span><br/> | <dl> <span data-ttu-id="7f947-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7f947-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f947-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f947-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f947-124">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="7f947-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




