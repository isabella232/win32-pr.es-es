---
description: Habilita o deshabilita el registro de depuración de una sección crítica determinada.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Función DbgLockTrace (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660501"
---
# <a name="dbglocktrace-function"></a><span data-ttu-id="8bb5a-103">DbgLockTrace función)</span><span class="sxs-lookup"><span data-stu-id="8bb5a-103">DbgLockTrace function</span></span>

<span data-ttu-id="8bb5a-104">Habilita o deshabilita el registro de depuración de una sección crítica determinada.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-104">Enables or disables debug logging of a given critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb5a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bb5a-105">Syntax</span></span>


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a><span data-ttu-id="8bb5a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bb5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb5a-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="8bb5a-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="8bb5a-108">Puntero a una sección crítica de [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="8bb5a-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> <dt>

<span data-ttu-id="8bb5a-109">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="8bb5a-109">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="8bb5a-110">Valor que especifica si el registro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-110">Value specifying whether logging is enabled.</span></span> <span data-ttu-id="8bb5a-111">Use **true** para habilitar el registro o **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-111">Use **TRUE** to enable logging or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb5a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bb5a-112">Return value</span></span>

<span data-ttu-id="8bb5a-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb5a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bb5a-114">Remarks</span></span>

<span data-ttu-id="8bb5a-115">Utilice esta función para realizar un seguimiento de una sección crítica específica.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-115">Use this function to trace a specific critical section.</span></span> <span data-ttu-id="8bb5a-116">De forma predeterminada, el registro de depuración de secciones críticas está deshabilitado debido al gran número de secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-116">By default, debug logging of critical sections is disabled, because of the large number of critical sections.</span></span>

<span data-ttu-id="8bb5a-117">Para realizar un seguimiento de una sección crítica, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8bb5a-117">To trace a critical section, perform the following steps:</span></span>

1.  <span data-ttu-id="8bb5a-118">Defina depurar o \_ depurar antes de incluir los encabezados de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-118">Define DEBUG or \_DEBUG before you include the DirectShow headers.</span></span>
2.  <span data-ttu-id="8bb5a-119">Habilite el registro de depuración para las secciones críticas llamando a [**DbgSetModuleLevel**](dbgsetmodulelevel.md) con la marca de bloqueo del registro \_ .</span><span class="sxs-lookup"><span data-stu-id="8bb5a-119">Enable debug logging for critical sections, by calling [**DbgSetModuleLevel**](dbgsetmodulelevel.md) with the LOG\_LOCKING flag.</span></span>
3.  <span data-ttu-id="8bb5a-120">Llame a **DbgLockTrace** en la sección crítica en la que desea realizar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-120">Call **DbgLockTrace** on the critical section you want to trace.</span></span>

<span data-ttu-id="8bb5a-121">En las compilaciones comerciales, la función **DbgLockTrace** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-121">In retail builds, the **DbgLockTrace** function has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="8bb5a-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8bb5a-122">Examples</span></span>

<span data-ttu-id="8bb5a-123">En el ejemplo de código siguiente se muestra cómo realizar un seguimiento de una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="8bb5a-123">The following code example shows how to trace a critical section.</span></span>


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a><span data-ttu-id="8bb5a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bb5a-124">Requirements</span></span>



| <span data-ttu-id="8bb5a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb5a-125">Requirement</span></span> | <span data-ttu-id="8bb5a-126">Value</span><span class="sxs-lookup"><span data-stu-id="8bb5a-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb5a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bb5a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8bb5a-128"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8bb5a-128"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8bb5a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bb5a-129">Library</span></span><br/> | <dl> <span data-ttu-id="8bb5a-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8bb5a-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb5a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bb5a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb5a-132">Funciones de depuración de sección crítica</span><span class="sxs-lookup"><span data-stu-id="8bb5a-132">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




