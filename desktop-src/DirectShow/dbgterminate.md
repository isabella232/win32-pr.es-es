---
description: La función DbgTerminate limpia la biblioteca de depuración. Se omite en las compilaciones comerciales.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Función DbgTerminate (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679359"
---
# <a name="dbgterminate-function"></a><span data-ttu-id="3d823-104">DbgTerminate función)</span><span class="sxs-lookup"><span data-stu-id="3d823-104">DbgTerminate function</span></span>

<span data-ttu-id="3d823-105">La función **DbgTerminate** limpia la biblioteca de depuración.</span><span class="sxs-lookup"><span data-stu-id="3d823-105">The **DbgTerminate** function cleans up the debug library.</span></span> <span data-ttu-id="3d823-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="3d823-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d823-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d823-107">Syntax</span></span>


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a><span data-ttu-id="3d823-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d823-108">Parameters</span></span>

<span data-ttu-id="3d823-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3d823-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d823-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d823-110">Return value</span></span>

<span data-ttu-id="3d823-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3d823-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d823-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d823-112">Remarks</span></span>

<span data-ttu-id="3d823-113">Llame a esta función si llama a la función [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="3d823-113">Call this function if you call the [**DbgInitialise**](dbginitialise.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d823-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d823-114">Requirements</span></span>



| <span data-ttu-id="3d823-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d823-115">Requirement</span></span> | <span data-ttu-id="3d823-116">Value</span><span class="sxs-lookup"><span data-stu-id="3d823-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d823-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d823-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3d823-118"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d823-118"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d823-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d823-119">Library</span></span><br/> | <dl> <span data-ttu-id="3d823-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3d823-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d823-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d823-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d823-122">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="3d823-122">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




