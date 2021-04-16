---
description: La macro reminds genera un recordatorio en tiempo de compilación. Esta macro genera una cadena que incluye la cadena de parámetro, el nombre del archivo de código fuente y el número de línea.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: RECORDAR (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690460"
---
# <a name="remind"></a><span data-ttu-id="c093b-104">TE</span><span class="sxs-lookup"><span data-stu-id="c093b-104">REMIND</span></span>

<span data-ttu-id="c093b-105">La `REMIND` macro genera un recordatorio en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="c093b-105">The `REMIND` macro generates a reminder at compile time.</span></span> <span data-ttu-id="c093b-106">Esta macro genera una cadena que incluye la cadena de parámetro, el nombre del archivo de código fuente y el número de línea.</span><span class="sxs-lookup"><span data-stu-id="c093b-106">This macro generates a string that includes the parameter string, the name of the source file, and the line number.</span></span>

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="c093b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c093b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c093b-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="c093b-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="c093b-109">Cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="c093b-109">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c093b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c093b-110">Remarks</span></span>

<span data-ttu-id="c093b-111">Esta macro es útil para generar advertencias en tiempo de compilación:</span><span class="sxs-lookup"><span data-stu-id="c093b-111">This macro is useful for generating compile-time warnings:</span></span>


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a><span data-ttu-id="c093b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c093b-112">Requirements</span></span>



| <span data-ttu-id="c093b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c093b-113">Requirement</span></span> | <span data-ttu-id="c093b-114">Value</span><span class="sxs-lookup"><span data-stu-id="c093b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c093b-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c093b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c093b-116"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c093b-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c093b-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c093b-117">Library</span></span><br/> | <dl> <span data-ttu-id="c093b-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c093b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c093b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c093b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c093b-120">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="c093b-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




