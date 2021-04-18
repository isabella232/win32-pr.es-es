---
description: El método ChangeOutputFormat cambia dinámicamente el tipo de medio para la conexión y proporciona información de nuevo segmento.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Método CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671756"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a><span data-ttu-id="63e2d-103">CDynamicOutputPin. ChangeOutputFormat, método</span><span class="sxs-lookup"><span data-stu-id="63e2d-103">CDynamicOutputPin.ChangeOutputFormat method</span></span>

<span data-ttu-id="63e2d-104">El `ChangeOutputFormat` método cambia dinámicamente el tipo de medio para la conexión y proporciona información de nuevo segmento.</span><span class="sxs-lookup"><span data-stu-id="63e2d-104">The `ChangeOutputFormat` method dynamically changes the media type for the connection, and delivers new segment information.</span></span> <span data-ttu-id="63e2d-105">El cambio puede producirse mientras se ejecuta el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="63e2d-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="63e2d-106">Una vez que se llama a este método, no se pueden entregar los ejemplos con el tipo de medio anterior.</span><span class="sxs-lookup"><span data-stu-id="63e2d-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="63e2d-107">El llamador debe asegurarse de que no haya ejemplos antiguos pendientes.</span><span class="sxs-lookup"><span data-stu-id="63e2d-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e2d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63e2d-108">Syntax</span></span>


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a><span data-ttu-id="63e2d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63e2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e2d-110">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="63e2d-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="63e2d-111">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="63e2d-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> <dt>

<span data-ttu-id="63e2d-112">*tSegmentStart*</span><span class="sxs-lookup"><span data-stu-id="63e2d-112">*tSegmentStart*</span></span> 
</dt> <dd>

<span data-ttu-id="63e2d-113">Hora de inicio del segmento.</span><span class="sxs-lookup"><span data-stu-id="63e2d-113">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="63e2d-114">*tSegmentStop*</span><span class="sxs-lookup"><span data-stu-id="63e2d-114">*tSegmentStop*</span></span> 
</dt> <dd>

<span data-ttu-id="63e2d-115">Hora de detención del segmento.</span><span class="sxs-lookup"><span data-stu-id="63e2d-115">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="63e2d-116">*dSegmentRate*</span><span class="sxs-lookup"><span data-stu-id="63e2d-116">*dSegmentRate*</span></span> 
</dt> <dd>

<span data-ttu-id="63e2d-117">Velocidad de segmento.</span><span class="sxs-lookup"><span data-stu-id="63e2d-117">Segment rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e2d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63e2d-118">Return value</span></span>

<span data-ttu-id="63e2d-119">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63e2d-119">Returns an **HRESULT** value.</span></span> <span data-ttu-id="63e2d-120">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="63e2d-120">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="63e2d-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="63e2d-121">Return code</span></span>                                                                                           | <span data-ttu-id="63e2d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="63e2d-122">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63e2d-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="63e2d-123"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="63e2d-124">Correcto.</span><span class="sxs-lookup"><span data-stu-id="63e2d-124">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="63e2d-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="63e2d-125"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="63e2d-126">Error.</span><span class="sxs-lookup"><span data-stu-id="63e2d-126">Failure.</span></span> <span data-ttu-id="63e2d-127">Es posible que el filtro propietario no llamara a [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="63e2d-127">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="63e2d-128"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="63e2d-128"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="63e2d-129">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="63e2d-129">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="63e2d-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63e2d-130">Remarks</span></span>

<span data-ttu-id="63e2d-131">Este método cambia el tipo de formato mientras se está ejecutando el filtro.</span><span class="sxs-lookup"><span data-stu-id="63e2d-131">This method changes the format type while the filter is running.</span></span> <span data-ttu-id="63e2d-132">Si el PIN de bajada acepta el nuevo formato, no es necesario volver a conectar.</span><span class="sxs-lookup"><span data-stu-id="63e2d-132">If the downstream pin accepts the new format, no reconnection is necessary.</span></span> <span data-ttu-id="63e2d-133">De lo contrario, el método intenta volver a conectar el código PIN.</span><span class="sxs-lookup"><span data-stu-id="63e2d-133">Otherwise, the method attempts to reconnect the pin.</span></span> <span data-ttu-id="63e2d-134">Si el método cambia el formato correctamente, entrega la nueva información del segmento.</span><span class="sxs-lookup"><span data-stu-id="63e2d-134">If the method successfully changes the format, it delivers the new segment information.</span></span> <span data-ttu-id="63e2d-135">Este método llama al método [**CDynamicOutputPin:: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) para realizar el cambio de formato.</span><span class="sxs-lookup"><span data-stu-id="63e2d-135">This method calls the [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) method to perform the format change.</span></span>

<span data-ttu-id="63e2d-136">Debe llamar al método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="63e2d-136">You must call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e2d-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e2d-137">Requirements</span></span>



| <span data-ttu-id="63e2d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e2d-138">Requirement</span></span> | <span data-ttu-id="63e2d-139">Value</span><span class="sxs-lookup"><span data-stu-id="63e2d-139">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e2d-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63e2d-140">Header</span></span><br/>  | <dl> <span data-ttu-id="63e2d-141"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63e2d-141"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="63e2d-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63e2d-142">Library</span></span><br/> | <dl> <span data-ttu-id="63e2d-143"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="63e2d-143"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e2d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="63e2d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e2d-145">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="63e2d-145">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




