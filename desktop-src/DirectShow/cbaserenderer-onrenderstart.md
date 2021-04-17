---
description: Se llama al método OnRenderStart cuando la representación está a punto de iniciarse.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Método CBaseRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670819"
---
# <a name="cbaserendereronrenderstart-method"></a><span data-ttu-id="9e31a-103">CBaseRenderer. OnRenderStart, método</span><span class="sxs-lookup"><span data-stu-id="9e31a-103">CBaseRenderer.OnRenderStart method</span></span>

<span data-ttu-id="9e31a-104">`OnRenderStart`Se llama al método cuando la representación está a punto de iniciarse.</span><span class="sxs-lookup"><span data-stu-id="9e31a-104">The `OnRenderStart` method is called when rendering is about to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e31a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e31a-105">Syntax</span></span>


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="9e31a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e31a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e31a-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="9e31a-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="9e31a-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9e31a-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e31a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e31a-109">Return value</span></span>

<span data-ttu-id="9e31a-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9e31a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e31a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e31a-111">Remarks</span></span>

<span data-ttu-id="9e31a-112">El método [**CBaseRenderer:: Render**](cbaserenderer-render.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="9e31a-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="9e31a-113">No realiza ninguna acción en la clase base, pero la clase derivada puede invalidarla. por ejemplo, para recopilar datos de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="9e31a-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e31a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e31a-114">Requirements</span></span>



| <span data-ttu-id="9e31a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e31a-115">Requirement</span></span> | <span data-ttu-id="9e31a-116">Value</span><span class="sxs-lookup"><span data-stu-id="9e31a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e31a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e31a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9e31a-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e31a-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9e31a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e31a-119">Library</span></span><br/> | <dl> <span data-ttu-id="9e31a-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9e31a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e31a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e31a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e31a-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="9e31a-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




