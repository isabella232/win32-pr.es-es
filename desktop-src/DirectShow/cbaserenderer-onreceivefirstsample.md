---
description: Se llama al método OnReceiveFirstSample cuando el filtro recibe un ejemplo mientras está en pausa.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Método CBaseRenderer. OnReceiveFirstSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671739"
---
# <a name="cbaserendereronreceivefirstsample-method"></a><span data-ttu-id="8f9cd-103">CBaseRenderer. OnReceiveFirstSample, método</span><span class="sxs-lookup"><span data-stu-id="8f9cd-103">CBaseRenderer.OnReceiveFirstSample method</span></span>

<span data-ttu-id="8f9cd-104">`OnReceiveFirstSample`Se llama al método cuando el filtro recibe un ejemplo mientras está en pausa.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-104">The `OnReceiveFirstSample` method is called when the filter receives a sample while paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f9cd-105">Syntax</span></span>


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="8f9cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f9cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9cd-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="8f9cd-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8f9cd-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9cd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f9cd-109">Return value</span></span>

<span data-ttu-id="8f9cd-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9cd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f9cd-111">Remarks</span></span>

<span data-ttu-id="8f9cd-112">El método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-112">The [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method calls this method.</span></span> <span data-ttu-id="8f9cd-113">No realiza ninguna acción en la clase base, pero la clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-113">It does nothing in the base class, but the derived class can override it.</span></span> <span data-ttu-id="8f9cd-114">Este método está pensado principalmente para representadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-114">This method is intended primarily for video renderers.</span></span> <span data-ttu-id="8f9cd-115">Cuando un representador de vídeo está en pausa, normalmente muestra la primera muestra como una imagen fija.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-115">When a video renderer is paused, it typically displays the first sample as a still image.</span></span>

<span data-ttu-id="8f9cd-116">La búsqueda del gráfico mientras se pausa también hace que se llame a este método.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-116">Seeking the graph while paused also causes this method to be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9cd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f9cd-117">Requirements</span></span>



| <span data-ttu-id="8f9cd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9cd-118">Requirement</span></span> | <span data-ttu-id="8f9cd-119">Value</span><span class="sxs-lookup"><span data-stu-id="8f9cd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9cd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f9cd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8f9cd-121"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f9cd-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8f9cd-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f9cd-122">Library</span></span><br/> | <dl> <span data-ttu-id="8f9cd-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8f9cd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9cd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f9cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9cd-125">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="8f9cd-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




