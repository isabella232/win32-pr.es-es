---
description: El método Inactive cierra el subproceso de trabajo que extrae los datos del terminal de salida. Este método también anula la confirmación del asignador.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Método CPullPin. Inactive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671384"
---
# <a name="cpullpininactive-method"></a><span data-ttu-id="68648-104">CPullPin. Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="68648-104">CPullPin.Inactive method</span></span>

<span data-ttu-id="68648-105">El `Inactive` método cierra el subproceso de trabajo que extrae los datos del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="68648-105">The `Inactive` method shuts down the worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="68648-106">Este método también anula la confirmación del asignador.</span><span class="sxs-lookup"><span data-stu-id="68648-106">This method also decommits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="68648-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68648-107">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="68648-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68648-108">Parameters</span></span>

<span data-ttu-id="68648-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="68648-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68648-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68648-110">Return value</span></span>

<span data-ttu-id="68648-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="68648-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="68648-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68648-112">Remarks</span></span>

<span data-ttu-id="68648-113">Llame a este método cuando el filtro propietario se vuelva inactivo.</span><span class="sxs-lookup"><span data-stu-id="68648-113">Call this method when the owning filter becomes inactive.</span></span> <span data-ttu-id="68648-114">(Si el PIN de entrada se deriva de [**CBasePin**](cbasepin.md), invalide el método [**CBasePin:: Inactive**](cbasepin-inactive.md) ).</span><span class="sxs-lookup"><span data-stu-id="68648-114">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Inactive**](cbasepin-inactive.md) method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="68648-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68648-115">Requirements</span></span>



| <span data-ttu-id="68648-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="68648-116">Requirement</span></span> | <span data-ttu-id="68648-117">Value</span><span class="sxs-lookup"><span data-stu-id="68648-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68648-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68648-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68648-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="68648-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="68648-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68648-120">Library</span></span><br/> | <dl> <span data-ttu-id="68648-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="68648-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68648-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="68648-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68648-123">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="68648-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




