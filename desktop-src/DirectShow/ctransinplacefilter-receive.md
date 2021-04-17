---
description: El método Receive recibe un ejemplo multimedia, lo procesa y lo entrega al filtro de nivel inferior.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Método CTransInPlaceFilter. Receive (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661021"
---
# <a name="ctransinplacefilterreceive-method"></a><span data-ttu-id="ecc57-103">CTransInPlaceFilter. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="ecc57-103">CTransInPlaceFilter.Receive method</span></span>

<span data-ttu-id="ecc57-104">El `Receive` método recibe un ejemplo multimedia, lo procesa y lo entrega al filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ecc57-104">The `Receive` method receives a media sample, processes it, and delivers it to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc57-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecc57-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="ecc57-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecc57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc57-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="ecc57-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ecc57-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ecc57-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc57-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecc57-109">Return value</span></span>

<span data-ttu-id="ecc57-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ecc57-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ecc57-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ecc57-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ecc57-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ecc57-112">Return code</span></span>                                                                                  | <span data-ttu-id="ecc57-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecc57-113">Description</span></span>                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="ecc57-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc57-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ecc57-115">Correcto</span><span class="sxs-lookup"><span data-stu-id="ecc57-115">Success</span></span><br/>          |
| <dl> <span data-ttu-id="ecc57-116"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc57-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="ecc57-117">Error inesperado</span><span class="sxs-lookup"><span data-stu-id="ecc57-117">Unexpected error</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ecc57-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecc57-118">Remarks</span></span>

<span data-ttu-id="ecc57-119">El PIN de entrada del filtro llama a este método cuando recibe un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ecc57-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="ecc57-120">El filtro llama al método de [**transformación**](ctransinplacefilter-transform.md) , que la clase derivada debe implementar.</span><span class="sxs-lookup"><span data-stu-id="ecc57-120">The filter calls the [**Transform**](ctransinplacefilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="ecc57-121">El método **Transform** procesa los datos.</span><span class="sxs-lookup"><span data-stu-id="ecc57-121">The **Transform** method processes the data.</span></span> <span data-ttu-id="ecc57-122">Si el filtro usa solo un asignador, pasa *pSample* directamente al método de **transformación** .</span><span class="sxs-lookup"><span data-stu-id="ecc57-122">If the filter is using only one allocator, it passes *pSample* directly to the **Transform** method.</span></span> <span data-ttu-id="ecc57-123">De lo contrario, copia *pSample* y pasa la copia.</span><span class="sxs-lookup"><span data-stu-id="ecc57-123">Otherwise, it copies *pSample* and passes the copy.</span></span>

<span data-ttu-id="ecc57-124">Si el método **Transform** devuelve S \_ false, el `Receive` método quita el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ecc57-124">If the **Transform** method returns S\_FALSE, the `Receive` method drops the sample.</span></span> <span data-ttu-id="ecc57-125">En el primer ejemplo quitado, el filtro envía un evento de [**\_ \_ cambio de calidad EC**](ec-quality-change.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="ecc57-125">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="ecc57-126">De lo contrario, si el método de **transformación** devuelve S \_ correcto, el filtro entrega el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="ecc57-126">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="ecc57-127">Para ello, llama al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ecc57-127">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc57-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecc57-128">Requirements</span></span>



| <span data-ttu-id="ecc57-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecc57-129">Requirement</span></span> | <span data-ttu-id="ecc57-130">Value</span><span class="sxs-lookup"><span data-stu-id="ecc57-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc57-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecc57-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ecc57-132"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecc57-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ecc57-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ecc57-133">Library</span></span><br/> | <dl> <span data-ttu-id="ecc57-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ecc57-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc57-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecc57-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc57-136">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="ecc57-136">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




