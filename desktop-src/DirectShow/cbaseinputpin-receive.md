---
description: 'El método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el método IMemInputPin:: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Método CBaseInputPin. Receive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660191"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="5d66f-104">CBaseInputPin. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="5d66f-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="5d66f-105">El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5d66f-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="5d66f-106">Este método implementa el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="5d66f-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d66f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d66f-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="5d66f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d66f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d66f-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="5d66f-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5d66f-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d66f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d66f-111">Return value</span></span>

<span data-ttu-id="5d66f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d66f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5d66f-113">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5d66f-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="5d66f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5d66f-114">Return code</span></span>                                                                                             | <span data-ttu-id="5d66f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d66f-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="5d66f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="5d66f-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="5d66f-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="5d66f-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="5d66f-119">El PIN se está vaciando actualmente; se rechazó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="5d66f-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="5d66f-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5d66f-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="5d66f-122"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="5d66f-123">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="5d66f-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="5d66f-124"><dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="5d66f-125">Se produjo un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5d66f-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="5d66f-126"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="5d66f-127">El PIN está detenido.</span><span class="sxs-lookup"><span data-stu-id="5d66f-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="5d66f-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d66f-128">Remarks</span></span>

<span data-ttu-id="5d66f-129">El PIN de salida ascendente llama a este método para proporcionar un ejemplo al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="5d66f-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="5d66f-130">El PIN de entrada debe realizar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="5d66f-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="5d66f-131">Procese el ejemplo antes de volver.</span><span class="sxs-lookup"><span data-stu-id="5d66f-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="5d66f-132">Devuelva y procese el ejemplo en un subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="5d66f-133">Rechace el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-133">Reject the sample.</span></span>

<span data-ttu-id="5d66f-134">Si el PIN usa un subproceso de trabajo para procesar el ejemplo, agregue un recuento de referencias al ejemplo dentro de este método.</span><span class="sxs-lookup"><span data-stu-id="5d66f-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="5d66f-135">Una vez que el método devuelve, el PIN ascendente libera el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="5d66f-136">Cuando el recuento de referencias del ejemplo llega a cero, el ejemplo vuelve al asignador para reutilizarlo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="5d66f-137">Este método es sincrónico y puede bloquearse.</span><span class="sxs-lookup"><span data-stu-id="5d66f-137">This method is synchronous and can block.</span></span> <span data-ttu-id="5d66f-138">Si el método puede bloquearse, el método [**CBaseInputPin:: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) del PIN debe devolver s \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5d66f-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="5d66f-139">En la clase base, este método realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d66f-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="5d66f-140">Llama al método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) para comprobar que el pin puede procesar los ejemplos ahora.</span><span class="sxs-lookup"><span data-stu-id="5d66f-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="5d66f-141">Si no puede, por ejemplo, si se detiene el PIN, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="5d66f-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="5d66f-142">Recupera las propiedades de ejemplo y comprueba si el formato ha cambiado (consulte a continuación).</span><span class="sxs-lookup"><span data-stu-id="5d66f-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="5d66f-143">Si el formato ha cambiado, el método llama al método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar si el nuevo formato es aceptable.</span><span class="sxs-lookup"><span data-stu-id="5d66f-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="5d66f-144">Si el nuevo formato no es aceptable, el método llama al método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) , envía un \_ evento ERRORABORT de EC y devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="5d66f-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="5d66f-145">Suponiendo que no haya errores, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5d66f-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="5d66f-146">Compruebe si hay un cambio de formato de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5d66f-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="5d66f-147">Si el ejemplo admite la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , compruebe el miembro **dwSampleFlags** de la estructura [**AM \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="5d66f-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="5d66f-148">Si la \_ marca TYPECHANGED de ejemplo AM \_ está presente, el formato ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="5d66f-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="5d66f-149">En caso contrario, si el ejemplo no es compatible con **IMediaSample2**, llame al método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="5d66f-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="5d66f-150">Si el método devuelve un valor distinto de **null** , el formato ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="5d66f-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="5d66f-151">En la clase base, este método no procesa el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="5d66f-152">La clase derivada debe invalidar este método para realizar el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="5d66f-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="5d66f-153">(Lo que conlleva depende completamente del filtro). La clase derivada debe llamar al método de clase base para comprobar los errores descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5d66f-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d66f-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d66f-154">Requirements</span></span>



| <span data-ttu-id="5d66f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d66f-155">Requirement</span></span> | <span data-ttu-id="5d66f-156">Value</span><span class="sxs-lookup"><span data-stu-id="5d66f-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d66f-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d66f-157">Header</span></span><br/>  | <dl> <span data-ttu-id="5d66f-158"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5d66f-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d66f-159">Library</span></span><br/> | <dl> <span data-ttu-id="5d66f-160"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5d66f-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d66f-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d66f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d66f-162">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="5d66f-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




