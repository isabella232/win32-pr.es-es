---
title: dcl_resource (SM4-ASM)
description: '\_recurso DCL (SM4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785008"
---
# <a name="dcl_resource-sm4---asm"></a>\_recurso DCL (SM4-ASM)

Declara un recurso de entrada de sombreador no multimuestreado.



| DCL \_ Resource *tN*, *resourceType*, *ReturnType (s)* |
|-----------------------------------------------------|



 

Declara un recurso de entrada de sombreador de muestreo múltiple.



| DCL \_ Resource *tN*, *resourceType \[ tamaño \] nn*, *ReturnType (s)* |
|---------------------------------------------------------------|



 



| Elemento                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[en \] el registro de textura, donde *N* es un entero que denota el número de registro.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*<br/>                                   | \[en \] cualquier tipo de objeto que se muestra en la página [Texture-Object](dx-graphics-hlsl-to-type.md) .<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType \[ tamaño \] NN*<br/> | \[en \] un tipo de objeto Texture2D o Texture2DArray (vea la página [Texture-Object](dx-graphics-hlsl-to-type.md) ); *size* es un entero opcional que denota el número de elementos de la matriz; *Nn* es un entero que denota el número de muestras de varios.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*<br/>                               | \[en \] el tipo de valor devuelto por componente, que es uno de los siguientes: UNORM, SNORM, Sint, uint o float. El número de tipos de valor devuelto puede ser tan pocos como 1 (si todos los componentes son del mismo tipo), pero puede ser de hasta cuatro.<br/>                                          |



 

Se tiene acceso a un recurso en HLSL mediante la [carga](dx-graphics-hlsl-to-load.md); también se puede tener acceso a una textura no multimuestreada mediante cualquiera de los métodos de ejemplo de [objeto de textura](dx-graphics-hlsl-to-type.md) HLSL.

Si un recurso se enlaza a una fase del sombreador, el formato de los recursos se validará con el tipo de valor devuelto.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo:


```
dcl_resource t3, buffer, UNORM
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

 

 





