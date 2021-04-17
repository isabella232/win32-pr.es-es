---
description: La función ConvertToMilliseconds convierte una hora de referencia en milisegundos.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Función ConvertToMilliseconds (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670755"
---
# <a name="converttomilliseconds-function"></a><span data-ttu-id="0174e-103">ConvertToMilliseconds función)</span><span class="sxs-lookup"><span data-stu-id="0174e-103">ConvertToMilliseconds function</span></span>

<span data-ttu-id="0174e-104">La `ConvertToMilliseconds` función convierte una hora de referencia en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="0174e-104">The `ConvertToMilliseconds` function converts a reference time to milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="0174e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0174e-105">Syntax</span></span>


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a><span data-ttu-id="0174e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0174e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0174e-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="0174e-107">*RT* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0174e-108">Tiempo de referencia, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="0174e-108">Reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0174e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0174e-109">Return value</span></span>

<span data-ttu-id="0174e-110">Devuelve la hora de referencia convertida en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="0174e-110">Returns the reference time converted to milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="0174e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0174e-111">Requirements</span></span>



| <span data-ttu-id="0174e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0174e-112">Requirement</span></span> | <span data-ttu-id="0174e-113">Value</span><span class="sxs-lookup"><span data-stu-id="0174e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0174e-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0174e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0174e-115"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0174e-115"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0174e-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0174e-116">Library</span></span><br/> | <dl> <span data-ttu-id="0174e-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0174e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0174e-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0174e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0174e-119">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="0174e-119">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




