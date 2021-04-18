---
description: El método SendQuality envía un mensaje de calidad para indicar lo que el proveedor debe hacer sobre la calidad.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Método CBaseVideoRenderer. SendQuality (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660239"
---
# <a name="cbasevideorenderersendquality-method"></a><span data-ttu-id="39a3f-103">CBaseVideoRenderer. SendQuality, método</span><span class="sxs-lookup"><span data-stu-id="39a3f-103">CBaseVideoRenderer.SendQuality method</span></span>

<span data-ttu-id="39a3f-104">El `SendQuality` método envía un mensaje de calidad para indicar lo que el proveedor debe hacer sobre la calidad.</span><span class="sxs-lookup"><span data-stu-id="39a3f-104">The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39a3f-105">Syntax</span></span>


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a><span data-ttu-id="39a3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39a3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a3f-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="39a3f-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="39a3f-108">Cantidad de tiempo que tarda el fotograma en retrasarse.</span><span class="sxs-lookup"><span data-stu-id="39a3f-108">Amount of time by which the frame is late.</span></span>

</dd> <dt>

<span data-ttu-id="39a3f-109">*trRealStream*</span><span class="sxs-lookup"><span data-stu-id="39a3f-109">*trRealStream*</span></span> 
</dt> <dd>

<span data-ttu-id="39a3f-110">Hora de Currentstream.</span><span class="sxs-lookup"><span data-stu-id="39a3f-110">Currentstream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a3f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39a3f-111">Return value</span></span>

<span data-ttu-id="39a3f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39a3f-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39a3f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39a3f-113">Remarks</span></span>

<span data-ttu-id="39a3f-114">Esta función miembro envía un mensaje de control de calidad ascendente para controlar la administración de calidad.</span><span class="sxs-lookup"><span data-stu-id="39a3f-114">This member function sends a quality control message upstream to control quality management.</span></span> <span data-ttu-id="39a3f-115">La naturaleza del mensaje de calidad (es decir, si se va a reducir o aumentar el número de muestras) se determina en la implementación de administración de calidad en esta clase derivada (vea [**CBaseVideoRenderer:: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span><span class="sxs-lookup"><span data-stu-id="39a3f-115">The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="39a3f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39a3f-116">Requirements</span></span>



| <span data-ttu-id="39a3f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39a3f-117">Requirement</span></span> | <span data-ttu-id="39a3f-118">Value</span><span class="sxs-lookup"><span data-stu-id="39a3f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a3f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39a3f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="39a3f-120"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39a3f-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39a3f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39a3f-121">Library</span></span><br/> | <dl> <span data-ttu-id="39a3f-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="39a3f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a3f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="39a3f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a3f-124">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="39a3f-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




