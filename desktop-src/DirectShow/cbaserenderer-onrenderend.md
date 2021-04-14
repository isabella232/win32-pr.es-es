---
description: El método OnRenderEnd se llama después de que se represente un ejemplo.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Método CBaseRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661332"
---
# <a name="cbaserendereronrenderend-method"></a><span data-ttu-id="69268-103">CBaseRenderer. OnRenderEnd, método</span><span class="sxs-lookup"><span data-stu-id="69268-103">CBaseRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="69268-104">`OnRenderEnd`Se llama al método después de que se represente un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="69268-104">The `OnRenderEnd` method is called after a sample is rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="69268-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69268-105">Syntax</span></span>


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="69268-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69268-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69268-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="69268-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="69268-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="69268-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69268-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69268-109">Return value</span></span>

<span data-ttu-id="69268-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="69268-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69268-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69268-111">Remarks</span></span>

<span data-ttu-id="69268-112">El método [**CBaseRenderer:: Render**](cbaserenderer-render.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="69268-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="69268-113">No realiza ninguna acción en la clase base, pero la clase derivada puede invalidarla. por ejemplo, para recopilar datos de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="69268-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="69268-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69268-114">Requirements</span></span>



| <span data-ttu-id="69268-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="69268-115">Requirement</span></span> | <span data-ttu-id="69268-116">Value</span><span class="sxs-lookup"><span data-stu-id="69268-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69268-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69268-117">Header</span></span><br/>  | <dl> <span data-ttu-id="69268-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69268-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="69268-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69268-119">Library</span></span><br/> | <dl> <span data-ttu-id="69268-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="69268-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69268-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="69268-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69268-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="69268-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




