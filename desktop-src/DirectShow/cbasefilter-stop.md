---
description: 'El método Stop detiene el filtro. Este método implementa el método IMediaFilter:: stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Método CBaseFilter. STOP (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660609"
---
# <a name="cbasefilterstop-method"></a><span data-ttu-id="a979c-104">CBaseFilter. STOP (método)</span><span class="sxs-lookup"><span data-stu-id="a979c-104">CBaseFilter.Stop method</span></span>

<span data-ttu-id="a979c-105">El `Stop` método detiene el filtro.</span><span class="sxs-lookup"><span data-stu-id="a979c-105">The `Stop` method stops the filter.</span></span> <span data-ttu-id="a979c-106">Este método implementa el método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="a979c-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a979c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a979c-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="a979c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a979c-108">Parameters</span></span>

<span data-ttu-id="a979c-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a979c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a979c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a979c-110">Return value</span></span>

<span data-ttu-id="a979c-111">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="a979c-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a979c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a979c-112">Remarks</span></span>

<span data-ttu-id="a979c-113">Este método llama al método [**CBasePin:: Inactive**](cbasepin-inactive.md) en cada una de las clavijas conectadas del filtro.</span><span class="sxs-lookup"><span data-stu-id="a979c-113">This method calls the [**CBasePin::Inactive**](cbasepin-inactive.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="a979c-114">También establece el estado del filtro en \_ detenido.</span><span class="sxs-lookup"><span data-stu-id="a979c-114">It also sets the filter's state to State\_Stopped.</span></span>

<span data-ttu-id="a979c-115">Cuando el filtro se detiene, debe rechazar los ejemplos del nivel superior, detener la entrega de muestras de bajada, cerrar los subprocesos de trabajo y liberar los recursos que se utilizaron para la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="a979c-115">When the filter stops, it should reject samples from upstream, stop delivering samples downstream, shut down worker threads, and free any resources that it used for streaming.</span></span>

## <a name="requirements"></a><span data-ttu-id="a979c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a979c-116">Requirements</span></span>



| <span data-ttu-id="a979c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a979c-117">Requirement</span></span> | <span data-ttu-id="a979c-118">Value</span><span class="sxs-lookup"><span data-stu-id="a979c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a979c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a979c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a979c-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a979c-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a979c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a979c-121">Library</span></span><br/> | <dl> <span data-ttu-id="a979c-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a979c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a979c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a979c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a979c-124">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a979c-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




