---
description: Se llama al método OnStartStreaming cuando el filtro comienza el streaming.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Método CBaseRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660571"
---
# <a name="cbaserendereronstartstreaming-method"></a><span data-ttu-id="46975-103">CBaseRenderer. OnStartStreaming, método</span><span class="sxs-lookup"><span data-stu-id="46975-103">CBaseRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="46975-104">`OnStartStreaming`Se llama al método cuando el filtro comienza el streaming.</span><span class="sxs-lookup"><span data-stu-id="46975-104">The `OnStartStreaming` method is called when the filter begins streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="46975-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46975-105">Syntax</span></span>


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="46975-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46975-106">Parameters</span></span>

<span data-ttu-id="46975-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="46975-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46975-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46975-108">Return value</span></span>

<span data-ttu-id="46975-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="46975-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="46975-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46975-110">Remarks</span></span>

<span data-ttu-id="46975-111">El método [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="46975-111">The [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method calls this method.</span></span> <span data-ttu-id="46975-112">No realiza ninguna acción en la clase base, pero la clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="46975-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="46975-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46975-113">Requirements</span></span>



| <span data-ttu-id="46975-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46975-114">Requirement</span></span> | <span data-ttu-id="46975-115">Value</span><span class="sxs-lookup"><span data-stu-id="46975-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46975-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46975-116">Header</span></span><br/>  | <dl> <span data-ttu-id="46975-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46975-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46975-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46975-118">Library</span></span><br/> | <dl> <span data-ttu-id="46975-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="46975-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46975-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="46975-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46975-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="46975-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




