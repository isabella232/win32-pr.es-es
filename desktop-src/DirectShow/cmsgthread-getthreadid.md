---
description: Recupera el identificador del subproceso.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Método CMsgThread. GetThreadID (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670987"
---
# <a name="cmsgthreadgetthreadid-method"></a><span data-ttu-id="8c989-103">CMsgThread. GetThreadID, método</span><span class="sxs-lookup"><span data-stu-id="8c989-103">CMsgThread.GetThreadID method</span></span>

<span data-ttu-id="8c989-104">Recupera el identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="8c989-104">Retrieves the thread's identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c989-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c989-105">Syntax</span></span>


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a><span data-ttu-id="8c989-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c989-106">Parameters</span></span>

<span data-ttu-id="8c989-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c989-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c989-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c989-108">Return value</span></span>

<span data-ttu-id="8c989-109">Devuelve el miembro de datos privado del **\_ ThreadId de m** .</span><span class="sxs-lookup"><span data-stu-id="8c989-109">Returns the **m\_ThreadId** private data member.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c989-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c989-110">Remarks</span></span>

<span data-ttu-id="8c989-111">Esta función devuelve el identificador de Microsoft Win32 para el subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="8c989-111">This function returns the Microsoft Win32 identifier for the worker thread.</span></span> <span data-ttu-id="8c989-112">Puede llamar a esta función miembro en el subproceso de trabajo o en un subproceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8c989-112">You can call this member function on either the worker thread or a client thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c989-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c989-113">Requirements</span></span>



| <span data-ttu-id="8c989-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c989-114">Requirement</span></span> | <span data-ttu-id="8c989-115">Value</span><span class="sxs-lookup"><span data-stu-id="8c989-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c989-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c989-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8c989-117"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c989-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c989-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c989-118">Library</span></span><br/> | <dl> <span data-ttu-id="8c989-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8c989-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c989-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c989-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c989-121">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="8c989-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




