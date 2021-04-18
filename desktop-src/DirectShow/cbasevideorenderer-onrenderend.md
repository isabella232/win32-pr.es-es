---
description: El método OnRenderEnd realiza el suavizado en los casos en los que el tiempo de representación varía debido a las interrupciones.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Método CBaseVideoRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660173"
---
# <a name="cbasevideorendereronrenderend-method"></a><span data-ttu-id="fb7a4-103">CBaseVideoRenderer. OnRenderEnd, método</span><span class="sxs-lookup"><span data-stu-id="fb7a4-103">CBaseVideoRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="fb7a4-104">El `OnRenderEnd` método realiza el suavizado en los casos en los que el tiempo de representación varía debido a las interrupciones.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-104">The `OnRenderEnd` method performs smoothing for cases where the rendering time varies due to interruptions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb7a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb7a4-105">Syntax</span></span>


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="fb7a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb7a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb7a4-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="fb7a4-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="fb7a4-108">Puntero al ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb7a4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb7a4-109">Return value</span></span>

<span data-ttu-id="fb7a4-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb7a4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb7a4-111">Remarks</span></span>

<span data-ttu-id="fb7a4-112">Se debe llamar a esta función miembro justo después de dibujar una imagen.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-112">This member function should be called just after drawing an image.</span></span>

<span data-ttu-id="fb7a4-113">Esta función miembro invalida [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-113">This member function overrides [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb7a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb7a4-114">Requirements</span></span>



| <span data-ttu-id="fb7a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb7a4-115">Requirement</span></span> | <span data-ttu-id="fb7a4-116">Value</span><span class="sxs-lookup"><span data-stu-id="fb7a4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb7a4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb7a4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fb7a4-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb7a4-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb7a4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb7a4-119">Library</span></span><br/> | <dl> <span data-ttu-id="fb7a4-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fb7a4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb7a4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb7a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb7a4-122">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




