---
description: Devuelve TRUE si el subproceso actual es el propietario de la sección crítica especificada.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Función CritCheckIn (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660449"
---
# <a name="critcheckin-function"></a><span data-ttu-id="f4527-103">CritCheckIn función)</span><span class="sxs-lookup"><span data-stu-id="f4527-103">CritCheckIn function</span></span>

<span data-ttu-id="f4527-104">Devuelve **true** si el subproceso actual es el propietario de la sección crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="f4527-104">Returns **TRUE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4527-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4527-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="f4527-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4527-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="f4527-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="f4527-108">Puntero a una sección crítica de [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="f4527-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4527-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4527-109">Return value</span></span>

<span data-ttu-id="f4527-110">En las compilaciones de depuración, devuelve **true** si el subproceso actual es el propietario de esta sección crítica o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f4527-110">In debug builds, returns **TRUE** if the current thread is the owner of this critical section, or **FALSE** otherwise.</span></span> <span data-ttu-id="f4527-111">En las compilaciones comerciales, siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f4527-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4527-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4527-112">Remarks</span></span>

<span data-ttu-id="f4527-113">Esta función es especialmente útil dentro de la macro [**Assert**](assert.md) para comprobar si un subproceso es propietario de un bloqueo determinado.</span><span class="sxs-lookup"><span data-stu-id="f4527-113">This function is especially useful within the [**ASSERT**](assert.md) macro, to test whether a thread owns a given lock.</span></span>

## <a name="examples"></a><span data-ttu-id="f4527-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f4527-114">Examples</span></span>

<span data-ttu-id="f4527-115">En el ejemplo de código siguiente se muestra cómo usar esta función:</span><span class="sxs-lookup"><span data-stu-id="f4527-115">The following code example shows how to use this function:</span></span>


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a><span data-ttu-id="f4527-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4527-116">Requirements</span></span>



| <span data-ttu-id="f4527-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4527-117">Requirement</span></span> | <span data-ttu-id="f4527-118">Value</span><span class="sxs-lookup"><span data-stu-id="f4527-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4527-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4527-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f4527-120"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4527-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f4527-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4527-121">Library</span></span><br/> | <dl> <span data-ttu-id="f4527-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f4527-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4527-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4527-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4527-124">Funciones de depuración de sección crítica</span><span class="sxs-lookup"><span data-stu-id="f4527-124">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




