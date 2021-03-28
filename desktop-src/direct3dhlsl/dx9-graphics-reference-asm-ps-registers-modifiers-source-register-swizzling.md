---
title: Registro de origen permutación (referencia de PS de HLSL)
description: Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. Permutación no afecta a los datos de registro de origen. Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358524"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Registro de origen permutación (referencia de PS de HLSL)

Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. Permutación no afecta a los datos de registro de origen. Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal.

## <a name="source-swizzling"></a>Permutación de origen

El swizzle de origen permite que un componente individual de un registro de origen asuma el valor de cualquiera de los cuatro componentes del mismo registro de origen antes de que se lea el registro para el cálculo.

Por ejemplo,. zxxy swizzle significa:

-   el componente. x tomará el valor del componente. z
-   el componente. y tomará el valor del componente. x
-   el componente. z tomará el valor del componente. x
-   el componente. w tomará el valor del componente. y

Los componentes pueden aparecer en cualquier orden. Si se especifican menos de cuatro componentes, se repite el último componente. Por ejemplo:


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Si no se especifica ningún componente, no se aplica ningún permutación.

Algunas instrucciones tienen restricciones de swizzle de código fuente. Aparecen en las páginas de referencia de instrucciones respetadas.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . z                    | x1\*  | x1\*  | x1\*  | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . xyzw (valor predeterminado)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| . zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| . wzyx                 |      |      |      |      | x    | x    | x     | x    | x     |
| swizzle arbitrario     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Solo disponible si la máscara de escritura de destino es. w (. a).

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Swizzles se puede aplicar a los registros de origen en un orden arbitrario. es decir, cualquier registro de origen puede tomar cualquier máscara de componente, en cualquier orden.

## <a name="replicate-swizzle"></a>Replicar swizzle

Replicar swizzle copia un componente en otro. Es, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[Registros de PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[Registros de PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[Registros de PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




