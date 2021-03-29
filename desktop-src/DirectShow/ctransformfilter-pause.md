---
description: El método PAUSE pausa el filtro. Este método implementa el método IMediaFilter::P ause.
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Método CTransformFilter. PAUSE (Transfrm. h)
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
ms.openlocfilehash: 5408b9a39f92fd68eacb83474a18da0acda6b961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680820"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="2ae68-104">CTransformFilter. PAUSE (método)</span><span class="sxs-lookup"><span data-stu-id="2ae68-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="2ae68-105">El `Pause` método pausa el filtro.</span><span class="sxs-lookup"><span data-stu-id="2ae68-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="2ae68-106">Este método implementa el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="2ae68-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae68-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ae68-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="2ae68-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ae68-108">Parameters</span></span>

<span data-ttu-id="2ae68-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2ae68-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ae68-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ae68-110">Return value</span></span>

<span data-ttu-id="2ae68-111">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ae68-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae68-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ae68-112">Remarks</span></span>

<span data-ttu-id="2ae68-113">Este método llama al método [**StartStreaming**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae68-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="2ae68-114">El método **StartStreaming** no realiza ninguna acción en la clase base, pero la clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="2ae68-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae68-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae68-115">Requirements</span></span>



| <span data-ttu-id="2ae68-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae68-116">Requirement</span></span> | <span data-ttu-id="2ae68-117">Value</span><span class="sxs-lookup"><span data-stu-id="2ae68-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae68-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ae68-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2ae68-119"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ae68-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2ae68-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ae68-120">Library</span></span><br/> | <dl> <span data-ttu-id="2ae68-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2ae68-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae68-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ae68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae68-123">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="2ae68-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




