---
description: 'El método IsSyncPoint determina si el principio del ejemplo es un punto de sincronización. Este método implementa el método IMediaSample:: IsSyncPoint.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Método CMediaSample. IsSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670472"
---
# <a name="cmediasampleissyncpoint-method"></a><span data-ttu-id="0aef5-104">CMediaSample. IsSyncPoint, método</span><span class="sxs-lookup"><span data-stu-id="0aef5-104">CMediaSample.IsSyncPoint method</span></span>

<span data-ttu-id="0aef5-105">El `IsSyncPoint` método determina si el principio del ejemplo es un punto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="0aef5-105">The `IsSyncPoint` method determines if the beginning of the sample is a synchronization point.</span></span> <span data-ttu-id="0aef5-106">Este método implementa el método [**IMediaSample:: IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="0aef5-106">This method implements the [**IMediaSample::IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aef5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aef5-107">Syntax</span></span>


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a><span data-ttu-id="0aef5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aef5-108">Parameters</span></span>

<span data-ttu-id="0aef5-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0aef5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0aef5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aef5-110">Return value</span></span>

<span data-ttu-id="0aef5-111">Devuelve S \_ OK si el ejemplo es un punto de sincronización o S \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0aef5-111">Returns S\_OK if the sample is a synchronization point, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aef5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aef5-112">Remarks</span></span>

<span data-ttu-id="0aef5-113">La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0aef5-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aef5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aef5-114">Requirements</span></span>



| <span data-ttu-id="0aef5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aef5-115">Requirement</span></span> | <span data-ttu-id="0aef5-116">Value</span><span class="sxs-lookup"><span data-stu-id="0aef5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aef5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aef5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0aef5-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aef5-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0aef5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0aef5-119">Library</span></span><br/> | <dl> <span data-ttu-id="0aef5-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0aef5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aef5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aef5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aef5-122">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="0aef5-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




