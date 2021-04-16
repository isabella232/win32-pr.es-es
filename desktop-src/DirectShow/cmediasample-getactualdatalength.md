---
description: 'El método GetActualDataLength recupera la longitud de los datos válidos en el búfer. Este método implementa el método IMediaSample:: GetActualDataLength.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Método CMediaSample. GetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671553"
---
# <a name="cmediasamplegetactualdatalength-method"></a><span data-ttu-id="36b92-104">CMediaSample. GetActualDataLength, método</span><span class="sxs-lookup"><span data-stu-id="36b92-104">CMediaSample.GetActualDataLength method</span></span>

<span data-ttu-id="36b92-105">El `GetActualDataLength` método recupera la longitud de los datos válidos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="36b92-105">The `GetActualDataLength` method retrieves the length of the valid data in the buffer.</span></span> <span data-ttu-id="36b92-106">Este método implementa el método [**IMediaSample:: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="36b92-106">This method implements the [**IMediaSample::GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b92-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36b92-107">Syntax</span></span>


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a><span data-ttu-id="36b92-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36b92-108">Parameters</span></span>

<span data-ttu-id="36b92-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="36b92-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36b92-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36b92-110">Return value</span></span>

<span data-ttu-id="36b92-111">Devuelve la longitud de los datos válidos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="36b92-111">Returns the length of the valid data, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="36b92-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36b92-112">Remarks</span></span>

<span data-ttu-id="36b92-113">La variable miembro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) especifica esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="36b92-113">The [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36b92-114">Requirements</span></span>



| <span data-ttu-id="36b92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="36b92-115">Requirement</span></span> | <span data-ttu-id="36b92-116">Value</span><span class="sxs-lookup"><span data-stu-id="36b92-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36b92-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36b92-117">Header</span></span><br/>  | <dl> <span data-ttu-id="36b92-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36b92-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="36b92-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36b92-119">Library</span></span><br/> | <dl> <span data-ttu-id="36b92-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="36b92-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b92-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="36b92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b92-122">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="36b92-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

