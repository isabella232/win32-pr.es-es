---
description: El método reply responde a una solicitud.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Método CAMThread. reply (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690868"
---
# <a name="camthreadreply-method"></a><span data-ttu-id="2a38e-103">CAMThread. reply (método)</span><span class="sxs-lookup"><span data-stu-id="2a38e-103">CAMThread.Reply method</span></span>

<span data-ttu-id="2a38e-104">El `Reply` método responde a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a38e-104">The `Reply` method replies to a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a38e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a38e-105">Syntax</span></span>


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a><span data-ttu-id="2a38e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a38e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a38e-107">*dw*</span><span class="sxs-lookup"><span data-stu-id="2a38e-107">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="2a38e-108">Valor que se va a devolver en el método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="2a38e-108">Value to return in the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a38e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a38e-109">Return value</span></span>

<span data-ttu-id="2a38e-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2a38e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a38e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a38e-111">Remarks</span></span>

<span data-ttu-id="2a38e-112">El método CallWorker se bloquea hasta que se llama a este método.</span><span class="sxs-lookup"><span data-stu-id="2a38e-112">The CallWorker method blocks until this method is called.</span></span> <span data-ttu-id="2a38e-113">El parámetro *DW* proporciona el valor devuelto para CallWorker.</span><span class="sxs-lookup"><span data-stu-id="2a38e-113">The *dw* parameter supplies the return value for CallWorker.</span></span> <span data-ttu-id="2a38e-114">Llame a este método en el procedimiento del subproceso después de recuperar una solicitud, para liberar el subproceso que lo solicita.</span><span class="sxs-lookup"><span data-stu-id="2a38e-114">Call this method in your thread procedure after you retrieve a request, to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a38e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a38e-115">Requirements</span></span>



| <span data-ttu-id="2a38e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a38e-116">Requirement</span></span> | <span data-ttu-id="2a38e-117">Value</span><span class="sxs-lookup"><span data-stu-id="2a38e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a38e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a38e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2a38e-119"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a38e-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2a38e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a38e-120">Library</span></span><br/> | <dl> <span data-ttu-id="2a38e-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2a38e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a38e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a38e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a38e-123">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="2a38e-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




