---
description: El método indica que aún no se ha completado una transición de estado.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Método CBaseRenderer. (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671745"
---
# <a name="cbaserenderernotready-method"></a><span data-ttu-id="e6d22-103">CBaseRenderer. (método)</span><span class="sxs-lookup"><span data-stu-id="e6d22-103">CBaseRenderer.NotReady method</span></span>

<span data-ttu-id="e6d22-104">El `NotReady` método indica que aún no se ha completado una transición de estado.</span><span class="sxs-lookup"><span data-stu-id="e6d22-104">The `NotReady` method signals that a state transition is not yet complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6d22-105">Syntax</span></span>


```C++
void NotReady();
```



## <a name="parameters"></a><span data-ttu-id="e6d22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6d22-106">Parameters</span></span>

<span data-ttu-id="e6d22-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e6d22-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6d22-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6d22-108">Return value</span></span>

<span data-ttu-id="e6d22-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6d22-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6d22-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6d22-110">Remarks</span></span>

<span data-ttu-id="e6d22-111">Este método hace que el método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) devuelva un \_ Estado VFW S \_ \_ Intermediate, lo que indica que el filtro sigue pasando a su estado actual.</span><span class="sxs-lookup"><span data-stu-id="e6d22-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return VFW\_S\_STATE\_INTERMEDIATE, which indicates that the filter is still transitioning to its current state.</span></span> <span data-ttu-id="e6d22-112">El filtro llama a este método cada vez que hay pendiente una transición de estado.</span><span class="sxs-lookup"><span data-stu-id="e6d22-112">The filter calls this method whenever a state transition is pending.</span></span> <span data-ttu-id="e6d22-113">(Esto sucede cuando el filtro se detiene, hasta que recibe un ejemplo).</span><span class="sxs-lookup"><span data-stu-id="e6d22-113">(This occurs when the filter pauses, until it receives a sample.)</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d22-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d22-114">Requirements</span></span>



| <span data-ttu-id="e6d22-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d22-115">Requirement</span></span> | <span data-ttu-id="e6d22-116">Value</span><span class="sxs-lookup"><span data-stu-id="e6d22-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d22-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6d22-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e6d22-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d22-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6d22-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6d22-119">Library</span></span><br/> | <dl> <span data-ttu-id="e6d22-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d22-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6d22-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6d22-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d22-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e6d22-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="e6d22-123">**CheckReady**</span><span class="sxs-lookup"><span data-stu-id="e6d22-123">**CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="e6d22-124">**Ready**</span><span class="sxs-lookup"><span data-stu-id="e6d22-124">**Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




