---
description: La función DbgDumpObjectRegister muestra información sobre los objetos activos. Se omite en las compilaciones comerciales.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Función DbgDumpObjectRegister (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660502"
---
# <a name="dbgdumpobjectregister-function"></a><span data-ttu-id="c93ad-104">DbgDumpObjectRegister función)</span><span class="sxs-lookup"><span data-stu-id="c93ad-104">DbgDumpObjectRegister function</span></span>

<span data-ttu-id="c93ad-105">La `DbgDumpObjectRegister` función muestra información sobre los objetos activos.</span><span class="sxs-lookup"><span data-stu-id="c93ad-105">The `DbgDumpObjectRegister` function displays information about active objects.</span></span> <span data-ttu-id="c93ad-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="c93ad-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93ad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c93ad-107">Syntax</span></span>


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a><span data-ttu-id="c93ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c93ad-108">Parameters</span></span>

<span data-ttu-id="c93ad-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c93ad-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c93ad-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c93ad-110">Return value</span></span>

<span data-ttu-id="c93ad-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c93ad-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93ad-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c93ad-112">Remarks</span></span>

<span data-ttu-id="c93ad-113">En las compilaciones de depuración, la biblioteca de depuración mantiene una lista de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="c93ad-113">In debug builds, the debug library maintains a list of active objects.</span></span> <span data-ttu-id="c93ad-114">La lista incluye todos los objetos que se derivan de [**CBaseObject**](cbaseobject.md), creados por el módulo actual y no se han destruido.</span><span class="sxs-lookup"><span data-stu-id="c93ad-114">The list includes any objects that derive from [**CBaseObject**](cbaseobject.md), were created by the current module, and have not been destroyed.</span></span> <span data-ttu-id="c93ad-115">Los métodos del constructor y el destructor de **CBaseObject** actualizan la lista.</span><span class="sxs-lookup"><span data-stu-id="c93ad-115">The **CBaseObject** constructor and destructor methods update the list.</span></span>

<span data-ttu-id="c93ad-116">Esta función genera varios mensajes de memoria de registro \_ .</span><span class="sxs-lookup"><span data-stu-id="c93ad-116">This function generates several LOG\_MEMORY messages.</span></span> <span data-ttu-id="c93ad-117">En el nivel de registro 1, la función muestra solo el número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="c93ad-117">At logging level 1, the function displays only the total number of objects.</span></span> <span data-ttu-id="c93ad-118">En el nivel de registro 2 o superior, se muestra una lista de los objetos.</span><span class="sxs-lookup"><span data-stu-id="c93ad-118">At logging level 2 or higher, it displays a list of the objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93ad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c93ad-119">Requirements</span></span>



| <span data-ttu-id="c93ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c93ad-120">Requirement</span></span> | <span data-ttu-id="c93ad-121">Value</span><span class="sxs-lookup"><span data-stu-id="c93ad-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93ad-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c93ad-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c93ad-123"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c93ad-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c93ad-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c93ad-124">Library</span></span><br/> | <dl> <span data-ttu-id="c93ad-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c93ad-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93ad-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c93ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93ad-127">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="c93ad-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




