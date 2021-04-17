---
description: Se llama al método activo cuando el estado cambia a en pausa o en ejecución.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Método CBaseRenderer. Active (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671083"
---
# <a name="cbaserendereractive-method"></a><span data-ttu-id="67858-103">CBaseRenderer. Active (método)</span><span class="sxs-lookup"><span data-stu-id="67858-103">CBaseRenderer.Active method</span></span>

<span data-ttu-id="67858-104">`Active`Se llama al método cuando el estado se cambia a en pausa o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="67858-104">The `Active` method is called when the state is switched to paused or running.</span></span>

## <a name="syntax"></a><span data-ttu-id="67858-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67858-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="67858-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67858-106">Parameters</span></span>

<span data-ttu-id="67858-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="67858-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67858-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67858-108">Return value</span></span>

<span data-ttu-id="67858-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="67858-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="67858-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67858-110">Remarks</span></span>

<span data-ttu-id="67858-111">El PIN de entrada llama a este método desde su propio método [**CRendererInputPin:: Active**](crendererinputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="67858-111">The input pin calls this method from its own [**CRendererInputPin::Active**](crendererinputpin-active.md) method.</span></span> <span data-ttu-id="67858-112">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="67858-112">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="67858-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67858-113">Requirements</span></span>



| <span data-ttu-id="67858-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67858-114">Requirement</span></span> | <span data-ttu-id="67858-115">Value</span><span class="sxs-lookup"><span data-stu-id="67858-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67858-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67858-116">Header</span></span><br/>  | <dl> <span data-ttu-id="67858-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67858-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67858-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67858-118">Library</span></span><br/> | <dl> <span data-ttu-id="67858-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="67858-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67858-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="67858-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67858-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="67858-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




