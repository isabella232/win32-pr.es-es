---
description: El método OnDirectRender recopila información de tiempo que controla la sincronización y el control de calidad.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Método CBaseVideoRenderer. OnDirectRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679334"
---
# <a name="cbasevideorendererondirectrender-method"></a><span data-ttu-id="22c99-103">CBaseVideoRenderer. OnDirectRender, método</span><span class="sxs-lookup"><span data-stu-id="22c99-103">CBaseVideoRenderer.OnDirectRender method</span></span>

<span data-ttu-id="22c99-104">El método **OnDirectRender** recopila información de tiempo que controla la sincronización y el control de calidad.</span><span class="sxs-lookup"><span data-stu-id="22c99-104">The **OnDirectRender** method collects timing information that controls synchronization and quality control.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c99-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22c99-105">Syntax</span></span>


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="22c99-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c99-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="22c99-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="22c99-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="22c99-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c99-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22c99-109">Return value</span></span>

<span data-ttu-id="22c99-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="22c99-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22c99-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22c99-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c99-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22c99-112">Remarks</span></span>

<span data-ttu-id="22c99-113">Llame a este método en lugar de a [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) y [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="22c99-113">Call this method instead of [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) and [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span></span> <span data-ttu-id="22c99-114">El representador de vídeo de DirectDraw usa este método.</span><span class="sxs-lookup"><span data-stu-id="22c99-114">This method is used by the DirectDraw video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c99-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c99-115">Requirements</span></span>



| <span data-ttu-id="22c99-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c99-116">Requirement</span></span> | <span data-ttu-id="22c99-117">Value</span><span class="sxs-lookup"><span data-stu-id="22c99-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c99-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22c99-118">Header</span></span><br/>  | <dl> <span data-ttu-id="22c99-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22c99-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22c99-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22c99-120">Library</span></span><br/> | <dl> <span data-ttu-id="22c99-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="22c99-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c99-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="22c99-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c99-123">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="22c99-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




