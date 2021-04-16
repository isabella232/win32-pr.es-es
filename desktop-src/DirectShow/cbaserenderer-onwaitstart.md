---
description: Se llama al método OnWaitStart cuando el filtro empieza a esperar el tiempo de presentación de un ejemplo.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Método CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671735"
---
# <a name="cbaserendereronwaitstart-method"></a><span data-ttu-id="a8722-103">CBaseRenderer. OnWaitStart, método</span><span class="sxs-lookup"><span data-stu-id="a8722-103">CBaseRenderer.OnWaitStart method</span></span>

<span data-ttu-id="a8722-104">`OnWaitStart`Se llama al método cuando el filtro empieza a esperar el tiempo de presentación de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a8722-104">The `OnWaitStart` method is called when the filter starts waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8722-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8722-105">Syntax</span></span>


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="a8722-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8722-106">Parameters</span></span>

<span data-ttu-id="a8722-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a8722-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8722-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8722-108">Return value</span></span>

<span data-ttu-id="a8722-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a8722-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8722-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8722-110">Remarks</span></span>

<span data-ttu-id="a8722-111">El método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) llama a este método cuando comienza a esperar el tiempo de presentación de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a8722-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it begins waiting for a sample's presentation time.</span></span> <span data-ttu-id="a8722-112">Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="a8722-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="a8722-113">Si está implementando el control de calidad, puede invalidar este método junto con el método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) .</span><span class="sxs-lookup"><span data-stu-id="a8722-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method.</span></span> <span data-ttu-id="a8722-114">Puede utilizar estos métodos para realizar el seguimiento del rendimiento del filtro.</span><span class="sxs-lookup"><span data-stu-id="a8722-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8722-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8722-115">Requirements</span></span>



| <span data-ttu-id="a8722-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8722-116">Requirement</span></span> | <span data-ttu-id="a8722-117">Value</span><span class="sxs-lookup"><span data-stu-id="a8722-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8722-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8722-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a8722-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8722-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8722-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8722-120">Library</span></span><br/> | <dl> <span data-ttu-id="a8722-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a8722-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8722-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8722-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8722-123">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="a8722-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




