---
title: Modificador /cstruct_out
description: El modificador /cstruct_out modifica la definición de C de una interfaz COM que devuelve estructuras para que coincidan con la ABI que proporcionaría un implementador de C++.
keywords:
- /cstruct_out switch MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 212f79eaad18ba49d12a49e9a831d2b2b5365a87cb9a36c558879adf76e8bb98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385820"
---
# <a name="cstruct_out-switch"></a>Modificador /cstruct \_ out

Este modificador modifica la definición de C de una interfaz COM que devuelve estructuras para que coincidan con la ABI que proporcionaría un implementador de C++.

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Algunas definiciones de interfaz (especialmente las de `d3d12.idl` ) contienen métodos `__stdcall` que devuelven estructuras. Las API de C y C++ MSVC difieren en la forma en que implementan estas funciones:

* C las trata como funciones sin formato que toman un `this` puntero oculto como primer parámetro. El cumplidor aplica una optimización de estructura pequeña que permite devolver structs de menos de 8 bytes (o más grandes si todos los valores son de punto flotante) en los registros. Solo se promueven estructuras más grandes para usar un parámetro oculto y un valor devuelto asignado por el autor de la llamada.
* C++ los trata como funciones miembro. El compilador *siempre lo* hace insertando un parámetro oculto (un puntero a un valor devuelto asignado por el autor de la llamada) como segundo parámetro, después del `this` puntero. También devuelve ese mismo puntero que su valor devuelto.

Este modificador obliga a la definición de C de interfaces en el encabezado resultante a asumir que el implementador usaba C++, y que el código de C debería usar explícitamente la ABI de C++. Esto implica que la función incluye un parámetro oculto para el puntero de valor devuelto y devuelve ese puntero en lugar de la estructura directamente.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>
