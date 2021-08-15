---
title: dcl_input (sm4 - asm)
description: entrada dcl \_ (sm4 - asm)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3242c2f1e753407d239057fdc4af0a6f04d6d83a66e2a22ffb1be929583c21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986745"
---
# <a name="dcl_input-sm4---asm"></a>entrada dcl \_ (sm4 - asm)

Declara un registro de entrada de sombreador.



| dcl \_ input v N *\[ .mask , \] \[ interpolationMode \]* |
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
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em><br/></td>
<td>[in] Registro de datos de vértice. <br/>
<ul>
<li><em>N</em> es un entero que identifica el número de registro.</li>
<li><em>[.mask] es</em> una máscara de componente opcional (.xyzw) que especifica cuál de los componentes de registro se va a usar.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br/></td>
<td>[in] Opcional. Modo de interpolación, que solo se respeta en los registros de entrada del sombreador de píxeles. Puede ser uno de los siguientes valores: <br/>
<ul>
<li>constant: no interpola entre los valores de registro.</li>
<li>linear: interpola linealmente entre los valores de registro.</li>
<li>linearCentroid: igual que lineal pero centroide fija al multimuestreo.</li>
<li>linearNoperspective: igual que lineal pero sin corrección de perspectiva.</li>
<li>linearNoperspectiveCentroid: igual que lineal, centroide con fijación cuando se multimuestreo, sin corrección de perspectiva.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a>Notas de interpolación

De forma predeterminada, los atributos de vértice se interpolan desde un centro de píxeles al realizar suavizado de contorno de múltiples muestras. Si no se cubre un centro de píxeles, un atributo se extrapola a un centro de píxeles antes de la interpolación.

Para un píxel que no está totalmente cubierto o un atributo que no cubre un centro de píxeles, puede especificar el muestreo de centroide que obliga a que el muestreo se produzca en algún lugar dentro del área cubierta del píxel. Dado que se aplica una máscara de ejemplo (si se usa) antes de calcular el centroide, no se puede elegir ninguna ubicación de ejemplo enmascarada por la máscara de ejemplo como ubicación de centroide.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Para identificar la entrada como un valor del sistema, use [dcl \_ input sv \_ (sm4 - asm).](dcl-input-sv.md)

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestran algunos ejemplos.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





