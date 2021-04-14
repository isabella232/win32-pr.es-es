---
description: El método CompleteConnect completa una conexión a un PIN de entrada.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Método CDynamicOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661355"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="95fc9-103">CDynamicOutputPin. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="95fc9-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="95fc9-104">El `CompleteConnect` método completa una conexión a un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="95fc9-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="95fc9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95fc9-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="95fc9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95fc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95fc9-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="95fc9-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="95fc9-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="95fc9-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95fc9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95fc9-109">Return value</span></span>

<span data-ttu-id="95fc9-110">Devuelve S \_ correcto si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="95fc9-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="95fc9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95fc9-111">Remarks</span></span>

<span data-ttu-id="95fc9-112">Este método invalida el método [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="95fc9-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="95fc9-113">Para admitir reconexiones dinámicas, este método confirma el asignador si el filtro está activo.</span><span class="sxs-lookup"><span data-stu-id="95fc9-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="95fc9-114">En la clase base, las conexiones solo se pueden producir cuando se detiene el filtro, por lo que el asignador siempre se confirma en el método [**CBaseOutputPin:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="95fc9-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="95fc9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95fc9-115">Requirements</span></span>



| <span data-ttu-id="95fc9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="95fc9-116">Requirement</span></span> | <span data-ttu-id="95fc9-117">Value</span><span class="sxs-lookup"><span data-stu-id="95fc9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fc9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95fc9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="95fc9-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95fc9-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95fc9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95fc9-120">Library</span></span><br/> | <dl> <span data-ttu-id="95fc9-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="95fc9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95fc9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="95fc9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95fc9-123">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="95fc9-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




