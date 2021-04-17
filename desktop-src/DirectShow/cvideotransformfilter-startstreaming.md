---
description: 'Se llama al método StartStreaming cuando el filtro cambia al estado de pausa. Este método invalida el método CTransformFilter:: StartStreaming.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Método CVideoTransformFilter. StartStreaming (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679129"
---
# <a name="cvideotransformfilterstartstreaming-method"></a><span data-ttu-id="a813a-104">CVideoTransformFilter. StartStreaming, método</span><span class="sxs-lookup"><span data-stu-id="a813a-104">CVideoTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="a813a-105">`StartStreaming`Se llama al método cuando el filtro cambia al estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="a813a-105">The `StartStreaming` method is called when the filter switches to the paused state.</span></span> <span data-ttu-id="a813a-106">Este método invalida el método [**CTransformFilter:: StartStreaming**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="a813a-106">This method overrides the [**CTransformFilter::StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a813a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a813a-107">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="a813a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a813a-108">Parameters</span></span>

<span data-ttu-id="a813a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a813a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a813a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a813a-110">Return value</span></span>

<span data-ttu-id="a813a-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a813a-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a813a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a813a-112">Remarks</span></span>

<span data-ttu-id="a813a-113">Este método restablece todas las estadísticas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a813a-113">This method resets all of the performance statistics.</span></span>

## <a name="requirements"></a><span data-ttu-id="a813a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a813a-114">Requirements</span></span>



| <span data-ttu-id="a813a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a813a-115">Requirement</span></span> | <span data-ttu-id="a813a-116">Value</span><span class="sxs-lookup"><span data-stu-id="a813a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a813a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a813a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a813a-118"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a813a-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a813a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a813a-119">Library</span></span><br/> | <dl> <span data-ttu-id="a813a-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a813a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a813a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a813a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a813a-122">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a813a-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




