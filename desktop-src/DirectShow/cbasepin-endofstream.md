---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin:: EndOfStream. Llame a este método solo en clavijas de entrada.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Método CBasePin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671633"
---
# <a name="cbasepinendofstream-method"></a><span data-ttu-id="e588c-105">CBasePin. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="e588c-105">CBasePin.EndOfStream method</span></span>

<span data-ttu-id="e588c-106">El `EndOfStream` método notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="e588c-106">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="e588c-107">Este método implementa el método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="e588c-107">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span> <span data-ttu-id="e588c-108">Llame a este método solo en clavijas de entrada.</span><span class="sxs-lookup"><span data-stu-id="e588c-108">Call this method only on input pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="e588c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e588c-109">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="e588c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e588c-110">Parameters</span></span>

<span data-ttu-id="e588c-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e588c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e588c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e588c-112">Return value</span></span>

<span data-ttu-id="e588c-113">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="e588c-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e588c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e588c-114">Remarks</span></span>

<span data-ttu-id="e588c-115">El filtro debe pasar las notificaciones de final de secuencia de nivel inferior a los pin de entrada de los filtros conectados.</span><span class="sxs-lookup"><span data-stu-id="e588c-115">The filter should pass end-of-stream notifications downstream, to the input pins of connected filters.</span></span> <span data-ttu-id="e588c-116">Si el filtro es un representador, debería publicar una notificación de evento de [**\_ finalización de EC**](ec-complete.md) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="e588c-116">If the filter is a renderer, it should post an [**EC\_COMPLETE**](ec-complete.md) event notification to the filter graph manager.</span></span> <span data-ttu-id="e588c-117">Para obtener más información, vea [flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e588c-117">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="e588c-118">En la clase base, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="e588c-118">In the base class, this method does nothing.</span></span> <span data-ttu-id="e588c-119">Las clases derivadas deben invalidar este método.</span><span class="sxs-lookup"><span data-stu-id="e588c-119">Derived classes should override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e588c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e588c-120">Requirements</span></span>



| <span data-ttu-id="e588c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e588c-121">Requirement</span></span> | <span data-ttu-id="e588c-122">Value</span><span class="sxs-lookup"><span data-stu-id="e588c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e588c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e588c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e588c-124"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e588c-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e588c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e588c-125">Library</span></span><br/> | <dl> <span data-ttu-id="e588c-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e588c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e588c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e588c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e588c-128">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e588c-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




