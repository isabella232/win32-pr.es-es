---
title: dcl_indexRange (SM4-ASM)
description: DCL \_ indexRange (SM4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983910"
---
# <a name="dcl_indexrange-sm4---asm"></a>DCL \_ indexRange (SM4-ASM)

Declara un intervalo de registros al que se tendrá acceso mediante el índice (un entero calculado en el sombreador).



| DCL \_ IndexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br/></td>
<td>de Primer registro al que se va a obtener acceso por índice. <br/>
<ul>
<li><em>minRegister</em> es <strong>v</strong> para un registro de entrada del sombreador de píxeles o vértices <strong>, o o</strong> para un registro de salida del sombreador de vértices.</li>
<li><em>M</em> es un entero que denota el número de registro.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>de Último registro al que obtener acceso por índice. La misma forma que <em>minRegister</em> , excepto <em>N</em> , es el número de registro.<br/></td>
</tr>
</tbody>
</table>



 

Se aplican las restricciones siguientes a todos los registros:

-   Los registros min y Max deben ser del mismo tipo y tener las mismas máscaras de componentes (si se declaran máscaras).
-   Un registro puede tener varios intervalos de índice, siempre y cuando no se superpongan.
-   El número de registro mínimo debe ser menor que el número de registro máximo.
-   Un registro de índice no puede contener un [valor del sistema](dx-graphics-hlsl-semantics.md).
-   La indización de un registro fuera de la declaración de índice máximo genera resultados no definidos.

Los registros de entrada del sombreador de píxeles deben usar el mismo modo de interpolación; los registros de salida del sombreador de píxeles no se pueden indexar.

Un registro de entrada del sombreador de geometría tiene dos dimensiones (eje de vértices, eje de atributo); el intervalo de índice solo se aplica al eje de atributo porque el eje del vértice siempre es totalmente indexable.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo:


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





