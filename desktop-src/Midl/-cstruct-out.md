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
# <a name="cstruct_out-switch"></a>/cstruct \_ conmutador de salida

Este modificador modifica la definición de C de una interfaz COM que devuelve estructuras para que coincidan con la ABI que proporcionaría un implementador de C++.

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Algunas definiciones de interfaz (en particular, las de `d3d12.idl` ) contienen `__stdcall` métodos que devuelven estructuras. El Abi de C y C++ de MSVC difiere en cómo implementan estas funciones:

* C los trata como funciones sin formato que toman un `this` puntero oculto como primer parámetro. El compilador aplica una pequeña optimización de estructura que permite la devolución de Structs de menos de 8 bytes (o mayor si todos los valores son de punto flotante) en los registros. Solo las estructuras de mayor tamaño se promocionan para utilizar un parámetro oculto y un valor devuelto asignado por el llamador.
* C++ los trata como funciones miembro. El compilador *siempre* lo hace insertando un parámetro oculto (un puntero a un valor devuelto asignado por el llamador) como segundo parámetro, después del `this` puntero. También devuelve el mismo puntero que el valor devuelto.

Este modificador fuerza a la definición de C de las interfaces en el encabezado resultante a suponer que el implementador estaba usando C++ y que en su lugar el código C debería usar explícitamente la ABI de C++. Esto implica que la función incluye un parámetro oculto para el puntero de valor devuelto y devuelve el puntero en lugar de la estructura directamente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>
