---
description: 'Método CBaseFilter.Pause: el método Pause pausa el filtro. Este método implementa el método IMediaFilter::P ause.'
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Método CBaseFilter.Pause (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120093"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="9fe96-104">Método CBaseFilter.Pause</span><span class="sxs-lookup"><span data-stu-id="9fe96-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="9fe96-105">El `Pause` método pausa el filtro.</span><span class="sxs-lookup"><span data-stu-id="9fe96-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="9fe96-106">Este método implementa el [**método IMediaFilter::P ause.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)</span><span class="sxs-lookup"><span data-stu-id="9fe96-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe96-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fe96-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="9fe96-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fe96-108">Parameters</span></span>

<span data-ttu-id="9fe96-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9fe96-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9fe96-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fe96-110">Return value</span></span>

<span data-ttu-id="9fe96-111">Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="9fe96-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fe96-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fe96-112">Remarks</span></span>

<span data-ttu-id="9fe96-113">Este método llama al [**método CBasePin::Active**](cbasepin-active.md) en cada uno de los pines conectados del filtro.</span><span class="sxs-lookup"><span data-stu-id="9fe96-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe96-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fe96-114">Requirements</span></span>



| <span data-ttu-id="9fe96-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe96-115">Requirement</span></span> | <span data-ttu-id="9fe96-116">Value</span><span class="sxs-lookup"><span data-stu-id="9fe96-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe96-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fe96-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9fe96-118"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fe96-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9fe96-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fe96-119">Library</span></span><br/> | <dl> <span data-ttu-id="9fe96-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9fe96-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fe96-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9fe96-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe96-122">**CBaseFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="9fe96-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




