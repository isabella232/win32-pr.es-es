---
title: yd (sm5 - asm)
description: Agregar precisión doble en el componente.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e382ea2660b587a843ecca4c3bae93251a5f9434bd2cdca5899beaf25bb2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793533"
---
# <a name="dadd-sm5---asm"></a>yd (sm5 - asm)

Agregar precisión doble en el componente.



| swd \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .swzzle\] |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Componentes que se agregarán con *src1*.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Los componentes que se agregarán con *src0*<br/>           |



 

## <a name="remarks"></a>Comentarios

Los swzzles válidos para los parámetros de origen son .xyzw, .xyxy, .zwxy, .zwzw. Las máscaras *dest* válidas son .xy, .zw y .xyzw. Las asignaciones siguientes son posteriores a swzzle:

-   *dest* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src0* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src1* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.

F significa número finito-real.



<table>
<tbody>
<tr class="odd">
<td><dl> <strong>src0</strong><br />
<strong>src1-></strong><br />
</dl></td>
<td><strong>-inf</strong></td>
<td><strong>-F</strong></td>
<td><strong>-0</strong></td>
<td><strong>+0</strong></td>
<td><strong>+F</strong></td>
<td><strong>+inf</strong></td>
<td><strong>NaN</strong></td>
</tr>
<tr class="even">
<td><strong>-inf</strong></td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>NaN</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>-F</strong></td>
<td>-inf</td>
<td>-F</td>
<td>src0</td>
<td>src0</td>
<td>+-F o +-0</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>-0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>-0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>+0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>+0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>+F</strong></td>
<td>-inf</td>
<td>+-F o +-0</td>
<td>src0</td>
<td>src0</td>
<td>+F</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>+inf</strong></td>
<td>NaN</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>NaN</strong></td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
</tr>
</tbody>
</table>



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





