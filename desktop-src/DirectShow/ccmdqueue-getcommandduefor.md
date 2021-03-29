---
description: El método GetCommandDueFor recupera un comando diferido que está programado en un momento especificado.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Método CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678963"
---
# <a name="ccmdqueuegetcommandduefor-method"></a><span data-ttu-id="c8f55-103">CCmdQueue. GetCommandDueFor, método</span><span class="sxs-lookup"><span data-stu-id="c8f55-103">CCmdQueue.GetCommandDueFor method</span></span>

<span data-ttu-id="c8f55-104">El `GetCommandDueFor` método recupera un comando diferido que se programa en un momento especificado.</span><span class="sxs-lookup"><span data-stu-id="c8f55-104">The `GetCommandDueFor` method retrieves a deferred command that is scheduled at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8f55-105">Syntax</span></span>


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c8f55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8f55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f55-107">*tStream*</span><span class="sxs-lookup"><span data-stu-id="c8f55-107">*tStream*</span></span> 
</dt> <dd>

<span data-ttu-id="c8f55-108">Hora en la que se programa el comando.</span><span class="sxs-lookup"><span data-stu-id="c8f55-108">Time for which the command is scheduled.</span></span>

</dd> <dt>

<span data-ttu-id="c8f55-109">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="c8f55-109">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="c8f55-110">Dirección de un puntero al comando aplazado que se va a realizar en el momento especificado en el parámetro *tStream* .</span><span class="sxs-lookup"><span data-stu-id="c8f55-110">Address of a pointer to the deferred command to be carried out at the time specified in the *tStream* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f55-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8f55-111">Return value</span></span>

<span data-ttu-id="c8f55-112">Devuelve VFW \_ E \_ no \_ encontrado si no hay ningún comando pendiente; de lo contrario, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8f55-112">Returns VFW\_E\_NOT\_FOUND if no commands are due; otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f55-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8f55-113">Remarks</span></span>

<span data-ttu-id="c8f55-114">Esta función miembro toma un tiempo de secuencia y devuelve el comando diferido programado en ese momento.</span><span class="sxs-lookup"><span data-stu-id="c8f55-114">This member function takes a stream time and returns the deferred command scheduled at that time.</span></span> <span data-ttu-id="c8f55-115">El desplazamiento real en tiempo de secuencia se calcula cuando se ejecuta la cola de comandos.</span><span class="sxs-lookup"><span data-stu-id="c8f55-115">The actual stream-time offset is calculated when the command queue is run.</span></span> <span data-ttu-id="c8f55-116">Los comandos permanecen en la cola hasta que se ejecutan o se cancelan.</span><span class="sxs-lookup"><span data-stu-id="c8f55-116">Commands remain queued until run or canceled.</span></span> <span data-ttu-id="c8f55-117">Esta función miembro no se bloqueará.</span><span class="sxs-lookup"><span data-stu-id="c8f55-117">This member function will not block.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f55-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8f55-118">Requirements</span></span>



| <span data-ttu-id="c8f55-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f55-119">Requirement</span></span> | <span data-ttu-id="c8f55-120">Value</span><span class="sxs-lookup"><span data-stu-id="c8f55-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f55-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8f55-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c8f55-122"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f55-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8f55-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8f55-123">Library</span></span><br/> | <dl> <span data-ttu-id="c8f55-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f55-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f55-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8f55-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f55-126">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="c8f55-126">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




