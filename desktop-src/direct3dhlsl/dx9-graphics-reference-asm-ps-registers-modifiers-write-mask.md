---
title: Máscara de escritura del registro de destino
description: Una máscara de escritura controla qué componentes de un registro de destino se escriben una vez completada una instrucción.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 754bca59a16ef43bec477c12fcf9ffd1ebaf64f5f0fa46e7db95a80b2e96cea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908448"
---
# <a name="destination-register-write-mask"></a>Máscara de escritura del registro de destino

Una máscara de escritura controla qué componentes de un registro de destino se escriben una vez completada una instrucción. Se permite una máscara de escritura de salida siempre que los componentes estén en el orden de .rgba o .xyzw. Es decir, .rba y .xw son máscaras válidas. Los registros de textura tienen un conjunto de reglas y los registros que no son de textura tienen otro conjunto de reglas.

## <a name="syntax"></a>Syntax



| dst.writemask |
|---------------|



 

where

-   dst es un registro de destino.
-   writemask es una secuencia de máscaras de un conjunto: (x,y, z,w) o (rojo, verde, azul, alfa).

## <a name="remarks"></a>Comentarios

Están disponibles las siguientes máscaras de escritura de destino.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .xyzw (valor predeterminado)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .xyz                  | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| máscara arbitraria        |      |      |      | x    | x    | x    | x     | x    | x     |



 

La máscara arbitraria permite combinar cualquier conjunto de canales para generar una máscara. Los canales deben aparecer en el orden r, g, b, a ; por ejemplo, register.rba, que actualiza los canales rojo, azul y alfa del destino. La máscara arbitraria está disponible en la versión 1 \_ 4 o superior.

Si no se especifica ninguna máscara de escritura de destino, la máscara de escritura de destino tiene como valor predeterminado el caso rgba. En otras palabras, se actualizan todos los canales del registro de destino.

Para las versiones 1 0 a 1 3, la instrucción aritmética dp3 - ps dp3 solo puede usar las máscaras de escritura de salida \_ \_ .rgb o .rgba. [](dp3---ps.md)

Las máscaras de escritura del registro de destino solo se admiten para operaciones aritméticas. No se pueden usar en instrucciones de direccionamiento de textura, a excepción de las instrucciones de la versión \_ 1 4, [texcrd - ps](texcrd---ps.md) y [texld - ps \_ 2 \_ 0 y up](texld---ps-2-0.md).

El valor predeterminado es escribir los cuatro canales de color.


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



La máscara de escritura alfa también se conoce como máscara de escritura escalar, porque usa la canalización escalar.


```
add r0.a, t1, v1
```



Por lo tanto, esta instrucción coloca eficazmente la suma del componente alfa de t1 y el componente alfa de v1 en r0.a.

La máscara de escritura de color se usa para controlar la escritura en los canales de color.


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



Para la versión 1 4, las máscaras de escritura de destino se pueden usar en cualquier combinación, siempre y cuando las máscaras estén \_ ordenadas r,g,b,a.


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



Una instrucción emitida de forma simultánea permite emitir dos instrucciones potencialmente diferentes. Esto se logra mediante la ejecución de las instrucciones de la canalización alfa y la canalización RGB.


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



La ventaja de las instrucciones de emparejamiento de esta manera es que permite realizar diferentes operaciones en el vector y la canalización escalar en paralelo.

Estos registros de salida del sombreador de vértices están restringidos a las siguientes máscaras de escritura:



| Tipo de registro | Máscara de escritura requerida                                              |
|---------------|------------------------------------------------------------------|
| oFog          | No se permite ninguna máscara de escritura explícita en este registro escalar        |
| Opta          | No se permite ninguna máscara de escritura explícita en este registro escalar        |
| Opos          | .xyzw(que es el valor predeterminado)                                      |
| Ot\#          | combined mask: .x \| .xy \| .xyz \| .xyzw (que es el valor predeterminado) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




