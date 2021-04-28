---
description: 'Destructor DE LAVTHREAD.~CAMThread: método destructor.'
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Destructor CAMThread.~CAMThread (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096443"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="00424-103">Destructor CAMThread.~CAMThread</span><span class="sxs-lookup"><span data-stu-id="00424-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="00424-104">Método destructor.</span><span class="sxs-lookup"><span data-stu-id="00424-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00424-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00424-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="00424-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00424-106">Remarks</span></span>

<span data-ttu-id="00424-107">El destructor llama al [**método CAMThread::Close,**](camthread-close.md) que espera a que se cierre el subproceso.</span><span class="sxs-lookup"><span data-stu-id="00424-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="00424-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00424-108">Requirements</span></span>



| <span data-ttu-id="00424-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="00424-109">Requirement</span></span> | <span data-ttu-id="00424-110">Value</span><span class="sxs-lookup"><span data-stu-id="00424-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00424-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00424-111">Header</span></span><br/>  | <dl> <span data-ttu-id="00424-112"><dt>Wxutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="00424-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="00424-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00424-113">Library</span></span><br/> | <dl> <span data-ttu-id="00424-114"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="00424-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00424-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00424-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00424-116">**CLASE CAMThread**</span><span class="sxs-lookup"><span data-stu-id="00424-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




