---
description: Se llama al método OnThreadDestroy cuando el subproceso de streaming está a punto de salir.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: CSourceStream. OnThreadDestroy (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660901"
---
# <a name="csourcestreamonthreaddestroy-method"></a><span data-ttu-id="a761b-103">CSourceStream. OnThreadDestroy, método</span><span class="sxs-lookup"><span data-stu-id="a761b-103">CSourceStream.OnThreadDestroy method</span></span>

<span data-ttu-id="a761b-104">`OnThreadDestroy`Se llama al método cuando el subproceso de streaming está a punto de salir.</span><span class="sxs-lookup"><span data-stu-id="a761b-104">The `OnThreadDestroy` method is called when the streaming thread is about to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="a761b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a761b-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a><span data-ttu-id="a761b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a761b-106">Parameters</span></span>

<span data-ttu-id="a761b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a761b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a761b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a761b-108">Return value</span></span>

<span data-ttu-id="a761b-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a761b-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a761b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a761b-110">Remarks</span></span>

<span data-ttu-id="a761b-111">El procedimiento de subproceso, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), llama a este método antes de salir.</span><span class="sxs-lookup"><span data-stu-id="a761b-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method before it exits.</span></span> <span data-ttu-id="a761b-112">El método no hace nada en la clase base; está disponible para que la clase derivada se invalide.</span><span class="sxs-lookup"><span data-stu-id="a761b-112">The method does nothing in the base class; it is available for the derived class to override.</span></span> <span data-ttu-id="a761b-113">Si la clase derivada devuelve un código de error, el subproceso se cierra con un error.</span><span class="sxs-lookup"><span data-stu-id="a761b-113">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a761b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a761b-114">Requirements</span></span>



| <span data-ttu-id="a761b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a761b-115">Requirement</span></span> | <span data-ttu-id="a761b-116">Value</span><span class="sxs-lookup"><span data-stu-id="a761b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a761b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a761b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a761b-118"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a761b-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a761b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a761b-119">Library</span></span><br/> | <dl> <span data-ttu-id="a761b-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a761b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a761b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a761b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a761b-122">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="a761b-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




