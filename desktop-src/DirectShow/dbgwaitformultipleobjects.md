---
description: Espera a que se señalen todos los objetos especificados (o todos).
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Función DbgWaitForMultipleObjects (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661309"
---
# <a name="dbgwaitformultipleobjects-function"></a><span data-ttu-id="e8cd5-103">DbgWaitForMultipleObjects función)</span><span class="sxs-lookup"><span data-stu-id="e8cd5-103">DbgWaitForMultipleObjects function</span></span>

<span data-ttu-id="e8cd5-104">Espera a que se señalen todos los objetos especificados (o todos).</span><span class="sxs-lookup"><span data-stu-id="e8cd5-104">Waits for any (or all) of the specified objects to be signaled.</span></span>

<span data-ttu-id="e8cd5-105">En una compilación de depuración, esta función desencadena una aserción si el intervalo de tiempo de espera expira antes de que se señalen los objetos.</span><span class="sxs-lookup"><span data-stu-id="e8cd5-105">In a debug build, this function triggers an assert if the time-out interval expires before the objects are signaled.</span></span> <span data-ttu-id="e8cd5-106">Para establecer el intervalo de tiempo de espera, llame a la función [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="e8cd5-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="e8cd5-107">En una compilación comercial, esta función es equivalente a la función **WaitForMultipleObjects** con un intervalo de tiempo de espera infinito.</span><span class="sxs-lookup"><span data-stu-id="e8cd5-107">In a retail build, this function is equivalent to the **WaitForMultipleObjects** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8cd5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8cd5-108">Syntax</span></span>


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a><span data-ttu-id="e8cd5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8cd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8cd5-110">*nCount*</span><span class="sxs-lookup"><span data-stu-id="e8cd5-110">*nCount*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cd5-111">Número de objetos.</span><span class="sxs-lookup"><span data-stu-id="e8cd5-111">Number of objects.</span></span>

</dd> <dt>

<span data-ttu-id="e8cd5-112">*lpHandles*</span><span class="sxs-lookup"><span data-stu-id="e8cd5-112">*lpHandles*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cd5-113">Matriz de identificadores de objetos, de tamaño *nCount*.</span><span class="sxs-lookup"><span data-stu-id="e8cd5-113">Array of handles to objects, of size *nCount*.</span></span>

</dd> <dt>

<span data-ttu-id="e8cd5-114">*bWaitAll*</span><span class="sxs-lookup"><span data-stu-id="e8cd5-114">*bWaitAll*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cd5-115">Valor booleano que especifica si se deben esperar todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="e8cd5-115">Boolean value that specifies whether to wait for all of the objects.</span></span> <span data-ttu-id="e8cd5-116">Si **es true**, la función espera a que se señalen todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="e8cd5-116">If **TRUE**, the function waits for all of the objects to be signaled.</span></span> <span data-ttu-id="e8cd5-117">De lo contrario, espera que se señalice al menos un objeto.</span><span class="sxs-lookup"><span data-stu-id="e8cd5-117">Otherwise, it waits for at least one object to be signaled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8cd5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8cd5-118">Requirements</span></span>



| <span data-ttu-id="e8cd5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8cd5-119">Requirement</span></span> | <span data-ttu-id="e8cd5-120">Value</span><span class="sxs-lookup"><span data-stu-id="e8cd5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8cd5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8cd5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e8cd5-122"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8cd5-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e8cd5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8cd5-123">Library</span></span><br/> | <dl> <span data-ttu-id="e8cd5-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e8cd5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8cd5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8cd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8cd5-126">Funciones de depuración de espera</span><span class="sxs-lookup"><span data-stu-id="e8cd5-126">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




