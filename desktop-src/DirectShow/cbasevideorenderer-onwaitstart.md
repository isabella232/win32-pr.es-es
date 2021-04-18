---
description: El método OnWaitStart actualiza los tiempos de espera y no espera.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Método CBaseVideoRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4fab7e1a1f24c3d00f46018db9478990be71666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679102"
---
# <a name="cbasevideorendereronwaitstart-method"></a><span data-ttu-id="92d19-103">CBaseVideoRenderer. OnWaitStart, método</span><span class="sxs-lookup"><span data-stu-id="92d19-103">CBaseVideoRenderer.OnWaitStart method</span></span>

<span data-ttu-id="92d19-104">El `OnWaitStart` método actualiza los tiempos de espera y no espera.</span><span class="sxs-lookup"><span data-stu-id="92d19-104">The `OnWaitStart` method updates times spent waiting and not waiting.</span></span>

## <a name="syntax"></a><span data-ttu-id="92d19-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d19-105">Syntax</span></span>


```C++
void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="92d19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92d19-106">Parameters</span></span>

<span data-ttu-id="92d19-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="92d19-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92d19-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92d19-108">Return value</span></span>

<span data-ttu-id="92d19-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="92d19-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92d19-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92d19-110">Remarks</span></span>

<span data-ttu-id="92d19-111">Se llama a esta función miembro cuando se inicia la espera de un evento de representación.</span><span class="sxs-lookup"><span data-stu-id="92d19-111">This member function is called when starting to wait for a rendering event.</span></span> <span data-ttu-id="92d19-112">Se usa solo para las mediciones de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="92d19-112">It is used only for performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="92d19-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92d19-113">Requirements</span></span>



| <span data-ttu-id="92d19-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92d19-114">Requirement</span></span> | <span data-ttu-id="92d19-115">Value</span><span class="sxs-lookup"><span data-stu-id="92d19-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d19-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92d19-116">Header</span></span><br/>  | <dl> <span data-ttu-id="92d19-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92d19-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92d19-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92d19-118">Library</span></span><br/> | <dl> <span data-ttu-id="92d19-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="92d19-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92d19-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="92d19-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92d19-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="92d19-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




