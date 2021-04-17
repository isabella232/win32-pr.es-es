---
description: El método EOS actualiza las marcas de tiempo almacenadas en caché después de una notificación de final de secuencia.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Método CRendererPosPassThru. EOS (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661284"
---
# <a name="crendererpospassthrueos-method"></a><span data-ttu-id="ab18a-103">CRendererPosPassThru. EOS, método</span><span class="sxs-lookup"><span data-stu-id="ab18a-103">CRendererPosPassThru.EOS method</span></span>

<span data-ttu-id="ab18a-104">El `EOS` método actualiza las marcas de tiempo almacenadas en caché después de una notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="ab18a-104">The `EOS` method updates the cached time stamps after an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab18a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab18a-105">Syntax</span></span>


```C++
HRESULT EOS();
```



## <a name="parameters"></a><span data-ttu-id="ab18a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab18a-106">Parameters</span></span>

<span data-ttu-id="ab18a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab18a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab18a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab18a-108">Return value</span></span>

<span data-ttu-id="ab18a-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab18a-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ab18a-110">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab18a-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="ab18a-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ab18a-111">Return code</span></span>                                                                            | <span data-ttu-id="ab18a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab18a-112">Description</span></span>                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="ab18a-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ab18a-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ab18a-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="ab18a-114">Success.</span></span><br/>                                       |
| <dl> <span data-ttu-id="ab18a-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab18a-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ab18a-116">Error.</span><span class="sxs-lookup"><span data-stu-id="ab18a-116">Failure.</span></span> <span data-ttu-id="ab18a-117">Posiblemente el filtro no se transmite por secuencias.</span><span class="sxs-lookup"><span data-stu-id="ab18a-117">Possibly the filter is not streaming.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab18a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab18a-118">Remarks</span></span>

<span data-ttu-id="ab18a-119">El filtro debe llamar a este método cuando recibe una notificación de final de secuencia ([**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span><span class="sxs-lookup"><span data-stu-id="ab18a-119">The filter should call this method when it receives an end-of-stream notification ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span></span> <span data-ttu-id="ab18a-120">El método establece las marcas de tiempo almacenadas en caché igual a la posición de detención, asegurándose de que el método [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) devuelva los valores correctos al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ab18a-120">The method sets both cached time stamps equal to the stop position, ensuring that the [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the correct values at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab18a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab18a-121">Requirements</span></span>



| <span data-ttu-id="ab18a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab18a-122">Requirement</span></span> | <span data-ttu-id="ab18a-123">Value</span><span class="sxs-lookup"><span data-stu-id="ab18a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab18a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab18a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ab18a-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab18a-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab18a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab18a-126">Library</span></span><br/> | <dl> <span data-ttu-id="ab18a-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab18a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




