---
description: El método ReceiveMultiple ofrece un lote de muestras de medios al pin de entrada.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Método COutputQueue. ReceiveMultiple (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678974"
---
# <a name="coutputqueuereceivemultiple-method"></a><span data-ttu-id="55ebd-103">COutputQueue. ReceiveMultiple, método</span><span class="sxs-lookup"><span data-stu-id="55ebd-103">COutputQueue.ReceiveMultiple method</span></span>

<span data-ttu-id="55ebd-104">El `ReceiveMultiple` método proporciona un lote de muestras de medios al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="55ebd-104">The `ReceiveMultiple` method delivers a batch of media samples to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ebd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55ebd-105">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="55ebd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55ebd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ebd-107">*ppSamples*</span><span class="sxs-lookup"><span data-stu-id="55ebd-107">*ppSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="55ebd-108">Dirección de un puntero a una matriz de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="55ebd-108">Address of a pointer to an array of samples.</span></span>

</dd> <dt>

<span data-ttu-id="55ebd-109">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="55ebd-109">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="55ebd-110">Número de muestras de la matriz.</span><span class="sxs-lookup"><span data-stu-id="55ebd-110">Number of samples in the array.</span></span>

</dd> <dt>

<span data-ttu-id="55ebd-111">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="55ebd-111">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="55ebd-112">Puntero a una variable que recibe el número de muestras que se han entregado correctamente.</span><span class="sxs-lookup"><span data-stu-id="55ebd-112">Pointer to a variable that receives the number of samples delivered successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ebd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55ebd-113">Return value</span></span>

<span data-ttu-id="55ebd-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55ebd-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="55ebd-115">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="55ebd-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="55ebd-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="55ebd-116">Return code</span></span>                                                                             | <span data-ttu-id="55ebd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="55ebd-117">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55ebd-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="55ebd-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="55ebd-119">Se recibió una notificación de final de secuencia antes de procesar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="55ebd-119">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="55ebd-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="55ebd-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="55ebd-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="55ebd-121">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="55ebd-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55ebd-122">Remarks</span></span>

<span data-ttu-id="55ebd-123">Si el objeto utiliza un subproceso, este método pone en cola todos los ejemplos pasados en la matriz.</span><span class="sxs-lookup"><span data-stu-id="55ebd-123">If the object is using a thread, this method queues all of the samples passed in the array.</span></span> <span data-ttu-id="55ebd-124">De lo contrario, el método llama al método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="55ebd-124">Otherwise, the method calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ebd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55ebd-125">Requirements</span></span>



| <span data-ttu-id="55ebd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ebd-126">Requirement</span></span> | <span data-ttu-id="55ebd-127">Value</span><span class="sxs-lookup"><span data-stu-id="55ebd-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ebd-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55ebd-128">Header</span></span><br/>  | <dl> <span data-ttu-id="55ebd-129"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55ebd-129"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55ebd-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55ebd-130">Library</span></span><br/> | <dl> <span data-ttu-id="55ebd-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="55ebd-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ebd-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="55ebd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ebd-133">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="55ebd-133">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




