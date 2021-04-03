---
title: Tipos simples
description: Todos los tipos simples se representan mediante un carácter de formato único que indica el tipo por su nombre.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe123ca7c06a0522a139dc0cca8a9e24d1d585d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778282"
---
# <a name="simple-types"></a><span data-ttu-id="4618a-103">Tipos simples</span><span class="sxs-lookup"><span data-stu-id="4618a-103">Simple Types</span></span>

<span data-ttu-id="4618a-104">Todos los tipos simples se representan mediante un carácter de formato único que indica el tipo por su nombre.</span><span class="sxs-lookup"><span data-stu-id="4618a-104">All simple types are represented by a single format character indicating the type by its name.</span></span> <span data-ttu-id="4618a-105">Esto incluye todos los tipos numéricos y otros tipos de IDL especiales.</span><span class="sxs-lookup"><span data-stu-id="4618a-105">This includes all the numerical types and some other special IDL types.</span></span> <span data-ttu-id="4618a-106">La lista es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="4618a-106">The list is as follows:</span></span>

``` syntax
FC_BYTE,                    // 0x01
FC_CHAR,                    // 0x02
FC_SMALL,                   // 0x03
FC_USMALL,                  // 0x04
FC_WCHAR,                   // 0x05
FC_SHORT,                   // 0x06
FC_USHORT,                  // 0x07
FC_LONG,                    // 0x08
FC_ULONG,                   // 0x09
FC_FLOAT,                   // 0x0a
FC_HYPER,                   // 0x0b
FC_DOUBLE,                  // 0x0c
FC_ENUM16,                  // 0x0d
FC_ENUM32,                  // 0x0e
FC_ERROR_STATUS_T,          // 0x10
FC_INT3264,                 // 0xb8
FC_UINT3264,                // 0xb9
```

<span data-ttu-id="4618a-107">Los tipos pequeños, WCHAR, HYPER, \_ status \_ T, \_ \_ INT3264 son intrínsecos de MIDL con interpretaciones RPC especiales.</span><span class="sxs-lookup"><span data-stu-id="4618a-107">The SMALL, WCHAR, HYPER, ERROR\_STATUS\_T, \_\_INT3264 types are MIDL intrinsics with special RPC interpretations.</span></span> <span data-ttu-id="4618a-108">Los tipos INT e \_ \_ Int32 se asignan a las asignaciones Long, unsigned \_ int y Unsigned \_ \_ INT32 a FC \_ ULong, \_ \_ INT64 y Unsigned \_ \_ INT64 se asignan a FC \_ Hyper.</span><span class="sxs-lookup"><span data-stu-id="4618a-108">The INT and \_\_INT32 types map to FC\_LONG, unsigned INT and unsigned \_\_INT32 map to FC\_ULONG, \_\_INT64 and unsigned \_\_INT64 map to FC\_HYPER.</span></span>

<span data-ttu-id="4618a-109">\_ \_ No se admiten los tipos INT128, FLOAT128 y FLOAT80.</span><span class="sxs-lookup"><span data-stu-id="4618a-109">The \_\_INT128, FLOAT128, and FLOAT80 types are not supported.</span></span>

 

 




