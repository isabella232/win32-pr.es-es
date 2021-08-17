---
title: dcl_indexRange (sm4 - asm)
description: dcl \_ indexRange (sm4 - asm)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a652d200a211eb5528f6e7ecdedf2cc20579817d1f0148d59855d1e864de55de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727195"
---
# <a name="dcl_indexrange-sm4---asm"></a>dcl \_ indexRange (sm4 - asm)

Declara un intervalo de registros a los que se accederá mediante índice (un entero calculado en el sombreador).



| dcl \_ indexRange *minRegisterM*, *maxRegisterN* |
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
<td>[in] Primer registro al que se accede por índice. <br/>
<ul>
<li><em>minRegister</em> es v para <strong>un</strong> registro de entrada de sombreador de vértices o píxeles, <strong>o para un</strong> registro de salida del sombreador de vértices.</li>
<li><em>M</em> es un entero que denota el número de registro.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>[in] Último registro al que se accede por índice. El mismo formato que <em>minRegister excepto</em> <em>N</em> es el número de registro.<br/></td>
</tr>
</tbody>
</table>



 

Las restricciones siguientes se aplican a todos los registros:

-   Los registros mínimo y máximo deben ser del mismo tipo y tener las mismas máscaras de componente (si se declaran máscaras).
-   Un registro puede tener varios intervalos de índice, siempre que no se superpongan.
-   El número de registro mínimo debe ser menor que el número de registro máximo.
-   Un registro de índice no puede contener [un valor del sistema](dx-graphics-hlsl-semantics.md).
-   La indexación de un registro fuera de la declaración de índice máximo genera resultados no definidos.

Los registros de entrada del sombreador de píxeles deben usar el mismo modo de interpolación; Los registros de salida del sombreador de píxeles no son indexables.

Un registro de entrada del sombreador de geometría tiene dos dimensiones (eje de vértices, eje de atributos); el intervalo de índice solo se aplica al eje de atributo porque el eje de vértice siempre es totalmente indexable.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo:


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





