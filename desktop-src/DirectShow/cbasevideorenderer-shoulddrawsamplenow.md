---
description: El método ShouldDrawSampleNow determina si el vídeo se debe dibujar sin establecer un vínculo de aviso de temporizador con el reloj.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Método CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679093"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a><span data-ttu-id="12866-103">CBaseVideoRenderer. ShouldDrawSampleNow, método</span><span class="sxs-lookup"><span data-stu-id="12866-103">CBaseVideoRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="12866-104">El `ShouldDrawSampleNow` método determina si el vídeo se debe dibujar sin establecer un vínculo de aviso de temporizador con el reloj.</span><span class="sxs-lookup"><span data-stu-id="12866-104">The `ShouldDrawSampleNow` method determines if the video should be drawn without setting a timer advise link with the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="12866-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12866-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a><span data-ttu-id="12866-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12866-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12866-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="12866-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="12866-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="12866-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface for the sample.</span></span>

</dd> <dt>

<span data-ttu-id="12866-109">*ptrStart*</span><span class="sxs-lookup"><span data-stu-id="12866-109">*ptrStart*</span></span> 
</dt> <dd>

<span data-ttu-id="12866-110">Puntero a la hora de inicio de la representación.</span><span class="sxs-lookup"><span data-stu-id="12866-110">Pointer to the time to begin rendering.</span></span>

</dd> <dt>

<span data-ttu-id="12866-111">*ptrEnd*</span><span class="sxs-lookup"><span data-stu-id="12866-111">*ptrEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="12866-112">Puntero a la hora de detener la representación.</span><span class="sxs-lookup"><span data-stu-id="12866-112">Pointer to the time to stop rendering.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12866-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12866-113">Return value</span></span>

<span data-ttu-id="12866-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12866-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="12866-115">Devuelve S \_ OK para indicar que el dibujo se realiza a la vez sin esperar, es \_ false para indicar que se dibuje en el tiempo *ptrStart*, o bien un error para indicar que no se dibuja el ejemplo; es decir, se omite para ahorrar tiempo.</span><span class="sxs-lookup"><span data-stu-id="12866-115">Returns S\_OK to mean draw at once without waiting, S\_FALSE to mean draw at time *ptrStart*, or an error to mean do not draw the sample; that is, skip it to save time.</span></span>

## <a name="remarks"></a><span data-ttu-id="12866-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12866-116">Remarks</span></span>

<span data-ttu-id="12866-117">Esta función miembro invalida [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span><span class="sxs-lookup"><span data-stu-id="12866-117">This member function overrides [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12866-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12866-118">Requirements</span></span>



| <span data-ttu-id="12866-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="12866-119">Requirement</span></span> | <span data-ttu-id="12866-120">Value</span><span class="sxs-lookup"><span data-stu-id="12866-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12866-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12866-121">Header</span></span><br/>  | <dl> <span data-ttu-id="12866-122"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12866-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12866-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12866-123">Library</span></span><br/> | <dl> <span data-ttu-id="12866-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="12866-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12866-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="12866-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12866-126">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="12866-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




