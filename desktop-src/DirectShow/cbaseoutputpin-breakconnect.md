---
description: El método BreakConnect libera el PIN de una conexión.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Método CBaseOutputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660799"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="fa351-103">CBaseOutputPin. BreakConnect, método</span><span class="sxs-lookup"><span data-stu-id="fa351-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="fa351-104">El `BreakConnect` método libera el PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="fa351-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa351-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa351-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="fa351-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa351-106">Parameters</span></span>

<span data-ttu-id="fa351-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fa351-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa351-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa351-108">Return value</span></span>

<span data-ttu-id="fa351-109">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="fa351-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa351-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa351-110">Remarks</span></span>

<span data-ttu-id="fa351-111">Este método invalida el método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="fa351-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="fa351-112">Desconfirma el asignador y libera las interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) y [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="fa351-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="fa351-113">Si invalida este método, llame al método de la clase base desde el método de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="fa351-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="fa351-114">De lo contrario, podría producir fugas de memoria.</span><span class="sxs-lookup"><span data-stu-id="fa351-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa351-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa351-115">Requirements</span></span>



| <span data-ttu-id="fa351-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa351-116">Requirement</span></span> | <span data-ttu-id="fa351-117">Value</span><span class="sxs-lookup"><span data-stu-id="fa351-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa351-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa351-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fa351-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa351-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fa351-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa351-120">Library</span></span><br/> | <dl> <span data-ttu-id="fa351-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fa351-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa351-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa351-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa351-123">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="fa351-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




