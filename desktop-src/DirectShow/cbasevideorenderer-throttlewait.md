---
description: El método ThrottleWait inserta un período de espera después de cada fotograma.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Método CBaseVideoRenderer. ThrottleWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679092"
---
# <a name="cbasevideorendererthrottlewait-method"></a><span data-ttu-id="53da0-103">CBaseVideoRenderer. ThrottleWait, método</span><span class="sxs-lookup"><span data-stu-id="53da0-103">CBaseVideoRenderer.ThrottleWait method</span></span>

<span data-ttu-id="53da0-104">El `ThrottleWait` método inserta un período de espera después de cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="53da0-104">The `ThrottleWait` method inserts a wait period after each frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="53da0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53da0-105">Syntax</span></span>


```C++
void ThrottleWait();
```



## <a name="parameters"></a><span data-ttu-id="53da0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53da0-106">Parameters</span></span>

<span data-ttu-id="53da0-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53da0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53da0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53da0-108">Return value</span></span>

<span data-ttu-id="53da0-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="53da0-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53da0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53da0-110">Remarks</span></span>

<span data-ttu-id="53da0-111">Esta función miembro espera un período de tiempo obtenido del miembro de datos **m \_ trThrottle** .</span><span class="sxs-lookup"><span data-stu-id="53da0-111">This member function waits for a time period obtained from the **m\_trThrottle** data member.</span></span>

## <a name="requirements"></a><span data-ttu-id="53da0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53da0-112">Requirements</span></span>



| <span data-ttu-id="53da0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="53da0-113">Requirement</span></span> | <span data-ttu-id="53da0-114">Value</span><span class="sxs-lookup"><span data-stu-id="53da0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53da0-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53da0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="53da0-116"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53da0-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="53da0-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53da0-117">Library</span></span><br/> | <dl> <span data-ttu-id="53da0-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="53da0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53da0-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="53da0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53da0-120">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="53da0-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




