---
description: El método ResetMediaTime restablece las marcas de tiempo almacenadas en caché a cero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Método CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660450"
---
# <a name="crendererpospassthruresetmediatime-method"></a><span data-ttu-id="273c5-103">CRendererPosPassThru. ResetMediaTime, método</span><span class="sxs-lookup"><span data-stu-id="273c5-103">CRendererPosPassThru.ResetMediaTime method</span></span>

<span data-ttu-id="273c5-104">El `ResetMediaTime` método restablece las marcas de tiempo almacenadas en caché a cero.</span><span class="sxs-lookup"><span data-stu-id="273c5-104">The `ResetMediaTime` method resets the cached time stamps to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="273c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="273c5-105">Syntax</span></span>


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a><span data-ttu-id="273c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="273c5-106">Parameters</span></span>

<span data-ttu-id="273c5-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="273c5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="273c5-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="273c5-108">Return value</span></span>

<span data-ttu-id="273c5-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="273c5-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="273c5-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="273c5-110">Remarks</span></span>

<span data-ttu-id="273c5-111">El filtro debe llamar a este método siempre que las marcas de tiempo almacenadas en caché por el método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) dejen de ser válidas.</span><span class="sxs-lookup"><span data-stu-id="273c5-111">The filter should call this method whenever the time stamps cached by the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method become invalid.</span></span> <span data-ttu-id="273c5-112">En concreto, debe llamar a este método en respuesta a los métodos [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) y [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="273c5-112">Specifically, it should call this method in response to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) and [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) methods.</span></span>

<span data-ttu-id="273c5-113">Después de llamar a este método, el método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) devuelve cero para las horas de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="273c5-113">After this method is called, the [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method returns zero for the start and end times.</span></span>

## <a name="requirements"></a><span data-ttu-id="273c5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="273c5-114">Requirements</span></span>



| <span data-ttu-id="273c5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="273c5-115">Requirement</span></span> | <span data-ttu-id="273c5-116">Value</span><span class="sxs-lookup"><span data-stu-id="273c5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="273c5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="273c5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="273c5-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="273c5-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="273c5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="273c5-119">Library</span></span><br/> | <dl> <span data-ttu-id="273c5-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="273c5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




