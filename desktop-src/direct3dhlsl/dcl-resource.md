---
title: dcl_resource (sm4 - asm)
description: recurso dcl \_ (sm4 - asm)
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f23fac2f6671584c69ecad045d13e885e86fb260164675da3bc51f7edf847f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515640"
---
# <a name="dcl_resource-sm4---asm"></a>recurso dcl \_ (sm4 - asm)

Declara un recurso de entrada de sombreador no multimuestreo.



| dcl \_ resource *tN*, *resourceType*, *returnType(s)* |
|-----------------------------------------------------|



 

Declara un recurso de entrada de sombreador multimuestreo.



| dcl \_ resource *tN*, *resourceType size \[ \] NN*, *returnType(s)* |
|---------------------------------------------------------------|



 



| Elemento                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[en \] El registro de textura, donde *N* es un entero que denota el número de registro.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*<br/>                                   | \[en \] Cualquier tipo de objeto enumerado en la página [texture-object.](dx-graphics-hlsl-to-type.md)<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*NN de \[ tamaño \] resourceType*<br/> | \[en \] un tipo de objeto Texture2D o Texture2DArray (vea la página [texture-object);](dx-graphics-hlsl-to-type.md) *size* es un entero opcional que denota el número de elementos de la matriz; *NN* es un entero que denota el número de muestras múltiples.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*<br/>                               | \[en tipo de valor devuelto por componente, que es uno de los \] siguientes: UNORM, SNORM, SINT, UINT o FLOAT. El número de tipos de valor devuelto puede ser tan solo 1 (si todos los componentes son del mismo tipo), pero puede ser de hasta cuatro.<br/>                                          |



 

Se tiene acceso a un recurso en HLSL mediante [load](dx-graphics-hlsl-to-load.md); También se puede acceder a una textura no multimuestreo mediante cualquiera de los métodos de ejemplo de objeto de [textura](dx-graphics-hlsl-to-type.md) HLSL.

Si un recurso está enlazado a una fase del sombreador, el formato del recurso se validará con el tipo de valor devuelto.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo:


```
dcl_resource t3, buffer, UNORM
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

 

 





