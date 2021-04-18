---
description: El método GetDueCommand recupera un puntero al siguiente comando que se debe a.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Método CCmdQueue. GetDueCommand (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660170"
---
# <a name="ccmdqueuegetduecommand-method"></a><span data-ttu-id="346de-103">CCmdQueue. GetDueCommand, método</span><span class="sxs-lookup"><span data-stu-id="346de-103">CCmdQueue.GetDueCommand method</span></span>

<span data-ttu-id="346de-104">El `GetDueCommand` método recupera un puntero al siguiente comando que se debe a.</span><span class="sxs-lookup"><span data-stu-id="346de-104">The `GetDueCommand` method retrieves a pointer to the next command that is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="346de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="346de-105">Syntax</span></span>


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="346de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="346de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="346de-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="346de-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="346de-108">Dirección de un puntero al comando aplazado.</span><span class="sxs-lookup"><span data-stu-id="346de-108">Address of a pointer to the deferred command.</span></span>

</dd> <dt>

<span data-ttu-id="346de-109">*msTimeout*</span><span class="sxs-lookup"><span data-stu-id="346de-109">*msTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="346de-110">Cantidad de tiempo que hay que esperar antes de que se agote el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="346de-110">Amount of time to wait before carrying out the time-out.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="346de-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="346de-111">Return value</span></span>

<span data-ttu-id="346de-112">Devuelve E \_ Abort si se agota el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="346de-112">Returns E\_ABORT if a time-out occurs.</span></span> <span data-ttu-id="346de-113">Devuelve \_ si es correcto; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="346de-113">Returns S\_OK if successful; otherwise, returns an error.</span></span> <span data-ttu-id="346de-114">Devuelve un objeto que se ha incrementado mediante **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="346de-114">Returns an object that has been incremented using **IUnknown::AddRef**.</span></span>

## <a name="remarks"></a><span data-ttu-id="346de-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="346de-115">Remarks</span></span>

<span data-ttu-id="346de-116">Esta función miembro se bloquea hasta que se venza un comando pendiente.</span><span class="sxs-lookup"><span data-stu-id="346de-116">This member function blocks until a pending command is due.</span></span> <span data-ttu-id="346de-117">La función miembro se bloquea durante el tiempo, en milisegundos, especificado en el parámetro *msTimeout* .</span><span class="sxs-lookup"><span data-stu-id="346de-117">The member function blocks for the amount of time, in milliseconds, specified in the *msTimeout* parameter.</span></span> <span data-ttu-id="346de-118">Los comandos de tiempo de secuencia solo se deben realizar entre las funciones miembro [**CCmdQueue:: Run**](ccmdqueue-run.md) y [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) .</span><span class="sxs-lookup"><span data-stu-id="346de-118">Stream-time commands become due only between the [**CCmdQueue::Run**](ccmdqueue-run.md) and [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) member functions.</span></span> <span data-ttu-id="346de-119">El comando permanece en cola hasta que se ejecuta o se cancela.</span><span class="sxs-lookup"><span data-stu-id="346de-119">The command remains queued until run or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="346de-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="346de-120">Requirements</span></span>



| <span data-ttu-id="346de-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="346de-121">Requirement</span></span> | <span data-ttu-id="346de-122">Value</span><span class="sxs-lookup"><span data-stu-id="346de-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346de-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="346de-123">Header</span></span><br/>  | <dl> <span data-ttu-id="346de-124"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="346de-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="346de-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="346de-125">Library</span></span><br/> | <dl> <span data-ttu-id="346de-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="346de-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346de-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="346de-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346de-128">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="346de-128">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




