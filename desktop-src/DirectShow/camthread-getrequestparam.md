---
description: El método GetRequestParam recupera la solicitud más reciente.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Método CAMThread. GetRequestParam (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690683"
---
# <a name="camthreadgetrequestparam-method"></a><span data-ttu-id="27bda-103">CAMThread. GetRequestParam, método</span><span class="sxs-lookup"><span data-stu-id="27bda-103">CAMThread.GetRequestParam method</span></span>

<span data-ttu-id="27bda-104">El `GetRequestParam` método recupera la solicitud más reciente.</span><span class="sxs-lookup"><span data-stu-id="27bda-104">The `GetRequestParam` method retrieves the latest request.</span></span>

## <a name="syntax"></a><span data-ttu-id="27bda-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27bda-105">Syntax</span></span>


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a><span data-ttu-id="27bda-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27bda-106">Parameters</span></span>

<span data-ttu-id="27bda-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="27bda-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27bda-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27bda-108">Return value</span></span>

<span data-ttu-id="27bda-109">Devuelve el valor del parámetro que se pasó más recientemente al método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="27bda-109">Returns the value of the parameter that was passed most recently to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="27bda-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27bda-110">Requirements</span></span>



| <span data-ttu-id="27bda-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="27bda-111">Requirement</span></span> | <span data-ttu-id="27bda-112">Value</span><span class="sxs-lookup"><span data-stu-id="27bda-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27bda-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27bda-113">Header</span></span><br/>  | <dl> <span data-ttu-id="27bda-114"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27bda-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="27bda-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27bda-115">Library</span></span><br/> | <dl> <span data-ttu-id="27bda-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="27bda-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27bda-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="27bda-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27bda-118">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="27bda-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




