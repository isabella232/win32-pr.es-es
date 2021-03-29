---
description: El método OnRenderStart establece información para la representación.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Método CBaseVideoRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679105"
---
# <a name="cbasevideorendereronrenderstart-method"></a><span data-ttu-id="3f99e-103">CBaseVideoRenderer. OnRenderStart, método</span><span class="sxs-lookup"><span data-stu-id="3f99e-103">CBaseVideoRenderer.OnRenderStart method</span></span>

<span data-ttu-id="3f99e-104">El `OnRenderStart` método establece la información para la representación.</span><span class="sxs-lookup"><span data-stu-id="3f99e-104">The `OnRenderStart` method sets information for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f99e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f99e-105">Syntax</span></span>


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="3f99e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f99e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f99e-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="3f99e-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="3f99e-108">Puntero al ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="3f99e-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f99e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f99e-109">Return value</span></span>

<span data-ttu-id="3f99e-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3f99e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f99e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f99e-111">Remarks</span></span>

<span data-ttu-id="3f99e-112">Esta función miembro recupera la hora actual del reloj del sistema y la almacena en una variable miembro que se utilizará cuando se complete el dibujo.</span><span class="sxs-lookup"><span data-stu-id="3f99e-112">This member function retrieves the current clock time from the system and stores it in a member variable to be used when the drawing is complete.</span></span> <span data-ttu-id="3f99e-113">La función también realiza el registro de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3f99e-113">The function also performs performance logging.</span></span> <span data-ttu-id="3f99e-114">Se debe llamar a esta función miembro justo antes de que se inicie el dibujo.</span><span class="sxs-lookup"><span data-stu-id="3f99e-114">This member function should be called just before drawing starts.</span></span>

<span data-ttu-id="3f99e-115">Esta función miembro invalida [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md).</span><span class="sxs-lookup"><span data-stu-id="3f99e-115">This member function overrides [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f99e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f99e-116">Requirements</span></span>



| <span data-ttu-id="3f99e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f99e-117">Requirement</span></span> | <span data-ttu-id="3f99e-118">Value</span><span class="sxs-lookup"><span data-stu-id="3f99e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f99e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f99e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3f99e-120"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f99e-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f99e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f99e-121">Library</span></span><br/> | <dl> <span data-ttu-id="3f99e-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3f99e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f99e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f99e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f99e-124">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="3f99e-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




