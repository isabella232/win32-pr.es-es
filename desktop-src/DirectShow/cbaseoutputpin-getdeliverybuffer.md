---
description: El método GetDeliveryBuffer recupera un ejemplo multimedia que contiene un búfer vacío.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Método CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671504"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a><span data-ttu-id="62e83-103">CBaseOutputPin. GetDeliveryBuffer, método</span><span class="sxs-lookup"><span data-stu-id="62e83-103">CBaseOutputPin.GetDeliveryBuffer method</span></span>

<span data-ttu-id="62e83-104">El `GetDeliveryBuffer` método recupera un ejemplo multimedia que contiene un búfer vacío.</span><span class="sxs-lookup"><span data-stu-id="62e83-104">The `GetDeliveryBuffer` method retrieves a media sample that contains an empty buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e83-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62e83-105">Syntax</span></span>


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="62e83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62e83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e83-107">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="62e83-107">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="62e83-108">Dirección de una variable que recibe un puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del búfer.</span><span class="sxs-lookup"><span data-stu-id="62e83-108">Address of a variable that receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="62e83-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="62e83-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="62e83-110">Puntero a la hora de inicio del ejemplo, o **null**.</span><span class="sxs-lookup"><span data-stu-id="62e83-110">Pointer to the start time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="62e83-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="62e83-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="62e83-112">Puntero a la hora de finalización del ejemplo, o **null**.</span><span class="sxs-lookup"><span data-stu-id="62e83-112">Pointer to the ending time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="62e83-113">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="62e83-113">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="62e83-114">Combinación bit a bit de las marcas admitidas por la interfaz [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="62e83-114">Bitwise combination of flags supported by the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e83-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62e83-115">Return value</span></span>

<span data-ttu-id="62e83-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62e83-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="62e83-117">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="62e83-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="62e83-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="62e83-118">Return code</span></span>                                                                                   | <span data-ttu-id="62e83-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="62e83-119">Description</span></span>                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="62e83-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="62e83-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="62e83-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="62e83-121">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="62e83-122"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="62e83-122"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="62e83-123">No hay ningún asignador disponible.</span><span class="sxs-lookup"><span data-stu-id="62e83-123">No allocator available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62e83-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62e83-124">Remarks</span></span>

<span data-ttu-id="62e83-125">Este método llama al método **IMemAllocator:: getBuffer** en el asignador y pasa los parámetros a ese método.</span><span class="sxs-lookup"><span data-stu-id="62e83-125">This method calls the **IMemAllocator::GetBuffer** method on the allocator, and passes the parameters to that method.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e83-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62e83-126">Requirements</span></span>



| <span data-ttu-id="62e83-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e83-127">Requirement</span></span> | <span data-ttu-id="62e83-128">Value</span><span class="sxs-lookup"><span data-stu-id="62e83-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62e83-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62e83-129">Header</span></span><br/>  | <dl> <span data-ttu-id="62e83-130"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62e83-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="62e83-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62e83-131">Library</span></span><br/> | <dl> <span data-ttu-id="62e83-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="62e83-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e83-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="62e83-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e83-134">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="62e83-134">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




