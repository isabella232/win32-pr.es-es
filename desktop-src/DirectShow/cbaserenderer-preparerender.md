---
description: Se llama al método PrepareRender antes de que el filtro represente un ejemplo.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Método CBaseRenderer. PrepareRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671732"
---
# <a name="cbaserendererpreparerender-method"></a><span data-ttu-id="13232-103">CBaseRenderer. PrepareRender, método</span><span class="sxs-lookup"><span data-stu-id="13232-103">CBaseRenderer.PrepareRender method</span></span>

<span data-ttu-id="13232-104">`PrepareRender`Se llama al método antes de que el filtro represente un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="13232-104">The `PrepareRender` method is called before the filter renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="13232-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13232-105">Syntax</span></span>


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a><span data-ttu-id="13232-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13232-106">Parameters</span></span>

<span data-ttu-id="13232-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="13232-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13232-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13232-108">Return value</span></span>

<span data-ttu-id="13232-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13232-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13232-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13232-110">Remarks</span></span>

<span data-ttu-id="13232-111">El filtro llama a este método antes de llamar al método [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) o al método [**CBaseRenderer:: Render**](cbaserenderer-render.md) .</span><span class="sxs-lookup"><span data-stu-id="13232-111">The filter calls this method before it calls the [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) method or the [**CBaseRenderer::Render**](cbaserenderer-render.md) method.</span></span> <span data-ttu-id="13232-112">`PrepareRender` no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="13232-112">`PrepareRender` does not do anything in the base class.</span></span> <span data-ttu-id="13232-113">La clase derivada puede invalidarlo para realizar las acciones necesarias antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="13232-113">The derived class can override it to perform any actions required before rendering.</span></span> <span data-ttu-id="13232-114">Por ejemplo, un representador de vídeo puede invalidar este método para obtener su paleta.</span><span class="sxs-lookup"><span data-stu-id="13232-114">For example, a video renderer can override this method to realize its palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="13232-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13232-115">Requirements</span></span>



| <span data-ttu-id="13232-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13232-116">Requirement</span></span> | <span data-ttu-id="13232-117">Value</span><span class="sxs-lookup"><span data-stu-id="13232-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13232-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13232-118">Header</span></span><br/>  | <dl> <span data-ttu-id="13232-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13232-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13232-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13232-120">Library</span></span><br/> | <dl> <span data-ttu-id="13232-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="13232-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13232-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="13232-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13232-123">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="13232-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




