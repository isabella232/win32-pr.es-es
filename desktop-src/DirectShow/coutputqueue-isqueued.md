---
description: El método IsQueued determina si el objeto está utilizando un subproceso de trabajo para proporcionar ejemplos.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Método COutputQueue. IsQueued (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670601"
---
# <a name="coutputqueueisqueued-method"></a><span data-ttu-id="bfa89-103">COutputQueue. IsQueued, método</span><span class="sxs-lookup"><span data-stu-id="bfa89-103">COutputQueue.IsQueued method</span></span>

<span data-ttu-id="bfa89-104">El `IsQueued` método determina si el objeto está utilizando un subproceso de trabajo para proporcionar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="bfa89-104">The `IsQueued` method determines whether the object is using a worker thread to deliver samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfa89-105">Syntax</span></span>


```C++
BOOL IsQueued();
```



## <a name="parameters"></a><span data-ttu-id="bfa89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfa89-106">Parameters</span></span>

<span data-ttu-id="bfa89-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bfa89-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfa89-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfa89-108">Return value</span></span>

<span data-ttu-id="bfa89-109">Devuelve **true** si el objeto está utilizando un subproceso de trabajo o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bfa89-109">Returns **TRUE** if the object is using a worker thread, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa89-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfa89-110">Requirements</span></span>



| <span data-ttu-id="bfa89-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa89-111">Requirement</span></span> | <span data-ttu-id="bfa89-112">Value</span><span class="sxs-lookup"><span data-stu-id="bfa89-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa89-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfa89-113">Header</span></span><br/>  | <dl> <span data-ttu-id="bfa89-114"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa89-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bfa89-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfa89-115">Library</span></span><br/> | <dl> <span data-ttu-id="bfa89-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bfa89-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa89-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfa89-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa89-118">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="bfa89-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




