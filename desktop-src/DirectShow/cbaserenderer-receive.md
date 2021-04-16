---
description: El método Receive recibe el siguiente ejemplo multimedia en la secuencia.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Método CBaseRenderer. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671844"
---
# <a name="cbaserendererreceive-method"></a><span data-ttu-id="4e51d-103">CBaseRenderer. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="4e51d-103">CBaseRenderer.Receive method</span></span>

<span data-ttu-id="4e51d-104">El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4e51d-104">The `Receive` method receives the next media sample in the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e51d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e51d-105">Syntax</span></span>


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="4e51d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e51d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e51d-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="4e51d-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4e51d-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e51d-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e51d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e51d-109">Return value</span></span>

<span data-ttu-id="4e51d-110">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="4e51d-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e51d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e51d-111">Remarks</span></span>

<span data-ttu-id="4e51d-112">El PIN de entrada llama a este método cuando recibe un ejemplo del filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4e51d-112">The input pin calls this method when it receives a sample from the upstream filter.</span></span>

<span data-ttu-id="4e51d-113">Si el filtro se está ejecutando, este método realiza los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="4e51d-113">If the filter is running, this method performs the following steps:</span></span>

1.  <span data-ttu-id="4e51d-114">Programa el ejemplo para la representación ([**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md)).</span><span class="sxs-lookup"><span data-stu-id="4e51d-114">Schedules the sample for rendering ([**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md)).</span></span>
2.  <span data-ttu-id="4e51d-115">Espera la hora programada ([**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span><span class="sxs-lookup"><span data-stu-id="4e51d-115">Waits for the scheduled time ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span></span>
3.  <span data-ttu-id="4e51d-116">Representa el ejemplo ([**CBaseRenderer:: Render**](cbaserenderer-render.md)).</span><span class="sxs-lookup"><span data-stu-id="4e51d-116">Renders the sample ([**CBaseRenderer::Render**](cbaserenderer-render.md)).</span></span>
4.  <span data-ttu-id="4e51d-117">Libera el ejemplo ([**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span><span class="sxs-lookup"><span data-stu-id="4e51d-117">Releases the sample ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span></span>

<span data-ttu-id="4e51d-118">Si el filtro está en pausa, el método realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e51d-118">If the filter is paused, the method performs the following steps:</span></span>

1.  <span data-ttu-id="4e51d-119">Notifica a la clase derivada que hay un ejemplo disponible ([**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span><span class="sxs-lookup"><span data-stu-id="4e51d-119">Notifies the derived class that a sample is available ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span></span>
2.  <span data-ttu-id="4e51d-120">Espera la hora programada.</span><span class="sxs-lookup"><span data-stu-id="4e51d-120">Waits for the scheduled time.</span></span>
3.  <span data-ttu-id="4e51d-121">Representa el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e51d-121">Renders the sample.</span></span>
4.  <span data-ttu-id="4e51d-122">Libera el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e51d-122">Releases the sample.</span></span>

<span data-ttu-id="4e51d-123">Mientras está en pausa, el método espera en el paso 2 hasta que el filtro cambia a un estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4e51d-123">While paused, the method waits in step 2 until the filter switches to a running state.</span></span> <span data-ttu-id="4e51d-124">En ese momento, el filtro programa el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e51d-124">At that point, the filter schedules the sample.</span></span>

<span data-ttu-id="4e51d-125">En la clase base, el método **OnReceiveFirstSample** no hace nada.</span><span class="sxs-lookup"><span data-stu-id="4e51d-125">In the base class, the **OnReceiveFirstSample** method does nothing.</span></span> <span data-ttu-id="4e51d-126">La clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="4e51d-126">The derived class can override it.</span></span> <span data-ttu-id="4e51d-127">Por ejemplo, cuando se pausa un representador de vídeo, muestra el primer ejemplo como imagen fija.</span><span class="sxs-lookup"><span data-stu-id="4e51d-127">For example, when a video renderer is paused, it displays the first sample as a still image.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e51d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e51d-128">Requirements</span></span>



| <span data-ttu-id="4e51d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e51d-129">Requirement</span></span> | <span data-ttu-id="4e51d-130">Value</span><span class="sxs-lookup"><span data-stu-id="4e51d-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e51d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e51d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4e51d-132"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e51d-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e51d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e51d-133">Library</span></span><br/> | <dl> <span data-ttu-id="4e51d-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4e51d-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e51d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e51d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e51d-136">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4e51d-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




