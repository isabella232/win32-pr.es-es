---
title: Máscara de escritura de registro de destino
description: Una máscara de escritura controla qué componentes de un registro de destino se escriben una vez completada una instrucción.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994597"
---
# <a name="destination-register-write-mask"></a>Máscara de escritura de registro de destino

Una máscara de escritura controla qué componentes de un registro de destino se escriben una vez completada una instrucción. Se permite una máscara de escritura de salida siempre que los componentes estén en el orden de. RGBA o. xyzw. Es decir,. RBA y. XW son máscaras válidas. Los registros de textura tienen un conjunto de reglas y los registros que no son de textura tienen otro conjunto de reglas.

## <a name="syntax"></a>Sintaxis



| DST. writemask |
|---------------|



 

, donde

-   DST es un registro de destino.
-   writemask es una secuencia de máscaras de cualquier conjunto: (x, y, z, w) o (rojo, verde, azul, alfa).

## <a name="remarks"></a>Observaciones

Están disponibles las siguientes máscaras de escritura de destino.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| . xyzw (valor predeterminado)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . XYZ                  | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| máscara arbitraria        |      |      |      | x    | x    | x    | x     | x    | x     |



 

La máscara arbitraria permite combinar cualquier conjunto de canales para generar una máscara. Los canales deben aparecer en el orden r, g, b, a-por ejemplo, Register. RBA, que actualiza los canales rojo, azul y alfa del destino. La máscara arbitraria está disponible en la versión 1 \_ 4 o superior.

Si no se especifica ninguna máscara de escritura de destino, el valor predeterminado de la máscara de escritura de destino es el caso RGBA. Es decir, se actualizan todos los canales del registro de destino.

En las versiones 1 \_ a 1 \_ 3, la instrucción aritmética [DP3-PS](dp3---ps.md) DP3 solo puede usar las máscaras de escritura de salida. RGB o. RGBA.

Las máscaras de escritura del registro de destino solo se admiten para las operaciones aritméticas. No se pueden usar en instrucciones de direccionamiento de textura, con la excepción de las instrucciones de la versión 1 \_ , [texcrd-PS](texcrd---ps.md) y [texld-PS \_ 2 \_ y versiones up](texld---ps-2-0.md).

El valor predeterminado es escribir los cuatro canales de color.


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



También se hace referencia a la máscara de escritura alfa como máscara de escritura escalar, ya que utiliza la canalización escalar.


```
add r0.a, t1, v1
```



Por lo tanto, esta instrucción coloca eficazmente la suma del componente alfa de T1 y el componente alfa de V1 en R0. a.

La máscara de escritura de color se utiliza para controlar la escritura en los canales de color.


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



\_En el caso de la versión 4, las máscaras de escritura de destino se pueden usar en cualquier combinación siempre que las máscaras se ordenen como r, g, b, a.


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



Una instrucción de emisión conjunta permite que dos instrucciones potencialmente diferentes se emitan simultáneamente. Esto se consigue mediante la ejecución de las instrucciones de la canalización alfa y la canalización RGB.


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



La ventaja de las instrucciones de emparejamiento de este modo es que permite realizar diferentes operaciones en el vector y en la canalización escalar en paralelo.

Estos registros de salida del sombreador de vértices están restringidos a las siguientes máscaras de escritura:



| Tipo de registro | Máscara de escritura necesaria                                              |
|---------------|------------------------------------------------------------------|
| oFog          | no se permite ninguna máscara de escritura explícita en este registro escalar        |
| Aporta          | no se permite ninguna máscara de escritura explícita en este registro escalar        |
| oPos          | . xyzw (que es el valor predeterminado)                                      |
| OTR\#          | máscara combinada:. x \| . XY \| . XYZ \| . xyzw (que es el valor predeterminado) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




