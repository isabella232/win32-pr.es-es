---
title: dcl_input (SM4-ASM)
description: '\_entrada de DCL (SM4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996981"
---
# <a name="dcl_input-sm4---asm"></a>\_entrada de DCL (SM4-ASM)

Declara un registro de entrada de sombreador.



| \_entrada de DCL v *N \[ . Mask \] \[ , \] interpolationMode* |
|-------------------------------------------------|



 



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
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Mask]</em><br/></td>
<td>de Un registro de datos de vértice. <br/>
<ul>
<li><em>N</em> es un entero que identifica el número de registro.</li>
<li><em>[. Mask]</em> es una máscara de componente opcional (. xyzw) que especifica cuál de los componentes de registro se va a usar.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br/></td>
<td>[in] Opcional. El modo de interpolación, que solo se admite en los registros de entrada del sombreador de píxeles. Puede ser uno de los siguientes valores: <br/>
<ul>
<li>constante: no se interpola entre los valores de registro.</li>
<li>lineal: interpolación lineal entre valores de registro.</li>
<li>linearCentroid: igual que lineal, pero centroide en el muestreo múltiple.</li>
<li>linearNoperspective: igual que lineal pero sin corrección de perspectiva.</li>
<li>linearNoperspectiveCentroid: igual que lineal, centroide se fija al muestreo múltiple, sin corrección de perspectiva.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a>Notas de interpolación

De forma predeterminada, los atributos de vértice se interpolan desde un centro de píxeles al realizar el suavizado de contorno de muestreo. Si no se trata de un centro de píxeles, se extrapola un atributo a un centro de píxeles antes de la interpolación.

En el caso de un píxel que no esté totalmente cubierto o de un atributo que no cubra un centro de píxeles, puede especificar el muestreo centroide, que fuerza el muestreo para que se produzca en algún lugar dentro del área cubierta del píxel. Dado que se aplica una máscara de ejemplo (si se usa) antes de que se calcule centroide, cualquier ubicación de ejemplo enmascarada por la máscara de ejemplo no se puede elegir como una ubicación de centroide.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Para identificar la entrada como un valor del sistema, use [DCL \_ Input \_ SV (SM4-ASM)](dcl-input-sv.md).

Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.

## <a name="example"></a>Ejemplo

Estos son algunos ejemplos.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





