---
description: El método Notify recibe una notificación que indica que se ha solicitado un cambio de calidad.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Método CBaseVideoRenderer. Notify (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660396"
---
# <a name="cbasevideorenderernotify-method"></a><span data-ttu-id="8b3d5-103">CBaseVideoRenderer. Notify (método)</span><span class="sxs-lookup"><span data-stu-id="8b3d5-103">CBaseVideoRenderer.Notify method</span></span>

<span data-ttu-id="8b3d5-104">El `Notify` método recibe una notificación de que se solicita un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="8b3d5-104">The `Notify` method receives a notification that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b3d5-105">Syntax</span></span>


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="8b3d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b3d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b3d5-107">*pSelf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b3d5-107">*pSelf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3d5-108">Puntero al filtro que está enviando la notificación de calidad.</span><span class="sxs-lookup"><span data-stu-id="8b3d5-108">Pointer to the filter that is sending the quality notification.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d5-109">*preguntas y respuestas* \[\]</span><span class="sxs-lookup"><span data-stu-id="8b3d5-109">*q* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3d5-110">Estructura de notificación de calidad.</span><span class="sxs-lookup"><span data-stu-id="8b3d5-110">Quality notification structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b3d5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b3d5-111">Return value</span></span>

<span data-ttu-id="8b3d5-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b3d5-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b3d5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b3d5-113">Remarks</span></span>

<span data-ttu-id="8b3d5-114">Esta función miembro implementa el método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) en el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8b3d5-114">This member function implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method on the video renderer.</span></span> <span data-ttu-id="8b3d5-115">Esto se llama, normalmente por el administrador de gráficos de filtro, cuando se debe recortar la calidad.</span><span class="sxs-lookup"><span data-stu-id="8b3d5-115">This is called, typically by the filter graph manager, when the quality must be cut back.</span></span> <span data-ttu-id="8b3d5-116">Esto puede ocurrir cuando se ha aumentado la calidad de la reproducción de audio hasta el punto en que se debe reducir la calidad de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8b3d5-116">This might occur when the quality of audio playback has been increased to the point that the video playback quality must be decreased.</span></span>

<span data-ttu-id="8b3d5-117">`Notify` establece el miembro de datos **m \_ trThrottle** en un valor de retraso que se va a insertar entre los marcos de [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span><span class="sxs-lookup"><span data-stu-id="8b3d5-117">`Notify` sets the **m\_trThrottle** data member to a delay value to be inserted between frames by [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b3d5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b3d5-118">Requirements</span></span>



| <span data-ttu-id="8b3d5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b3d5-119">Requirement</span></span> | <span data-ttu-id="8b3d5-120">Value</span><span class="sxs-lookup"><span data-stu-id="8b3d5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3d5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b3d5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8b3d5-122"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d5-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b3d5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b3d5-123">Library</span></span><br/> | <dl> <span data-ttu-id="8b3d5-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b3d5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b3d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3d5-126">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="8b3d5-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




