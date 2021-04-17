---
description: El método Receive recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Método CTransformFilter. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661024"
---
# <a name="ctransformfilterreceive-method"></a><span data-ttu-id="e8226-103">CTransformFilter. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="e8226-103">CTransformFilter.Receive method</span></span>

<span data-ttu-id="e8226-104">El `Receive` método recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="e8226-104">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8226-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8226-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e8226-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8226-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8226-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="e8226-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e8226-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) en el ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8226-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8226-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8226-109">Return value</span></span>

<span data-ttu-id="e8226-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e8226-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e8226-111">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8226-111">Possible values include the following:</span></span>



| <span data-ttu-id="e8226-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e8226-112">Return code</span></span>                                                                             | <span data-ttu-id="e8226-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8226-113">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="e8226-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e8226-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e8226-115">El filtro de nivel superior debe dejar de enviar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="e8226-115">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="e8226-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e8226-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e8226-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e8226-117">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="e8226-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8226-118">Remarks</span></span>

<span data-ttu-id="e8226-119">El PIN de entrada del filtro llama a este método cuando recibe un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e8226-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="e8226-120">Este método llama al método [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , que prepara un nuevo ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="e8226-120">This method calls the [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) method, which prepares a new output sample.</span></span> <span data-ttu-id="e8226-121">A continuación, llama al método [**CTransformFilter:: transform**](ctransformfilter-transform.md) , que la clase derivada debe implementar.</span><span class="sxs-lookup"><span data-stu-id="e8226-121">Then it calls the [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="e8226-122">El método **Transform** procesa los datos de entrada y genera datos de salida.</span><span class="sxs-lookup"><span data-stu-id="e8226-122">The **Transform** method processes the input data and produces output data.</span></span>

<span data-ttu-id="e8226-123">Si el método **Transform** devuelve S \_ false, el `Receive` método quita este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e8226-123">If the **Transform** method returns S\_FALSE, the `Receive` method drops this sample.</span></span> <span data-ttu-id="e8226-124">En el primer ejemplo quitado, el filtro envía un evento de [**\_ \_ cambio de calidad EC**](ec-quality-change.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="e8226-124">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="e8226-125">De lo contrario, si el método de **transformación** devuelve S \_ correcto, el filtro entrega el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="e8226-125">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="e8226-126">Para ello, llama al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="e8226-126">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8226-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8226-127">Requirements</span></span>



| <span data-ttu-id="e8226-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8226-128">Requirement</span></span> | <span data-ttu-id="e8226-129">Value</span><span class="sxs-lookup"><span data-stu-id="e8226-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8226-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8226-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e8226-131"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8226-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8226-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8226-132">Library</span></span><br/> | <dl> <span data-ttu-id="e8226-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e8226-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8226-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8226-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8226-135">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="e8226-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




