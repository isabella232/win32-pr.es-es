---
description: El método PAUSE indica al subproceso de streaming que se active.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Método CSourceStream. PAUSE (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680690"
---
# <a name="csourcestreampause-method"></a><span data-ttu-id="4b42b-103">CSourceStream. PAUSE (método)</span><span class="sxs-lookup"><span data-stu-id="4b42b-103">CSourceStream.Pause method</span></span>

<span data-ttu-id="4b42b-104">El `Pause` método indica al subproceso de streaming que se active.</span><span class="sxs-lookup"><span data-stu-id="4b42b-104">The `Pause` method signals the streaming thread to become active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b42b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b42b-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="4b42b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b42b-106">Parameters</span></span>

<span data-ttu-id="4b42b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4b42b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b42b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b42b-108">Return value</span></span>

<span data-ttu-id="4b42b-109">Devuelve S \_ correcto o E \_ inesperados.</span><span class="sxs-lookup"><span data-stu-id="4b42b-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b42b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b42b-110">Remarks</span></span>

<span data-ttu-id="4b42b-111">El método [**CSourceStream:: Active**](csourcestream-active.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="4b42b-111">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span> <span data-ttu-id="4b42b-112">Cuando el método [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) recibe esta solicitud, llama al método [**obufferprocessingloop de CSourceStream::D**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="4b42b-112">When the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method receives this request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b42b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b42b-113">Requirements</span></span>



| <span data-ttu-id="4b42b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b42b-114">Requirement</span></span> | <span data-ttu-id="4b42b-115">Value</span><span class="sxs-lookup"><span data-stu-id="4b42b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b42b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b42b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4b42b-117"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b42b-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b42b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b42b-118">Library</span></span><br/> | <dl> <span data-ttu-id="4b42b-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4b42b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b42b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b42b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b42b-121">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="4b42b-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




