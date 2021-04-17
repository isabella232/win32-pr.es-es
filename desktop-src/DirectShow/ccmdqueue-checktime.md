---
description: El método CheckTime determina si se debe a una hora especificada.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Método CCmdQueue. CheckTime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681198"
---
# <a name="ccmdqueuechecktime-method"></a><span data-ttu-id="47f10-103">CCmdQueue. CheckTime, método</span><span class="sxs-lookup"><span data-stu-id="47f10-103">CCmdQueue.CheckTime method</span></span>

<span data-ttu-id="47f10-104">El `CheckTime` método determina si se debe a una hora especificada.</span><span class="sxs-lookup"><span data-stu-id="47f10-104">The `CheckTime` method determines if a specified time is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47f10-105">Syntax</span></span>


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a><span data-ttu-id="47f10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47f10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f10-107">*time*</span><span class="sxs-lookup"><span data-stu-id="47f10-107">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="47f10-108">Tiempo de comprobación.</span><span class="sxs-lookup"><span data-stu-id="47f10-108">Time to check.</span></span>

</dd> <dt>

<span data-ttu-id="47f10-109">*bStream*</span><span class="sxs-lookup"><span data-stu-id="47f10-109">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="47f10-110">**True** si el parámetro *Time* es un valor de tiempo de secuencia; **False** si la *hora* es un valor de tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="47f10-110">**TRUE** if the *time* parameter is a stream-time value; **FALSE** if *time* is a presentation-time value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f10-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47f10-111">Return value</span></span>

<span data-ttu-id="47f10-112">Devuelve **true** si aún no se ha pasado la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="47f10-112">Returns **TRUE** if the specified time has not yet passed.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f10-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47f10-113">Requirements</span></span>



| <span data-ttu-id="47f10-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47f10-114">Requirement</span></span> | <span data-ttu-id="47f10-115">Value</span><span class="sxs-lookup"><span data-stu-id="47f10-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f10-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47f10-116">Header</span></span><br/>  | <dl> <span data-ttu-id="47f10-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47f10-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47f10-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47f10-118">Library</span></span><br/> | <dl> <span data-ttu-id="47f10-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="47f10-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f10-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="47f10-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f10-121">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="47f10-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




