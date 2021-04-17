---
description: El método CompleteConnect completa una conexión a un PIN de entrada.
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Método CBaseOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671108"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="0ccbd-103">CBaseOutputPin. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="0ccbd-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="0ccbd-104">El `CompleteConnect` método completa una conexión a un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ccbd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ccbd-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="0ccbd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ccbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ccbd-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="0ccbd-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="0ccbd-108">Puntero al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ccbd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ccbd-109">Return value</span></span>

<span data-ttu-id="0ccbd-110">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ccbd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ccbd-111">Remarks</span></span>

<span data-ttu-id="0ccbd-112">Este método invalida el método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0ccbd-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="0ccbd-113">Llama al método [**DecideAllocator**](cbaseoutputpin-decideallocator.md) , que selecciona el asignador de memoria que se va a usar para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="0ccbd-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ccbd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ccbd-114">Requirements</span></span>



| <span data-ttu-id="0ccbd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ccbd-115">Requirement</span></span> | <span data-ttu-id="0ccbd-116">Value</span><span class="sxs-lookup"><span data-stu-id="0ccbd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ccbd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ccbd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0ccbd-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ccbd-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ccbd-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ccbd-119">Library</span></span><br/> | <dl> <span data-ttu-id="0ccbd-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0ccbd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ccbd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ccbd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ccbd-122">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0ccbd-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




