---
description: 'Método CBaseInputPin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Método CBaseInputPin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099743"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="05f5e-103">Método CBaseInputPin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="05f5e-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="05f5e-104">El `BreakConnect` método libera el pin de una conexión.</span><span class="sxs-lookup"><span data-stu-id="05f5e-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05f5e-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="05f5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05f5e-106">Parameters</span></span>

<span data-ttu-id="05f5e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="05f5e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05f5e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05f5e-108">Return value</span></span>

<span data-ttu-id="05f5e-109">Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="05f5e-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f5e-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05f5e-110">Remarks</span></span>

<span data-ttu-id="05f5e-111">Este método invalida el [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="05f5e-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="05f5e-112">Desasigna el asignador y libera la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)</span><span class="sxs-lookup"><span data-stu-id="05f5e-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="05f5e-113">Si invalida este método, llame al método de clase base desde el método de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="05f5e-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="05f5e-114">De lo contrario, podría provocar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="05f5e-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f5e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05f5e-115">Requirements</span></span>



| <span data-ttu-id="05f5e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f5e-116">Requirement</span></span> | <span data-ttu-id="05f5e-117">Value</span><span class="sxs-lookup"><span data-stu-id="05f5e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f5e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05f5e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="05f5e-119"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="05f5e-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="05f5e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05f5e-120">Library</span></span><br/> | <dl> <span data-ttu-id="05f5e-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="05f5e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f5e-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="05f5e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f5e-123">**CBaseInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="05f5e-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




