---
title: dcl_input_sv (sm4 - asm)
description: dcl \_ input \_ sv (sm4 - asm)
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b703677bb4e99f70443c89a8f907fa7abfaaff11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481271"
---
# <a name="dcl_input_sv-sm4---asm"></a>dcl \_ input \_ sv (sm4 - asm)

Declara un registro de entrada de sombreador que espera que se proporciona un valor [del](dx-graphics-hlsl-semantics.md) sistema de una fase anterior.



| dcl \_ input sv v N \_ *\[ \] .mask*, *systemValueName \[ , interpolationMode \]* |
|------------------------------------------------------------------------|



 




| Elemento | Descripción | 
|------|-------------|
| <span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em><br /> | [in] Registro de datos de vértice. <br /><ul><li><em>N</em> es un entero que identifica el número de registro.</li><li><em>[.mask] es</em> una máscara de componente opcional (.xyzw) que especifica cuál de los componentes de registro se va a usar.</li></ul> | 
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em><br /> | [in] Nombre del valor del sistema que es una cadena (vea semántica de valores del <a href="dx-graphics-hlsl-semantics.md">sistema)</a>sin el prefijo "SV_".<br /> | 
| <span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br /> | [in] Opcional. Modo de interpolación que afecta a cómo se calculan los valores durante la rasterización; el modo solo lo usa un sombreador de píxeles. Puede ser uno de los siguientes valores: <br /><ul><li>constant: no interpola entre los valores de registro.</li><li>linear: interpola linealmente entre valores de registro.</li><li>linearCentroid: igual que lineal pero centroide fija al multimuestreo.</li><li>linearNoperspective: igual que lineal pero sin corrección de perspectiva.</li><li>linearNoperspectiveCentroid: igual que lineal pero sin corrección de perspectiva y centroide fija cuando se multimuestreo.</li></ul> | 




 

Una máscara de componente para una declaración de valor del sistema puede ser cualquier subconjunto adecuado de xyzw; es posible que las declaraciones no se superpongan (cada declaración debe \[ \] seguir la secuencia xyzw). Al declarar valores escalares del sistema (por ejemplo, distancia de recorte y distancia cull), puede declarar varios valores del sistema en un único registro. Si lo hace, asegúrese de que otros modificadores, como los modos de interpolación, coincidan.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

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

[Ensamblado del modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





