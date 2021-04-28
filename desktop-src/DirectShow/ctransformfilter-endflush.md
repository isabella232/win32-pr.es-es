---
description: 'Método CTransformFilter.EndFlush: el método EndFlush finaliza una operación de vaciado.'
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Método CTransformFilter.EndFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085064"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="fe840-103">Método CTransformFilter.EndFlush</span><span class="sxs-lookup"><span data-stu-id="fe840-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="fe840-104">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="fe840-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe840-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe840-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="fe840-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe840-106">Parameters</span></span>

<span data-ttu-id="fe840-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fe840-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe840-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe840-108">Return value</span></span>

<span data-ttu-id="fe840-109">Devuelve S \_ OK u otro valor **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="fe840-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe840-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe840-110">Remarks</span></span>

<span data-ttu-id="fe840-111">Al final de una operación de vaciado, el método [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) del pin de entrada llama a este método.</span><span class="sxs-lookup"><span data-stu-id="fe840-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="fe840-112">Este método pasa la `EndFlush` llamada de bajada.</span><span class="sxs-lookup"><span data-stu-id="fe840-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="fe840-113">Si la clase derivada usa un subproceso de trabajo para entregar ejemplos, debe descartar los datos en cola antes de enviar la `EndFlush` llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="fe840-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="fe840-114">Para obtener más información, [vea Data Flow para desarrolladores de filtros.](data-flow-for-filter-developers.md)</span><span class="sxs-lookup"><span data-stu-id="fe840-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe840-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe840-115">Requirements</span></span>



| <span data-ttu-id="fe840-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe840-116">Requirement</span></span> | <span data-ttu-id="fe840-117">Value</span><span class="sxs-lookup"><span data-stu-id="fe840-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe840-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe840-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fe840-119"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe840-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe840-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe840-120">Library</span></span><br/> | <dl> <span data-ttu-id="fe840-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fe840-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe840-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe840-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe840-123">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="fe840-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




