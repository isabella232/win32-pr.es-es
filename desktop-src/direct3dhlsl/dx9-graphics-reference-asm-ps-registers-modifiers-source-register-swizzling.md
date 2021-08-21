---
title: Swling del registro de origen (referencia de HLSL PS)
description: Swling hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. El desdobado no afecta a los datos de registro de origen. Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c0357a902c793165149da5c853ac953cf5989f8a472fe936c6c2b95cb9e3197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090118"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Swling del registro de origen (referencia de HLSL PS)

Swling hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. El desdobado no afecta a los datos de registro de origen. Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal.

## <a name="source-swizzling"></a>Swling de origen

El swzzle de origen permite que un componente individual de un registro de origen tome el valor de cualquiera de los cuatro componentes del mismo registro de origen antes de leer el registro para el cálculo.

Por ejemplo, el swzzle .zxxy significa:

-   El componente .x asumirá el valor del componente .z.
-   El componente .y asumirá el valor del componente .x.
-   El componente .z asumirá el valor del componente .x.
-   El componente .w asumirá el valor del componente .y

Los componentes pueden aparecer en cualquier orden. Si se especifican menos de cuatro componentes, se repite el último componente. Por ejemplo:


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Si no se especifica ningún componente, no se aplica ningún desdobado.

Algunas instrucciones tienen restricciones para el swzzle de origen. Se enumeran en las páginas de referencia de instrucciones respetadas.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| .y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| .z                    | X\*  | X\*  | X\*  | x    | x    | x    | x     | x    | x     |
| .w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .xyzw (valor predeterminado)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .wzyx                 |      |      |      |      | x    | x    | x     | x    | x     |
| sw swzzle arbitrario     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Solo está disponible si la máscara de escritura de destino es .w (.a).

## <a name="arbitrary-swizzle"></a>Swzzle arbitrario

Se pueden aplicar swzzles a los registros de origen en un orden arbitrario; Es decir, cualquier registro de origen puede tomar cualquier máscara de componente, en cualquier orden.

## <a name="replicate-swizzle"></a>Replicación de Swzzle

Replicar swzzle copia un componente en otro. Es decir, debe especificarse exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 Registros](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x Registros](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 Registros](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




