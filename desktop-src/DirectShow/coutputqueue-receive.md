---
description: El método Receive entrega un ejemplo multimedia al pin de entrada.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: Método COutputQueue. Receive (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ce8a0d44730fa35b38cf6d738edd26168284a46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670409"
---
# <a name="coutputqueuereceive-method"></a><span data-ttu-id="77c0b-103">COutputQueue. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="77c0b-103">COutputQueue.Receive method</span></span>

<span data-ttu-id="77c0b-104">El `Receive` método entrega un ejemplo multimedia al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="77c0b-104">The `Receive` method delivers a media sample to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77c0b-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="77c0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77c0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77c0b-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="77c0b-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="77c0b-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="77c0b-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77c0b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77c0b-109">Return value</span></span>

<span data-ttu-id="77c0b-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77c0b-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="77c0b-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="77c0b-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="77c0b-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="77c0b-112">Return code</span></span>                                                                             | <span data-ttu-id="77c0b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="77c0b-113">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77c0b-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="77c0b-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="77c0b-115">Se recibió una notificación de final de secuencia antes de procesar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="77c0b-115">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="77c0b-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="77c0b-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="77c0b-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="77c0b-117">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="77c0b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77c0b-118">Remarks</span></span>

<span data-ttu-id="77c0b-119">Este método llama al método [**COutputQueue:: ReceiveMultiple**](coutputqueue-receivemultiple.md) .</span><span class="sxs-lookup"><span data-stu-id="77c0b-119">This method calls the [**COutputQueue::ReceiveMultiple**](coutputqueue-receivemultiple.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="77c0b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77c0b-120">Requirements</span></span>



| <span data-ttu-id="77c0b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="77c0b-121">Requirement</span></span> | <span data-ttu-id="77c0b-122">Value</span><span class="sxs-lookup"><span data-stu-id="77c0b-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77c0b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77c0b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="77c0b-124"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77c0b-124"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77c0b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77c0b-125">Library</span></span><br/> | <dl> <span data-ttu-id="77c0b-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="77c0b-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77c0b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="77c0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77c0b-128">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="77c0b-128">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




