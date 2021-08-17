---
title: dcl_indexableTemp (sm4 - asm)
description: dcl \_ indexableTemp (sm4 - asm)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f1d6e02b36daef0643910d69404adc0973ebbcf6370ae5f5c11ad2aa7bd3480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793451"
---
# <a name="dcl_indexabletemp-sm4---asm"></a>dcl \_ indexableTemp (sm4 - asm)

Declara un registro temporal indexable.



| dcl \_ indexableTemp x *N size , \[ \] ComponentCount* |
|-------------------------------------------------|



 



| Elemento                                                                                                                           | Descripción                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/>                                                                         | \[en \] Entero que denota el número de registro.<br/>                              |
| <span id="_size_"></span><span id="_SIZE_"></span>*\[Tamaño\]*<br/>                                                        | \[en \] Un valor entero opcional. Número de elementos de la matriz de registros.<br/>  |
| <span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*<br/> | \[en \] Un valor entero opcional. Número de componentes de la matriz de registro.<br/> |



 

Un registro contiene suficiente espacio para un valor de cuatro componentes de 32 bits; El número de elementos de la matriz de registros temporales (indexable y no [indexable)](dcl-temps.md)no puede superar 4096.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

Estos son algunos ejemplos del código generado para los registros indexables.


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





