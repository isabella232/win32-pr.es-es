---
description: El método Deliver entrega un ejemplo multimedia al pin de entrada conectado.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Método CBaseOutputPin. Deliver (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671509"
---
# <a name="cbaseoutputpindeliver-method"></a><span data-ttu-id="45878-103">CBaseOutputPin. Deliver (método)</span><span class="sxs-lookup"><span data-stu-id="45878-103">CBaseOutputPin.Deliver method</span></span>

<span data-ttu-id="45878-104">El `Deliver` método entrega un ejemplo multimedia al pin de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="45878-104">The `Deliver` method delivers a media sample to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="45878-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45878-105">Syntax</span></span>


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="45878-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45878-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45878-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="45878-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="45878-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="45878-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45878-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45878-109">Return value</span></span>

<span data-ttu-id="45878-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45878-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="45878-111">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="45878-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="45878-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="45878-112">Return code</span></span>                                                                                           | <span data-ttu-id="45878-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="45878-113">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="45878-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="45878-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="45878-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="45878-115">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="45878-116"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="45878-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="45878-117">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="45878-117">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="45878-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45878-118">Remarks</span></span>

<span data-ttu-id="45878-119">Este método llama al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="45878-119">This method calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input pin.</span></span> <span data-ttu-id="45878-120">**Receive** puede bloquear si el método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) devuelve S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="45878-120">**Receive** can block if the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method returns S\_OK.</span></span>

<span data-ttu-id="45878-121">Libere el ejemplo después de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="45878-121">Release the sample after calling this method.</span></span> <span data-ttu-id="45878-122">El PIN de entrada puede contener un recuento de referencias en el ejemplo, por lo que no vuelva a usar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="45878-122">The input pin might hold a reference count on the sample, so do not reuse the sample.</span></span> <span data-ttu-id="45878-123">Llame siempre al método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obtener un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="45878-123">Always call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain a new sample.</span></span>

<span data-ttu-id="45878-124">Mantenga la sección crítica del filtro antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="45878-124">Hold the filter's critical section before calling this method.</span></span> <span data-ttu-id="45878-125">De lo contrario, el PIN podría desconectarse durante la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="45878-125">Otherwise, the pin might get disconnected during the method call.</span></span> <span data-ttu-id="45878-126">Si el filtro usa un subproceso de trabajo para entregar ejemplos, mantenga la sección crítica cuando el filtro esté listo para entregar un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="45878-126">If the filter uses a worker thread to deliver samples, hold the critical section when the filter is ready to deliver a sample.</span></span> <span data-ttu-id="45878-127">De lo contrario, puede almacenar la sección crítica en el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del filtro, donde el filtro procesa los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="45878-127">Otherwise, you can hold the critical section in the filter's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, where the filter processes samples.</span></span>

<span data-ttu-id="45878-128">Los subprocesos de trabajo pueden crear un posible interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="45878-128">Worker threads can create a potential deadlock.</span></span> <span data-ttu-id="45878-129">Cuando el subproceso contiene la sección crítica, podría esperar en un cambio de estado en el filtro.</span><span class="sxs-lookup"><span data-stu-id="45878-129">When the thread holds the critical section, it might wait on a state change in the filter.</span></span> <span data-ttu-id="45878-130">Al mismo tiempo, el cambio de estado podría estar esperando a que el subproceso se complete.</span><span class="sxs-lookup"><span data-stu-id="45878-130">At the same time, the state change might be waiting for the thread to complete.</span></span> <span data-ttu-id="45878-131">Para evitar esto, el código de cambio de Estado debe señalar un evento que termine el subproceso y, a continuación, esperar a que el subproceso señale la finalización.</span><span class="sxs-lookup"><span data-stu-id="45878-131">To prevent this, the state-change code should signal an event that terminates the thread, and then wait for the thread to signal completion.</span></span>

## <a name="requirements"></a><span data-ttu-id="45878-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45878-132">Requirements</span></span>



| <span data-ttu-id="45878-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="45878-133">Requirement</span></span> | <span data-ttu-id="45878-134">Value</span><span class="sxs-lookup"><span data-stu-id="45878-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45878-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45878-135">Header</span></span><br/>  | <dl> <span data-ttu-id="45878-136"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45878-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="45878-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45878-137">Library</span></span><br/> | <dl> <span data-ttu-id="45878-138"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="45878-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45878-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="45878-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45878-140">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="45878-140">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




