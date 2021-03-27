---
title: dcl_input_sv (SM4-ASM)
description: '\_ \_ SV de entrada de DCL (SM4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785021"
---
# <a name="dcl_input_sv-sm4---asm"></a>\_ \_ SV de entrada de DCL (SM4-ASM)

Declara un registro de entrada de sombreador que espera que se proporcione un [valor del sistema](dx-graphics-hlsl-semantics.md) desde una fase anterior.



| \_entrada \_ de DCL SV v *N \[ . \] Mask*, *systemValueName \[ , \] interpolationMode* |
|------------------------------------------------------------------------|



 



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
<td><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em><br/></td>
<td>de Nombre del valor del sistema que es una cadena (vea <a href="dx-graphics-hlsl-semantics.md">semántica de valor del sistema</a>) sin el &quot; &quot; prefijo SV_.<br/></td>
</tr>
<tr class="odd">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br/></td>
<td>[in] Opcional. El modo de interpolación que afecta al modo en que se calculan los valores durante la rasterización; el modo solo lo usa un sombreador de píxeles. Puede ser uno de los siguientes valores: <br/>
<ul>
<li>constante: no se interpola entre los valores de registro.</li>
<li>lineal: interpolación lineal entre valores de registro.</li>
<li>linearCentroid: igual que lineal, pero centroide en el muestreo múltiple.</li>
<li>linearNoperspective: igual que lineal pero sin corrección de perspectiva.</li>
<li>linearNoperspectiveCentroid: igual que lineal, pero sin corrección de la perspectiva y centroide en el muestreo múltiple.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Una máscara de componente para una declaración de valor del sistema puede ser cualquier subconjunto adecuado de \[ xyzw \] ; las declaraciones no pueden superponerse (cada declaración debe seguir a la secuencia xyzw). Al declarar valores del sistema escalares (distancia de clip y distancia de selección, por ejemplo), puede declarar varios valores del sistema en un solo registro. Si lo hace, asegúrese de que otros modificadores, como los modos de interpolación coinciden.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestran algunos ejemplos:


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
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

 

 





