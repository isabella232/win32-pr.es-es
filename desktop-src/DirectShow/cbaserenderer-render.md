---
description: El método Render representa un ejemplo.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Método CBaseRenderer. Render (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661324"
---
# <a name="cbaserendererrender-method"></a><span data-ttu-id="e0093-103">CBaseRenderer. Render (método)</span><span class="sxs-lookup"><span data-stu-id="e0093-103">CBaseRenderer.Render method</span></span>

<span data-ttu-id="e0093-104">El `Render` método representa un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e0093-104">The `Render` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0093-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0093-105">Syntax</span></span>


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="e0093-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0093-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0093-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="e0093-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e0093-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e0093-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0093-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0093-109">Return value</span></span>

<span data-ttu-id="e0093-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0093-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e0093-111">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0093-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e0093-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e0093-112">Return code</span></span>                                                                             | <span data-ttu-id="e0093-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0093-113">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0093-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e0093-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e0093-115">El filtro está detenido o *pMediaSample* es **null**.</span><span class="sxs-lookup"><span data-stu-id="e0093-115">The filter is stopped, or *pMediaSample* is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="e0093-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e0093-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e0093-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e0093-117">Success.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="e0093-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0093-118">Remarks</span></span>

<span data-ttu-id="e0093-119">Este método llama al método virtual puro [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md), que realiza el trabajo real.</span><span class="sxs-lookup"><span data-stu-id="e0093-119">This method calls the pure virtual method [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md), which does the real work.</span></span> <span data-ttu-id="e0093-120">La clase derivada debe implementar **DoRenderSample**.</span><span class="sxs-lookup"><span data-stu-id="e0093-120">The derived class must implement **DoRenderSample**.</span></span>

<span data-ttu-id="e0093-121">Inmediatamente antes de llamar a **DoRenderSample**, este método llama al método [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md) .</span><span class="sxs-lookup"><span data-stu-id="e0093-121">Immediately before calling **DoRenderSample**, this method calls the [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md) method.</span></span> <span data-ttu-id="e0093-122">Inmediatamente después de, llama al método [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md) .</span><span class="sxs-lookup"><span data-stu-id="e0093-122">Immediately after, it calls the [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md) method.</span></span> <span data-ttu-id="e0093-123">La clase derivada puede invalidar esos dos métodos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e0093-123">The derived class can override those two methods as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0093-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0093-124">Requirements</span></span>



| <span data-ttu-id="e0093-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0093-125">Requirement</span></span> | <span data-ttu-id="e0093-126">Value</span><span class="sxs-lookup"><span data-stu-id="e0093-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0093-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0093-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e0093-128"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0093-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0093-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0093-129">Library</span></span><br/> | <dl> <span data-ttu-id="e0093-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e0093-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0093-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0093-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0093-132">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e0093-132">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




