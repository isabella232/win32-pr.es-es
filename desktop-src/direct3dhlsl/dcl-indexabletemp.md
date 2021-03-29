---
title: dcl_indexableTemp (SM4-ASM)
description: DCL \_ indexableTemp (SM4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996988"
---
# <a name="dcl_indexabletemp-sm4---asm"></a>DCL \_ indexableTemp (SM4-ASM)

Declara un registro temporal indexable.



| DCL \_ indexableTemp x *N \[ tamaño \] , ComponentCount* |
|-------------------------------------------------|



 



| Elemento                                                                                                                           | Descripción                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/>                                                                         | \[en \] un entero que denota el número de registro.<br/>                              |
| <span id="_size_"></span><span id="_SIZE_"></span>*\[ajusta\]*<br/>                                                        | \[en \] un valor entero opcional. El número de elementos de la matriz de registro.<br/>  |
| <span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*<br/> | \[en \] un valor entero opcional. El número de componentes de la matriz de registro.<br/> |



 

Un registro contiene suficiente espacio para un valor de cuatro componentes de 32 bits; el número de elementos de la matriz de registros temporales (indexables y [no indexables](dcl-temps.md)) no puede superar 4096.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.

## <a name="example"></a>Ejemplo

Estos son algunos ejemplos del código generado para los registros indexables.


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
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

 

 





