---
description: Se llama al método OnThreadCreate cuando se inicializa el subproceso de streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: CSourceStream. OnThreadCreate (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660902"
---
# <a name="csourcestreamonthreadcreate-method"></a><span data-ttu-id="13d77-103">CSourceStream. OnThreadCreate, método</span><span class="sxs-lookup"><span data-stu-id="13d77-103">CSourceStream.OnThreadCreate method</span></span>

<span data-ttu-id="13d77-104">`OnThreadCreate`Se llama al método cuando se inicializa el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="13d77-104">The `OnThreadCreate` method is called when the streaming thread is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d77-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13d77-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a><span data-ttu-id="13d77-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13d77-106">Parameters</span></span>

<span data-ttu-id="13d77-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="13d77-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13d77-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13d77-108">Return value</span></span>

<span data-ttu-id="13d77-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="13d77-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="13d77-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13d77-110">Remarks</span></span>

<span data-ttu-id="13d77-111">El procedimiento de subproceso, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), llama a este método cuando recibe por primera vez una solicitud [**CSourceStream:: init**](csourcestream-init.md) .</span><span class="sxs-lookup"><span data-stu-id="13d77-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method when it first receives a [**CSourceStream::Init**](csourcestream-init.md) request.</span></span> <span data-ttu-id="13d77-112">El método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="13d77-112">The method does nothing in the base class.</span></span> <span data-ttu-id="13d77-113">La clase derivada puede invalidar este método para realizar inicializaciones de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="13d77-113">The derived class can override this method to perform thread initializations.</span></span> <span data-ttu-id="13d77-114">Si la clase derivada devuelve un código de error, el subproceso se cierra con un error.</span><span class="sxs-lookup"><span data-stu-id="13d77-114">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d77-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d77-115">Requirements</span></span>



| <span data-ttu-id="13d77-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d77-116">Requirement</span></span> | <span data-ttu-id="13d77-117">Value</span><span class="sxs-lookup"><span data-stu-id="13d77-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d77-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13d77-118">Header</span></span><br/>  | <dl> <span data-ttu-id="13d77-119"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13d77-119"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="13d77-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13d77-120">Library</span></span><br/> | <dl> <span data-ttu-id="13d77-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="13d77-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d77-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="13d77-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d77-123">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="13d77-123">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




