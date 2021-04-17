---
description: El método BeginFlush inicia una operación de vaciado.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Método CTransformFilter. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660304"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="6fce2-103">CTransformFilter. BeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="6fce2-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="6fce2-104">El `BeginFlush` método inicia una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="6fce2-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fce2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fce2-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="6fce2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fce2-106">Parameters</span></span>

<span data-ttu-id="6fce2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6fce2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6fce2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fce2-108">Return value</span></span>

<span data-ttu-id="6fce2-109">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fce2-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fce2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fce2-110">Remarks</span></span>

<span data-ttu-id="6fce2-111">Al inicio de una operación de vaciado, el método [**CTransformInputPin:: BeginFlush**](ctransforminputpin-beginflush.md) del PIN de entrada llama a este método.</span><span class="sxs-lookup"><span data-stu-id="6fce2-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="6fce2-112">Este método pasa la `BeginFlush` llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="6fce2-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="6fce2-113">Si la clase derivada usa un subproceso de trabajo para proporcionar ejemplos, debe descartar todos los datos en cola durante una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="6fce2-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="6fce2-114">Esto puede hacerse en el `BeginFlush` método o en el método [**EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="6fce2-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="6fce2-115">Sin embargo, tenga en cuenta que las llamadas a `BeginFlush` no se sincronizan con el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="6fce2-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="6fce2-116">Si el `BeginFlush` método descarta los datos en cola, el filtro debe tener cuidado de no procesar más datos entre las `BeginFlush` llamadas a y **EndFlush** .</span><span class="sxs-lookup"><span data-stu-id="6fce2-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="6fce2-117">Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="6fce2-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fce2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fce2-118">Requirements</span></span>



| <span data-ttu-id="6fce2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fce2-119">Requirement</span></span> | <span data-ttu-id="6fce2-120">Value</span><span class="sxs-lookup"><span data-stu-id="6fce2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fce2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fce2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6fce2-122"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fce2-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6fce2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fce2-123">Library</span></span><br/> | <dl> <span data-ttu-id="6fce2-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6fce2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fce2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fce2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fce2-126">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="6fce2-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




