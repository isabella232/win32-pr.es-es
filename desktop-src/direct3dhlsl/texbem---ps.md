---
title: texbem-PS
description: Aplicar una transformación de mapa de entorno de rugosidad falsa. Para ello, se modifican los datos de la dirección de textura del registro de destino, utilizando los datos de dirección Perturbation (du, DV) y una matriz de entorno de rugosidad 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984007"
---
# <a name="texbem---ps"></a>texbem-PS

Aplicar una transformación de mapa de entorno de rugosidad falsa. Para ello, se modifican los datos de la dirección de textura del registro de destino, utilizando los datos de dirección Perturbation (du, DV) y una matriz de entorno de rugosidad 2D.

## <a name="syntax"></a>Sintaxis



| texbem DST, src |
|-----------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbem                | x    | x    | x    |      |      |      |       |      |       |



 

Los datos de color rojo y verde del registro de src se interpretan como los datos de Perturbation (du, DV).

Esta instrucción transforma los componentes rojo y verde en el registro de origen mediante la matriz de asignación del entorno de rugosidad 2D. El resultado se agrega al conjunto de coordenadas de textura correspondiente al número de registro de destino y se usa para muestrear la fase de textura actual.

Esta operación siempre interpreta du y DV como cantidades firmadas. En las versiones 1 \_ y 1 \_ 1, no se permite el modificador de entrada de [escala firmada del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) en el argumento de entrada.

Esta instrucción genera resultados definidos cuando las texturas de entrada contienen datos de formato firmados. Los datos con formato mixto solo funcionan si los dos primeros canales contienen datos firmados. Para obtener más información sobre los formatos de Surface, vea [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

Se puede usar para una variedad de técnicas basadas en la dirección Perturbation, incluida la asignación de entorno falsa por píxel y la iluminación difusa (asignación de rugosidad).

Al utilizar esta instrucción, los registros de textura deben seguir la secuencia siguiente.


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



Los cálculos realizados dentro de la instrucción se muestran a continuación.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



u ' = TextureCoordinates (Stage m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (Stage m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (Stage m) \* t (n)<sub>G</sub> v ' = TextureCoordinates (Stage m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (Stage m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (Stage m) \* t (n)<sub>G</sub> t (m)<sub>RGBA</sub> = TextureSample (fase m)

usar (u ', v ') como coordenadas

Los datos de registro que ha leído una instrucción texbem-PS o [texbeml-PS](texbeml---ps.md) no se pueden leer más adelante, excepto en otro texbem-PS o texbeml-PS.


```
// This example demonstrates the validation error caused by t0 being reread:
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
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



texbem requiere las siguientes texturas en las siguientes fases de textura.

-   A la fase 0 se le asigna un mapa de rugosidad con datos Perturbation (du, DV).
-   En la fase 1 se usa un mapa de textura con datos de color.
-   Esta instrucción establece los datos de la matriz en la fase de textura que se muestrea.
-   Esto es diferente de la funcionalidad de la canalización de función fija en la que los datos de Perturbation y las matrices ocupan la misma fase de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 