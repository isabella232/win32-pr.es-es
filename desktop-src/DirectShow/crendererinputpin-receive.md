---
description: 'El método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método invalida el método CBaseInputPin:: Receive.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Método CRendererInputPin. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661285"
---
# <a name="crendererinputpinreceive-method"></a><span data-ttu-id="c320e-104">CRendererInputPin. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="c320e-104">CRendererInputPin.Receive method</span></span>

<span data-ttu-id="c320e-105">El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c320e-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="c320e-106">Este método invalida el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="c320e-106">This method overrides the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c320e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c320e-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c320e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c320e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c320e-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c320e-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c320e-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c320e-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c320e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c320e-111">Return value</span></span>

<span data-ttu-id="c320e-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c320e-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c320e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c320e-113">Remarks</span></span>

<span data-ttu-id="c320e-114">Este método llama al método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) del filtro, que controla la representación.</span><span class="sxs-lookup"><span data-stu-id="c320e-114">This method calls the filter's [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, which handles the rendering.</span></span> <span data-ttu-id="c320e-115">Si se produce un error en ese método, el PIN envía un \_ evento ERRORABORT de EC.</span><span class="sxs-lookup"><span data-stu-id="c320e-115">If that method fails, the pin sends an EC\_ERRORABORT event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c320e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c320e-116">Requirements</span></span>



| <span data-ttu-id="c320e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c320e-117">Requirement</span></span> | <span data-ttu-id="c320e-118">Value</span><span class="sxs-lookup"><span data-stu-id="c320e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c320e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c320e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c320e-120"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c320e-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c320e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c320e-121">Library</span></span><br/> | <dl> <span data-ttu-id="c320e-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c320e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c320e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c320e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c320e-124">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="c320e-124">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




