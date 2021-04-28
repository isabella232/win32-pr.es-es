---
description: 'Método CTransformFilter.BeginFlush: el método BeginFlush comienza una operación de vaciado.'
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Método CTransformFilter.BeginFlush (Transfrm.h)
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
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085163"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="aabab-103">Método CTransformFilter.BeginFlush</span><span class="sxs-lookup"><span data-stu-id="aabab-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="aabab-104">El `BeginFlush` método comienza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="aabab-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aabab-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="aabab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aabab-106">Parameters</span></span>

<span data-ttu-id="aabab-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="aabab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aabab-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aabab-108">Return value</span></span>

<span data-ttu-id="aabab-109">Devuelve S \_ OK u otro valor **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="aabab-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aabab-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aabab-110">Remarks</span></span>

<span data-ttu-id="aabab-111">Al principio de una operación de vaciado, el método [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) del pin de entrada llama a este método.</span><span class="sxs-lookup"><span data-stu-id="aabab-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="aabab-112">Este método pasa la `BeginFlush` llamada de bajada.</span><span class="sxs-lookup"><span data-stu-id="aabab-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="aabab-113">Si la clase derivada usa un subproceso de trabajo para entregar ejemplos, debe descartar los datos en cola durante una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="aabab-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="aabab-114">Esto se puede hacer en el `BeginFlush` método o en el método [**EndFlush.**](ctransformfilter-endflush.md)</span><span class="sxs-lookup"><span data-stu-id="aabab-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="aabab-115">Sin embargo, tenga en cuenta que las `BeginFlush` llamadas a no se sincronizan con el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="aabab-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="aabab-116">Si el método descarta los datos en cola, el filtro debe tener cuidado de no procesar más datos entre `BeginFlush` las llamadas a y `BeginFlush` **EndFlush.**</span><span class="sxs-lookup"><span data-stu-id="aabab-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="aabab-117">Para obtener más información, [vea Data Flow para desarrolladores de filtros.](data-flow-for-filter-developers.md)</span><span class="sxs-lookup"><span data-stu-id="aabab-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aabab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aabab-118">Requirements</span></span>



| <span data-ttu-id="aabab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aabab-119">Requirement</span></span> | <span data-ttu-id="aabab-120">Value</span><span class="sxs-lookup"><span data-stu-id="aabab-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aabab-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aabab-121">Header</span></span><br/>  | <dl> <span data-ttu-id="aabab-122"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="aabab-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aabab-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aabab-123">Library</span></span><br/> | <dl> <span data-ttu-id="aabab-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="aabab-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aabab-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aabab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabab-126">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="aabab-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




