---
description: 'Método CBaseOutputPin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Método CBaseOutputPin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: 746783a73892bc34273da4b020446f2668a19cd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096223"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="50223-103">Método CBaseOutputPin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="50223-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="50223-104">El `BreakConnect` método libera el pin de una conexión.</span><span class="sxs-lookup"><span data-stu-id="50223-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="50223-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50223-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="50223-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50223-106">Parameters</span></span>

<span data-ttu-id="50223-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="50223-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50223-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50223-108">Return value</span></span>

<span data-ttu-id="50223-109">Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="50223-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="50223-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50223-110">Remarks</span></span>

<span data-ttu-id="50223-111">Este método invalida el [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="50223-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="50223-112">Desasigna el asignador y libera las interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) [**e IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="50223-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="50223-113">Si invalida este método, llame al método de clase base desde el método de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="50223-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="50223-114">De lo contrario, podría provocar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="50223-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="50223-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50223-115">Requirements</span></span>



| <span data-ttu-id="50223-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="50223-116">Requirement</span></span> | <span data-ttu-id="50223-117">Value</span><span class="sxs-lookup"><span data-stu-id="50223-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50223-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50223-118">Header</span></span><br/>  | <dl> <span data-ttu-id="50223-119"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="50223-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="50223-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50223-120">Library</span></span><br/> | <dl> <span data-ttu-id="50223-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="50223-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50223-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50223-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50223-123">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="50223-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




