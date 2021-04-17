---
description: La macro NOTE envía una cadena a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Nota (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690914"
---
# <a name="note"></a><span data-ttu-id="7a25f-104">NOTA</span><span class="sxs-lookup"><span data-stu-id="7a25f-104">NOTE</span></span>

<span data-ttu-id="7a25f-105">La `NOTE` macro envía una cadena a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="7a25f-105">The `NOTE` macro sends a string to the debug output location.</span></span> <span data-ttu-id="7a25f-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="7a25f-106">Ignored in retail builds.</span></span>

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a><span data-ttu-id="7a25f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a25f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a25f-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span><span class="sxs-lookup"><span data-stu-id="7a25f-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span></span>
</dt> <dd>

<span data-ttu-id="7a25f-109">Una cadena de formato de estilo printf.</span><span class="sxs-lookup"><span data-stu-id="7a25f-109">A printf -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="7a25f-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*:*arg5*</span><span class="sxs-lookup"><span data-stu-id="7a25f-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span></span>
</dt> <dd>

<span data-ttu-id="7a25f-111">Argumentos adicionales para la cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="7a25f-111">Additional arguments for the format string.</span></span> <span data-ttu-id="7a25f-112">El número de argumentos debe coincidir con el nombre de la macro.</span><span class="sxs-lookup"><span data-stu-id="7a25f-112">The number of arguments must match the macro name.</span></span> <span data-ttu-id="7a25f-113">Por ejemplo, **NOTE1** toma un argumento y **NOTE5** toma cinco argumentos.</span><span class="sxs-lookup"><span data-stu-id="7a25f-113">For example, **NOTE1** takes one argument, and **NOTE5** takes five arguments.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a25f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a25f-114">Remarks</span></span>

<span data-ttu-id="7a25f-115">Estas macros son variantes de la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="7a25f-115">These macros are variants of the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="7a25f-116">Generan mensajes de seguimiento de registro de nivel 5 \_ .</span><span class="sxs-lookup"><span data-stu-id="7a25f-116">They generate level 5 LOG\_TRACE messages.</span></span>

## <a name="example"></a><span data-ttu-id="7a25f-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a25f-117">Example</span></span>


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a><span data-ttu-id="7a25f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a25f-118">Requirements</span></span>



| <span data-ttu-id="7a25f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a25f-119">Requirement</span></span> | <span data-ttu-id="7a25f-120">Value</span><span class="sxs-lookup"><span data-stu-id="7a25f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a25f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a25f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7a25f-122"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a25f-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a25f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a25f-123">Library</span></span><br/> | <dl> <span data-ttu-id="7a25f-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7a25f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a25f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a25f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a25f-126">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="7a25f-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




