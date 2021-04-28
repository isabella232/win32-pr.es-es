---
description: 'Método CTransformFilter.Pause: el método Pause pausa el filtro. Este método implementa el método IMediaFilter::P ause.'
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Método CTransformFilter.Pause (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095103"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="1ea6a-104">Método CTransformFilter.Pause</span><span class="sxs-lookup"><span data-stu-id="1ea6a-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="1ea6a-105">El `Pause` método pausa el filtro.</span><span class="sxs-lookup"><span data-stu-id="1ea6a-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="1ea6a-106">Este método implementa el [**método IMediaFilter::P ause.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)</span><span class="sxs-lookup"><span data-stu-id="1ea6a-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea6a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ea6a-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="1ea6a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ea6a-108">Parameters</span></span>

<span data-ttu-id="1ea6a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1ea6a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ea6a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ea6a-110">Return value</span></span>

<span data-ttu-id="1ea6a-111">Devuelve S \_ OK u otro valor **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1ea6a-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ea6a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ea6a-112">Remarks</span></span>

<span data-ttu-id="1ea6a-113">Este método llama al [**método StartStreaming.**](ctransformfilter-startstreaming.md)</span><span class="sxs-lookup"><span data-stu-id="1ea6a-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="1ea6a-114">El **método StartStreaming** no hace nada en la clase base, pero la clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="1ea6a-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea6a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ea6a-115">Requirements</span></span>



| <span data-ttu-id="1ea6a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ea6a-116">Requirement</span></span> | <span data-ttu-id="1ea6a-117">Value</span><span class="sxs-lookup"><span data-stu-id="1ea6a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea6a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ea6a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1ea6a-119"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ea6a-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1ea6a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ea6a-120">Library</span></span><br/> | <dl> <span data-ttu-id="1ea6a-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1ea6a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea6a-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ea6a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea6a-123">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="1ea6a-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




