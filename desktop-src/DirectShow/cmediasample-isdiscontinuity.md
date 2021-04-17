---
description: 'El método IsDiscontinuity determina si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el método IMediaSample:: IsDiscontinuity.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Método CMediaSample. IsDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670474"
---
# <a name="cmediasampleisdiscontinuity-method"></a><span data-ttu-id="35dc5-104">CMediaSample. IsDiscontinuity, método</span><span class="sxs-lookup"><span data-stu-id="35dc5-104">CMediaSample.IsDiscontinuity method</span></span>

<span data-ttu-id="35dc5-105">El `IsDiscontinuity` método determina si este ejemplo representa una interrupción en el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="35dc5-105">The `IsDiscontinuity` method determines if this sample represents a break in the data stream.</span></span> <span data-ttu-id="35dc5-106">Este método implementa el método [**IMediaSample:: IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="35dc5-106">This method implements the [**IMediaSample::IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35dc5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35dc5-107">Syntax</span></span>


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a><span data-ttu-id="35dc5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35dc5-108">Parameters</span></span>

<span data-ttu-id="35dc5-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="35dc5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35dc5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35dc5-110">Return value</span></span>

<span data-ttu-id="35dc5-111">Devuelve S \_ OK si el ejemplo es un salto en el flujo de datos y S \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="35dc5-111">Returns S\_OK if the sample is a break in the data stream, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="35dc5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35dc5-112">Remarks</span></span>

<span data-ttu-id="35dc5-113">La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="35dc5-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="35dc5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35dc5-114">Requirements</span></span>



| <span data-ttu-id="35dc5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35dc5-115">Requirement</span></span> | <span data-ttu-id="35dc5-116">Value</span><span class="sxs-lookup"><span data-stu-id="35dc5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dc5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35dc5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="35dc5-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35dc5-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="35dc5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35dc5-119">Library</span></span><br/> | <dl> <span data-ttu-id="35dc5-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="35dc5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35dc5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="35dc5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dc5-122">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="35dc5-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




