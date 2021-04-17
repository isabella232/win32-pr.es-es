---
description: El método Create crea el subproceso.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Método CAMThread. Create (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690676"
---
# <a name="camthreadcreate-method"></a><span data-ttu-id="98826-103">CAMThread. Create (método)</span><span class="sxs-lookup"><span data-stu-id="98826-103">CAMThread.Create method</span></span>

<span data-ttu-id="98826-104">El `Create` método crea el subproceso.</span><span class="sxs-lookup"><span data-stu-id="98826-104">The `Create` method creates the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="98826-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98826-105">Syntax</span></span>


```C++
BOOL Create();
```



## <a name="parameters"></a><span data-ttu-id="98826-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98826-106">Parameters</span></span>

<span data-ttu-id="98826-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="98826-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98826-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98826-108">Return value</span></span>

<span data-ttu-id="98826-109">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="98826-109">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="98826-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98826-110">Remarks</span></span>

<span data-ttu-id="98826-111">Este método crea el subproceso con el método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) para el procedimiento de subproceso y `this` para el argumento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="98826-111">This method creates the thread, using the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method for the thread procedure and `this` for the thread argument.</span></span>

<span data-ttu-id="98826-112">El método genera un error si el subproceso ya existe.</span><span class="sxs-lookup"><span data-stu-id="98826-112">The method fails if the thread already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="98826-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98826-113">Requirements</span></span>



| <span data-ttu-id="98826-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98826-114">Requirement</span></span> | <span data-ttu-id="98826-115">Value</span><span class="sxs-lookup"><span data-stu-id="98826-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98826-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98826-116">Header</span></span><br/>  | <dl> <span data-ttu-id="98826-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98826-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="98826-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98826-118">Library</span></span><br/> | <dl> <span data-ttu-id="98826-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98826-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98826-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="98826-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98826-121">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="98826-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




