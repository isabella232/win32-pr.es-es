---
description: El método CheckStreamState determina si se debe entregar o descartar un ejemplo multimedia.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Método CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660397"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a><span data-ttu-id="98ad5-103">CBaseStreamControl. CheckStreamState, método</span><span class="sxs-lookup"><span data-stu-id="98ad5-103">CBaseStreamControl.CheckStreamState method</span></span>

<span data-ttu-id="98ad5-104">El `CheckStreamState` método determina si se debe entregar o descartar un ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="98ad5-104">The `CheckStreamState` method determines whether a media sample should be delivered or discarded.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ad5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98ad5-105">Syntax</span></span>


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="98ad5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98ad5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ad5-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="98ad5-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="98ad5-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="98ad5-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ad5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98ad5-109">Return value</span></span>

<span data-ttu-id="98ad5-110">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="98ad5-110">Returns one of the following values.</span></span>



| <span data-ttu-id="98ad5-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98ad5-111">Return code</span></span>                                                                                       | <span data-ttu-id="98ad5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="98ad5-112">Description</span></span>                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="98ad5-113"><dt>**descartar el flujo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="98ad5-113"><dt>**STREAM\_DISCARDING**</dt></span></span> </dl> | <span data-ttu-id="98ad5-114">Descartar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="98ad5-114">Discard this sample.</span></span><br/> |
| <dl> <span data-ttu-id="98ad5-115"><dt>**FLUJO \_ de flujos**</dt></span><span class="sxs-lookup"><span data-stu-id="98ad5-115"><dt>**STREAM\_FLOWING**</dt></span></span> </dl>    | <span data-ttu-id="98ad5-116">Entregue este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="98ad5-116">Deliver this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98ad5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98ad5-117">Remarks</span></span>

<span data-ttu-id="98ad5-118">Llame a este método cuando el código PIN reciba un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="98ad5-118">Call this method when your pin receives a sample.</span></span> <span data-ttu-id="98ad5-119">Entregue el ejemplo solo si el valor devuelto es flujo de flujo \_ .</span><span class="sxs-lookup"><span data-stu-id="98ad5-119">Deliver the sample only if the return value is STREAM\_FLOWING.</span></span> <span data-ttu-id="98ad5-120">Si el valor devuelto es \_ DEScartando el flujo, descarte el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="98ad5-120">If the return value is STREAM\_DISCARDING, discard the sample.</span></span>

<span data-ttu-id="98ad5-121">Si el PIN descarta cualquier ejemplo, debe marcar el siguiente ejemplo que ofrece como discontinuidad, llamando al método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="98ad5-121">If the pin discards any samples, it should mark the next sample that it delivers as a discontinuity, by calling the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="98ad5-122">Si el filtro implementa la interfaz [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) para contar el número de fotogramas que quita, no cuente un fotograma descartado como un fotograma quitado.</span><span class="sxs-lookup"><span data-stu-id="98ad5-122">If your filter implements the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface to count how many frames it drops, do not count a discarded frame as a dropped frame.</span></span>

<span data-ttu-id="98ad5-123">Cuando el valor devuelto está \_ DEScartando el flujo, el método se bloquea hasta que el tiempo de referencia alcanza la hora de inicio del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="98ad5-123">When the return value is STREAM\_DISCARDING, the method blocks until the reference time reaches the sample's start time.</span></span> <span data-ttu-id="98ad5-124">Esto evita que el PIN descartará los ejemplos demasiado rápidamente.</span><span class="sxs-lookup"><span data-stu-id="98ad5-124">This prevents your pin from discarding samples too quickly.</span></span> <span data-ttu-id="98ad5-125">Si el filtro está en pausa, el tiempo de espera es infinito, hasta que el filtro se ejecute, detenga o vacíe los datos.</span><span class="sxs-lookup"><span data-stu-id="98ad5-125">If the filter is paused, the wait time is infinite, until the filter runs, stops, or flushes data.</span></span> <span data-ttu-id="98ad5-126">(Los cambios de estado de filtro y la transmisión por secuencias se producen en subprocesos independientes, por lo que no produce ningún interbloqueo).</span><span class="sxs-lookup"><span data-stu-id="98ad5-126">(Filter state changes and streaming happen on separate threads, so this does not cause any deadlock.)</span></span>

<span data-ttu-id="98ad5-127">La enumeración **CBaseStreamControl:: StreamControlState** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="98ad5-127">The **CBaseStreamControl::StreamControlState** enumeration is defined as follows:</span></span>


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a><span data-ttu-id="98ad5-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="98ad5-128">Examples</span></span>

<span data-ttu-id="98ad5-129">En el ejemplo siguiente se da por supuesto que el PIN usa una variable miembro denominada m \_ fLastSampleDiscarded para realizar un seguimiento de las discontinuidades.</span><span class="sxs-lookup"><span data-stu-id="98ad5-129">The following example assumes that the pin uses a member variable named m\_fLastSampleDiscarded to keep track of discontinuities.</span></span>


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="98ad5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98ad5-130">Requirements</span></span>



| <span data-ttu-id="98ad5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="98ad5-131">Requirement</span></span> | <span data-ttu-id="98ad5-132">Value</span><span class="sxs-lookup"><span data-stu-id="98ad5-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ad5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98ad5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="98ad5-134"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98ad5-134"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98ad5-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98ad5-135">Library</span></span><br/> | <dl> <span data-ttu-id="98ad5-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98ad5-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ad5-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="98ad5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ad5-138">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="98ad5-138">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




