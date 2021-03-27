---
title: texbeml-PS
description: Aplicar una transformación de mapa de entorno de rugosidad falsa con corrección de luminancia. Esto se logra modificando los datos de la dirección de textura del registro de destino, utilizando los datos de la dirección Perturbation (du, DV), una matriz de entorno de rugosidad 2D y luminancia.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995580"
---
# <a name="texbeml---ps"></a>texbeml-PS

Aplicar una transformación de mapa de entorno de rugosidad falsa con corrección de luminancia. Esto se logra modificando los datos de la dirección de textura del registro de destino, utilizando los datos de la dirección Perturbation (du, DV), una matriz de entorno de rugosidad 2D y luminancia.

## <a name="syntax"></a>Sintaxis



| texbeml DST, src |
|------------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

Los datos de color rojo y verde del registro de src se interpretan como los datos de Perturbation (du, DV). Los datos de color azul del registro de src se interpretan como los datos de luminancia.

Esta instrucción transforma los componentes rojo y verde del registro de origen mediante la matriz de asignación del entorno de rugosidad 2D. El resultado se agrega al conjunto de coordenadas de textura correspondiente al número de registro de destino. Una corrección de luminancia se aplica mediante el valor de luminancia y los valores de la fase de textura de sesgo. El resultado se usa para muestrear la fase de textura actual.

Se puede usar para una variedad de técnicas basadas en la dirección Perturbation, como la asignación de entorno falsa por píxel.

Esta operación siempre interpreta du y DV como cantidades firmadas. En las versiones 1 \_ y 1 \_ 1, no se permite el modificador de entrada de [escala firmada del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) en el argumento de entrada.

Esta instrucción genera resultados definidos cuando las texturas de entrada contienen datos de formato mixto. Para obtener más información sobre los formatos de Surface, vea [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



Este ejemplo muestra los cálculos realizados dentro de la instrucción.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u ' = TextureCoordinates (fase m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00 (Stage m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10 (Stage m) \* t (n)<sub>G</sub>

v ' = TextureCoordinates (fase m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01 (Stage m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11 (Stage m) \* t (n)<sub>G</sub>

t (m)<sub>RGBA</sub> = TextureSample (fase m) mediante (u ', v ') como coordenadas

t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*

\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (fase m)) +

D3DTSS \_ BUMPENVLOFFSET (fase m)\]

Los datos de registro que ha leído una instrucción [texbem](texbem---ps.md) o texbeml no se pueden leer más adelante, excepto por otro texbem o texbeml.


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

A continuación se muestra un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Este ejemplo requiere las siguientes texturas en las siguientes fases de textura.

-   A la fase 0 se le asigna un mapa de rugosidad con datos Perturbation (du, DV).
-   En la fase 1 se le asigna un mapa de textura con datos de color.
-   texbeml establece los datos de la matriz en la fase de textura que se muestrea. Esto es diferente de la funcionalidad de la canalización de función fija en la que los datos de Perturbation y las matrices ocupan la misma fase de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 