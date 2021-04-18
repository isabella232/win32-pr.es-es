---
description: El método ShouldSkipFrame determina si el filtro debe quitar un ejemplo especificado.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Método CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660275"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a><span data-ttu-id="be5e6-103">CVideoTransformFilter. ShouldSkipFrame, método</span><span class="sxs-lookup"><span data-stu-id="be5e6-103">CVideoTransformFilter.ShouldSkipFrame method</span></span>

<span data-ttu-id="be5e6-104">El `ShouldSkipFrame` método determina si el filtro debe quitar un ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="be5e6-104">The `ShouldSkipFrame` method determines whether the filter should drop a specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="be5e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be5e6-105">Syntax</span></span>


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="be5e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be5e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be5e6-107">*Agujas*</span><span class="sxs-lookup"><span data-stu-id="be5e6-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="be5e6-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="be5e6-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be5e6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be5e6-109">Return value</span></span>

<span data-ttu-id="be5e6-110">Devuelve **true** si el filtro debe quitar este ejemplo o **false** si el filtro debe procesar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="be5e6-110">Returns **TRUE** if the filter should drop this sample, or **FALSE** if the filter should process this sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="be5e6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be5e6-111">Remarks</span></span>

<span data-ttu-id="be5e6-112">Este método devuelve **true** si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="be5e6-112">This method returns **TRUE** if the following conditions are met:</span></span>

-   <span data-ttu-id="be5e6-113">El ejemplo tiene marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="be5e6-113">The sample has time stamps.</span></span>
-   <span data-ttu-id="be5e6-114">El tiempo medio de descodificación es al menos el 25% de la duración del fotograma.</span><span class="sxs-lookup"><span data-stu-id="be5e6-114">The average decoding time is at least 25% of the frame duration.</span></span>
-   <span data-ttu-id="be5e6-115">Actualmente, el representador tiene al menos un fotograma más tarde, como se muestra en los mensajes de calidad.</span><span class="sxs-lookup"><span data-stu-id="be5e6-115">The renderer is currently at least one frame late, as reported through quality messages.</span></span>
-   <span data-ttu-id="be5e6-116">Omitir el fotograma clave siguiente no hará que el fotograma llegue a más de un fotograma al principio.</span><span class="sxs-lookup"><span data-stu-id="be5e6-116">Skipping to the next key frame would not cause the frame to arrive more than one frame early.</span></span>

<span data-ttu-id="be5e6-117">Para los fines de este cálculo, el filtro registra la siguiente información a medida que procesa los datos:</span><span class="sxs-lookup"><span data-stu-id="be5e6-117">For purposes of this calculation, the filter records the following information as it processes data:</span></span>

-   <span data-ttu-id="be5e6-118">El tiempo medio de descodificación en los 20 últimos fotogramas (**m \_ itrAvgDecode**)</span><span class="sxs-lookup"><span data-stu-id="be5e6-118">The average decoding time over the past 20 frames (**m\_itrAvgDecode**)</span></span>
-   <span data-ttu-id="be5e6-119">Número de fotogramas desde el último fotograma clave (**m \_ nFramesSinceKeyFrame**)</span><span class="sxs-lookup"><span data-stu-id="be5e6-119">The number of frames since the last key frame (**m\_nFramesSinceKeyFrame**)</span></span>
-   <span data-ttu-id="be5e6-120">Una estimación del número de fotogramas que hay entre fotogramas clave (**m \_ nKeyFramePeriod**)</span><span class="sxs-lookup"><span data-stu-id="be5e6-120">An estimate of how many frames there are between key frames (**m\_nKeyFramePeriod**)</span></span>

<span data-ttu-id="be5e6-121">Una vez que el filtro quita un fotograma, sigue colocando fotogramas hasta que llega al siguiente fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="be5e6-121">Once the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="be5e6-122">Si este método devuelve **true**, también envía un evento [**de \_ \_ cambio de calidad de EC**](ec-quality-change.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="be5e6-122">If this method returns **TRUE**, it also sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the Filter Graph Manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="be5e6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be5e6-123">Requirements</span></span>



| <span data-ttu-id="be5e6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be5e6-124">Requirement</span></span> | <span data-ttu-id="be5e6-125">Value</span><span class="sxs-lookup"><span data-stu-id="be5e6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be5e6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be5e6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="be5e6-127"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be5e6-127"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="be5e6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be5e6-128">Library</span></span><br/> | <dl> <span data-ttu-id="be5e6-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="be5e6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5e6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="be5e6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5e6-131">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="be5e6-131">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




