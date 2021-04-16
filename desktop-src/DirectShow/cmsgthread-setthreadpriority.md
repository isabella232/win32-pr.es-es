---
description: Usa la función SetThreadPriority de Microsoft Win32 para establecer la prioridad del subproceso en un nuevo valor.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Método CMsgThread. SetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671726"
---
# <a name="cmsgthreadsetthreadpriority-method"></a><span data-ttu-id="a5a89-103">CMsgThread. SetThreadPriority, método</span><span class="sxs-lookup"><span data-stu-id="a5a89-103">CMsgThread.SetThreadPriority method</span></span>

<span data-ttu-id="a5a89-104">Usa la función **SetThreadPriority** de Microsoft Win32 para establecer la prioridad del subproceso en un nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="a5a89-104">Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5a89-105">Syntax</span></span>


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a><span data-ttu-id="a5a89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5a89-107">*nPriority*</span><span class="sxs-lookup"><span data-stu-id="a5a89-107">*nPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="a5a89-108">Prioridad del subproceso.</span><span class="sxs-lookup"><span data-stu-id="a5a89-108">Priority of the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5a89-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5a89-109">Return value</span></span>

<span data-ttu-id="a5a89-110">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a5a89-110">Returns one of the following values.</span></span>



| <span data-ttu-id="a5a89-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a5a89-111">Return code</span></span>                                                                              | <span data-ttu-id="a5a89-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5a89-112">Description</span></span>                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a5a89-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a5a89-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="a5a89-114">La prioridad se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5a89-114">Priority was successfully set.</span></span><br/> |
| <dl> <span data-ttu-id="a5a89-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a5a89-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a5a89-116">No se estableció la prioridad.</span><span class="sxs-lookup"><span data-stu-id="a5a89-116">Priority was not set.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="a5a89-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5a89-117">Remarks</span></span>

<span data-ttu-id="a5a89-118">El cliente y el subproceso de trabajo pueden llamar a esta función miembro.</span><span class="sxs-lookup"><span data-stu-id="a5a89-118">The client and the worker thread can call this member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a89-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5a89-119">Requirements</span></span>



| <span data-ttu-id="a5a89-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a89-120">Requirement</span></span> | <span data-ttu-id="a5a89-121">Value</span><span class="sxs-lookup"><span data-stu-id="a5a89-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a89-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5a89-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a5a89-123"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5a89-123"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5a89-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5a89-124">Library</span></span><br/> | <dl> <span data-ttu-id="a5a89-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a5a89-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5a89-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5a89-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a89-127">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="a5a89-127">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




