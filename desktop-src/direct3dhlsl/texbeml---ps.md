---
title: texbeml - ps
description: Aplicar una transformación de mapa de entorno de protuberancia falsa con corrección de luminosidad. Esto se logra mediante la modificación de los datos de dirección de textura del registro de destino, mediante datos de alteración de direcciones (du,dv), una matriz de entorno de protuberancia 2D y luminosidad.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966447"
---
# <a name="texbeml---ps"></a>texbeml - ps

Aplicar una transformación de mapa de entorno de protuberancia falsa con corrección de luminosidad. Esto se logra mediante la modificación de los datos de dirección de textura del registro de destino, mediante datos de alteración de direcciones (du,dv), una matriz de entorno de protuberancia 2D y luminosidad.

## <a name="syntax"></a>Sintaxis



| texbeml dst, src |
|------------------|



 

, donde

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

Los datos de color rojo y verde del registro src se interpretan como los datos de alteración (du,dv). Los datos de color azul del registro src se interpretan como datos de luminosidad.

Esta instrucción transforma los componentes rojo y verde en el registro de origen mediante la matriz de asignación de entorno de protuberancia 2D. El resultado se agrega al conjunto de coordenadas de textura correspondiente al número de registro de destino. Se aplica una corrección de luminosidad mediante el valor de luminosidad y los valores de fase de textura de sesgo. El resultado se usa para muestrear la fase de textura actual.

Esto se puede usar para diversas técnicas basadas en la alteración de direcciones, como la asignación de entornos falsos por píxel.

Esta operación siempre interpreta du y dv como cantidades firmadas. Para las versiones 1 0 y 1 1, el modificador de entrada \_ Source Register Signed \_ [Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) \_ (bx2) no se permite en el argumento de entrada.

Esta instrucción genera resultados definidos cuando las texturas de entrada contienen datos de formato mixto. Para obtener más información sobre los formatos de superficie, [vea D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



En este ejemplo se muestran los cálculos que se realizan dentro de la instrucción .


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u' = TextureCoordinates(stage m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00(stage m) \* t(n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10(stage m) \* t(n)<sub>G</sub>

v' = TextureCoordinates(stage m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01(stage m) \* t(n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11(stage m) \* t(n)<sub>G</sub>

t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates

t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub>\*

\[(t(n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE(stage m)) +

D3DTSS \_ BUMPENVLOFFSET(stage m)\]

Los datos de registro leídos por una instrucción [de tipo "texbem"](texbem---ps.md) o "texbeml" no se pueden leer más adelante, excepto por otro tipo de archivo.


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a>Ejemplos

Este es un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Este ejemplo requiere las siguientes texturas en las siguientes fases de textura.

-   A la fase 0 se le asigna un mapa de protuberancias con datos de alteración (du, dv).
-   A la fase 1 se le asigna un mapa de textura con datos de color.
-   establece los datos de la matriz en la fase de textura muestreada. Esto es diferente de la funcionalidad de la canalización de función fija donde los datos de la alteración y las matrices ocupan la misma fase de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 