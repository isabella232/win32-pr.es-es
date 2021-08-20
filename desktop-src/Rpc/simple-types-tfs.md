---
title: Tipos simples
description: Todos los tipos simples se representan mediante un carácter de formato único que indica el tipo por su nombre.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e265c24d1eaf4b85ab67c7f8997c656257522bfc8290e73596a8628bdd4215c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925165"
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

Los tipos SMALL, WCHAR, HYPER, ERROR \_ STATUS \_ T, \_ \_ INT3264 son intrínsecos MIDL con interpretaciones de RPC especiales. Los tipos INT e INT32 se asignan a FC LONG, INT sin signo e INT32 sin signo se asignan a \_ \_ \_ \_ \_ FC \_ ULONG, \_ \_ INT64 y \_ \_ INT64 \_ sin signo a FC HYPER.

No \_ \_ se admiten los tipos INT128, FLOAT128 y FLOAT80.

 

 




