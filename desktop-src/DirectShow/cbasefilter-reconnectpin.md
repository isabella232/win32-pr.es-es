---
description: El método ReconnectPin interrumpe una conexión de PIN existente y la vuelve a conectar al mismo pin, utilizando un tipo de medio especificado.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Método CBaseFilter. ReconnectPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660148"
---
# <a name="cbasefilterreconnectpin-method"></a><span data-ttu-id="52a84-103">CBaseFilter. ReconnectPin, método</span><span class="sxs-lookup"><span data-stu-id="52a84-103">CBaseFilter.ReconnectPin method</span></span>

<span data-ttu-id="52a84-104">El `ReconnectPin` método interrumpe una conexión de PIN existente y lo vuelve a conectar al mismo pin, utilizando un tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="52a84-104">The `ReconnectPin` method breaks an existing pin connection and reconnects it to the same pin, using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a84-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52a84-105">Syntax</span></span>


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="52a84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52a84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a84-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="52a84-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="52a84-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="52a84-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="52a84-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="52a84-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="52a84-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio, o **null**.</span><span class="sxs-lookup"><span data-stu-id="52a84-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a84-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52a84-111">Return value</span></span>

<span data-ttu-id="52a84-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52a84-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="52a84-113">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="52a84-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="52a84-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="52a84-114">Return code</span></span>                                                                                   | <span data-ttu-id="52a84-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="52a84-115">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52a84-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="52a84-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="52a84-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="52a84-117">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="52a84-118"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="52a84-118"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="52a84-119">la variable miembro de [**m \_ PGraph**](cbasefilter-m-pgraph.md) es **null**.</span><span class="sxs-lookup"><span data-stu-id="52a84-119">[**m\_pGraph**](cbasefilter-m-pgraph.md) member variable is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52a84-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52a84-120">Remarks</span></span>

<span data-ttu-id="52a84-121">Este método llama al método [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="52a84-121">This method calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span> <span data-ttu-id="52a84-122">Si la interfaz [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) no está disponible, el método llama a [**IFilterGraph:: reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span><span class="sxs-lookup"><span data-stu-id="52a84-122">If the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface is not available, the method calls [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span></span>

## <a name="requirements"></a><span data-ttu-id="52a84-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52a84-123">Requirements</span></span>



| <span data-ttu-id="52a84-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a84-124">Requirement</span></span> | <span data-ttu-id="52a84-125">Value</span><span class="sxs-lookup"><span data-stu-id="52a84-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a84-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52a84-126">Header</span></span><br/>  | <dl> <span data-ttu-id="52a84-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52a84-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="52a84-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52a84-128">Library</span></span><br/> | <dl> <span data-ttu-id="52a84-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="52a84-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a84-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="52a84-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a84-131">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="52a84-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




