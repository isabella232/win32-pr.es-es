---
description: Espera a que se señale un objeto.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Función DbgWaitForSingleObject (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681160"
---
# <a name="dbgwaitforsingleobject-function"></a><span data-ttu-id="dd88c-103">DbgWaitForSingleObject función)</span><span class="sxs-lookup"><span data-stu-id="dd88c-103">DbgWaitForSingleObject function</span></span>

<span data-ttu-id="dd88c-104">Espera a que se señale un objeto.</span><span class="sxs-lookup"><span data-stu-id="dd88c-104">Waits for an object to become signaled.</span></span>

<span data-ttu-id="dd88c-105">En una compilación de depuración, esta función desencadena una aserción si el intervalo de tiempo de espera expira antes de que se Señalice el objeto.</span><span class="sxs-lookup"><span data-stu-id="dd88c-105">In a debug build, this function triggers an assert if the time-out interval expires before the object is signaled.</span></span> <span data-ttu-id="dd88c-106">Para establecer el intervalo de tiempo de espera, llame a la función [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="dd88c-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="dd88c-107">En una compilación comercial, esta función es equivalente a la función **WaitForSingleObject** con un intervalo de tiempo de espera infinito.</span><span class="sxs-lookup"><span data-stu-id="dd88c-107">In a retail build, this function is equivalent to the **WaitForSingleObject** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd88c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd88c-108">Syntax</span></span>


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a><span data-ttu-id="dd88c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd88c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd88c-110">*h*</span><span class="sxs-lookup"><span data-stu-id="dd88c-110">*h*</span></span> 
</dt> <dd>

<span data-ttu-id="dd88c-111">Identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="dd88c-111">Handle to the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd88c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd88c-112">Requirements</span></span>



| <span data-ttu-id="dd88c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd88c-113">Requirement</span></span> | <span data-ttu-id="dd88c-114">Value</span><span class="sxs-lookup"><span data-stu-id="dd88c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd88c-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd88c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="dd88c-116"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd88c-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd88c-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd88c-117">Library</span></span><br/> | <dl> <span data-ttu-id="dd88c-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dd88c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd88c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd88c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd88c-120">Funciones de depuración de espera</span><span class="sxs-lookup"><span data-stu-id="dd88c-120">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




