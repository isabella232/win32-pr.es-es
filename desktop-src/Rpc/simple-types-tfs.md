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
# <a name="simple-types"></a>Tipos simples

Todos los tipos simples se representan mediante un carácter de formato único que indica el tipo por su nombre. Esto incluye todos los tipos numéricos y otros tipos de IDL especiales. La lista es la siguiente:

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

Los tipos pequeños, WCHAR, HYPER, \_ status \_ T, \_ \_ INT3264 son intrínsecos de MIDL con interpretaciones RPC especiales. Los tipos INT e \_ \_ Int32 se asignan a las asignaciones Long, unsigned \_ int y Unsigned \_ \_ INT32 a FC \_ ULong, \_ \_ INT64 y Unsigned \_ \_ INT64 se asignan a FC \_ Hyper.

\_ \_ No se admiten los tipos INT128, FLOAT128 y FLOAT80.

 

 




