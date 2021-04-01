---
title: modificador/cstruct_out
description: El modificador/cstruct_out modifica la definición de C de una interfaz COM que devuelve estructuras para que coincidan con la ABI que proporcionaría un implementador de C++.
keywords:
- /cstruct_out modificador MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905711"
---
# <a name="cstruct_out-switch"></a><span data-ttu-id="b3545-104">/cstruct \_ conmutador de salida</span><span class="sxs-lookup"><span data-stu-id="b3545-104">/cstruct\_out switch</span></span>

<span data-ttu-id="b3545-105">Este modificador modifica la definición de C de una interfaz COM que devuelve estructuras para que coincidan con la ABI que proporcionaría un implementador de C++.</span><span class="sxs-lookup"><span data-stu-id="b3545-105">This switch modifies the C definition of a COM interface which returns structures to match the ABI a C++ implementer would provide.</span></span>

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a><span data-ttu-id="b3545-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="b3545-106">Switch Options</span></span>

<span data-ttu-id="b3545-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b3545-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3545-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3545-108">Remarks</span></span>

<span data-ttu-id="b3545-109">Algunas definiciones de interfaz (en particular, las de `d3d12.idl` ) contienen `__stdcall` métodos que devuelven estructuras.</span><span class="sxs-lookup"><span data-stu-id="b3545-109">Some interface definitions (notably those in `d3d12.idl`) contain `__stdcall` methods that return structures.</span></span> <span data-ttu-id="b3545-110">El Abi de C y C++ de MSVC difiere en cómo implementan estas funciones:</span><span class="sxs-lookup"><span data-stu-id="b3545-110">The C and C++ ABIs from MSVC differ in how they implement such functions:</span></span>

* <span data-ttu-id="b3545-111">C los trata como funciones sin formato que toman un `this` puntero oculto como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="b3545-111">C treats them as plain functions that take a hidden `this` pointer as the first parameter.</span></span> <span data-ttu-id="b3545-112">El compilador aplica una pequeña optimización de estructura que permite la devolución de Structs de menos de 8 bytes (o mayor si todos los valores son de punto flotante) en los registros.</span><span class="sxs-lookup"><span data-stu-id="b3545-112">The complier applies a small struct optimization that allows structs smaller than 8 bytes (or larger if all values are floating point) to be returned in registers.</span></span> <span data-ttu-id="b3545-113">Solo las estructuras de mayor tamaño se promocionan para utilizar un parámetro oculto y un valor devuelto asignado por el llamador.</span><span class="sxs-lookup"><span data-stu-id="b3545-113">Only larger structures are promoted to use a hidden parameter and caller-allocated return value.</span></span>
* <span data-ttu-id="b3545-114">C++ los trata como funciones miembro.</span><span class="sxs-lookup"><span data-stu-id="b3545-114">C++ treats them as member functions.</span></span> <span data-ttu-id="b3545-115">El compilador *siempre* lo hace insertando un parámetro oculto (un puntero a un valor devuelto asignado por el llamador) como segundo parámetro, después del `this` puntero.</span><span class="sxs-lookup"><span data-stu-id="b3545-115">The compiler *always* does so by inserting a hidden parameter (a pointer to a caller-allocated return value) as the second parameter, after the `this` pointer.</span></span> <span data-ttu-id="b3545-116">También devuelve el mismo puntero que el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="b3545-116">It also returns that same pointer as its return value.</span></span>

<span data-ttu-id="b3545-117">Este modificador fuerza a la definición de C de las interfaces en el encabezado resultante a suponer que el implementador estaba usando C++ y que en su lugar el código C debería usar explícitamente la ABI de C++.</span><span class="sxs-lookup"><span data-stu-id="b3545-117">This switch forces the C definition of interfaces in the resulting header to assume that the implementer was using C++, and that the C code should instead explicitly use the C++ ABI.</span></span> <span data-ttu-id="b3545-118">Esto implica que la función incluye un parámetro oculto para el puntero de valor devuelto y devuelve el puntero en lugar de la estructura directamente.</span><span class="sxs-lookup"><span data-stu-id="b3545-118">This implies that the function includes a hidden parameter for the return value pointer and returns that pointer instead of the structure directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3545-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3545-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3545-120">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="b3545-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>
