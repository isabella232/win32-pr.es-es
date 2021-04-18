---
description: El método GetDueHandle recupera el identificador de evento que se va a señalar.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Método CCmdQueue. GetDueHandle (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678959"
---
# <a name="ccmdqueuegetduehandle-method"></a><span data-ttu-id="a4861-103">CCmdQueue. GetDueHandle, método</span><span class="sxs-lookup"><span data-stu-id="a4861-103">CCmdQueue.GetDueHandle method</span></span>

<span data-ttu-id="a4861-104">El `GetDueHandle` método recupera el identificador de evento que se va a señalar.</span><span class="sxs-lookup"><span data-stu-id="a4861-104">The `GetDueHandle` method retrieves the event handle to be signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4861-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4861-105">Syntax</span></span>


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a><span data-ttu-id="a4861-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4861-106">Parameters</span></span>

<span data-ttu-id="a4861-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a4861-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4861-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4861-108">Return value</span></span>

<span data-ttu-id="a4861-109">Devuelve el identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="a4861-109">Returns the event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4861-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4861-110">Remarks</span></span>

<span data-ttu-id="a4861-111">Devuelva el identificador de evento siempre que haya comandos diferidos que deban ejecutarse (cuando [**CCmdQueue:: GetDueCommand**](ccmdqueue-getduecommand.md) no se bloquee).</span><span class="sxs-lookup"><span data-stu-id="a4861-111">Return the event handle whenever there are deferred commands that are due for execution (when [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) will not block).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4861-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4861-112">Requirements</span></span>



| <span data-ttu-id="a4861-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4861-113">Requirement</span></span> | <span data-ttu-id="a4861-114">Value</span><span class="sxs-lookup"><span data-stu-id="a4861-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4861-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4861-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a4861-116"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4861-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4861-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4861-117">Library</span></span><br/> | <dl> <span data-ttu-id="a4861-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a4861-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4861-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4861-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4861-120">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="a4861-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




