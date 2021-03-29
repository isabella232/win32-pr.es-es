---
description: El método BreakConnect libera el PIN de una conexión.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Método CBaseInputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6981ef97b98cc25b1996f1599d6d66b8e7d41f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660572"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="69b39-103">CBaseInputPin. BreakConnect, método</span><span class="sxs-lookup"><span data-stu-id="69b39-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="69b39-104">El `BreakConnect` método libera el PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="69b39-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b39-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69b39-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="69b39-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69b39-106">Parameters</span></span>

<span data-ttu-id="69b39-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="69b39-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69b39-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69b39-108">Return value</span></span>

<span data-ttu-id="69b39-109">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="69b39-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b39-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69b39-110">Remarks</span></span>

<span data-ttu-id="69b39-111">Este método invalida el método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="69b39-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="69b39-112">Desconfirma el asignador y libera la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="69b39-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="69b39-113">Si invalida este método, llame al método de la clase base desde el método de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="69b39-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="69b39-114">De lo contrario, podría producir fugas de memoria.</span><span class="sxs-lookup"><span data-stu-id="69b39-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b39-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b39-115">Requirements</span></span>



| <span data-ttu-id="69b39-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b39-116">Requirement</span></span> | <span data-ttu-id="69b39-117">Value</span><span class="sxs-lookup"><span data-stu-id="69b39-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b39-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69b39-118">Header</span></span><br/>  | <dl> <span data-ttu-id="69b39-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69b39-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="69b39-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69b39-120">Library</span></span><br/> | <dl> <span data-ttu-id="69b39-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="69b39-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b39-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="69b39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b39-123">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="69b39-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




