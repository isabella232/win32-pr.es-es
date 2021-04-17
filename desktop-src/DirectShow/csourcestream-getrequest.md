---
description: El método GetRequest espera a la siguiente solicitud de subproceso.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: CSourceStream. GetRequest (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660905"
---
# <a name="csourcestreamgetrequest-method"></a><span data-ttu-id="40805-103">CSourceStream. GetRequest, método</span><span class="sxs-lookup"><span data-stu-id="40805-103">CSourceStream.GetRequest method</span></span>

<span data-ttu-id="40805-104">El `GetRequest` método espera a la siguiente solicitud de subproceso.</span><span class="sxs-lookup"><span data-stu-id="40805-104">The `GetRequest` method waits for the next thread request.</span></span>

## <a name="syntax"></a><span data-ttu-id="40805-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40805-105">Syntax</span></span>


```C++
Command GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="40805-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40805-106">Parameters</span></span>

<span data-ttu-id="40805-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="40805-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40805-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40805-108">Return value</span></span>

<span data-ttu-id="40805-109">Devuelve la siguiente solicitud de subproceso.</span><span class="sxs-lookup"><span data-stu-id="40805-109">Returns the next thread request.</span></span>

## <a name="remarks"></a><span data-ttu-id="40805-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40805-110">Remarks</span></span>

<span data-ttu-id="40805-111">Este método invalida el método [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="40805-111">This method overrides the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="40805-112">El valor devuelto se convierte al siguiente tipo enumerado:</span><span class="sxs-lookup"><span data-stu-id="40805-112">The return value is cast to the following enumerated type:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="40805-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40805-113">Requirements</span></span>



| <span data-ttu-id="40805-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="40805-114">Requirement</span></span> | <span data-ttu-id="40805-115">Value</span><span class="sxs-lookup"><span data-stu-id="40805-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40805-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40805-116">Header</span></span><br/>  | <dl> <span data-ttu-id="40805-117"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40805-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="40805-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40805-118">Library</span></span><br/> | <dl> <span data-ttu-id="40805-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="40805-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40805-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="40805-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40805-121">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="40805-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




