---
description: Establece el valor de tiempo de espera de depuración. Se omite en las compilaciones comerciales.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Función DbgSetWaitTimeout (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660404"
---
# <a name="dbgsetwaittimeout-function"></a><span data-ttu-id="68278-104">DbgSetWaitTimeout función)</span><span class="sxs-lookup"><span data-stu-id="68278-104">DbgSetWaitTimeout function</span></span>

<span data-ttu-id="68278-105">Establece el valor de tiempo de espera de depuración.</span><span class="sxs-lookup"><span data-stu-id="68278-105">Sets the debugging time-out value.</span></span> <span data-ttu-id="68278-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="68278-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="68278-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68278-107">Syntax</span></span>


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="68278-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68278-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68278-109">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="68278-109">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="68278-110">Valor de tiempo de espera en milisegundos o infinito para esperar indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="68278-110">Time-out value in milliseconds, or INFINITE to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68278-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68278-111">Return value</span></span>

<span data-ttu-id="68278-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="68278-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68278-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68278-113">Remarks</span></span>

<span data-ttu-id="68278-114">En las compilaciones de depuración, las funciones [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) y [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) usan este valor como el intervalo de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="68278-114">In debug builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions use this value as the time-out interval.</span></span>

## <a name="requirements"></a><span data-ttu-id="68278-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68278-115">Requirements</span></span>



| <span data-ttu-id="68278-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="68278-116">Requirement</span></span> | <span data-ttu-id="68278-117">Value</span><span class="sxs-lookup"><span data-stu-id="68278-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68278-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68278-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68278-119"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68278-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="68278-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68278-120">Library</span></span><br/> | <dl> <span data-ttu-id="68278-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="68278-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68278-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="68278-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68278-123">Funciones de depuración de espera</span><span class="sxs-lookup"><span data-stu-id="68278-123">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




