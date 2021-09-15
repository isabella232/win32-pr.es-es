---
title: dcl_output_sgv (sm4 - asm)
description: dcl \_ output \_ sgv (sm4 - asm)
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573912"
---
# <a name="dcl_output_sgv-sm4---asm"></a>dcl \_ output \_ sgv (sm4 - asm)

Declara un registro de salida que contiene un [parámetro de valor del](dx-graphics-hlsl-semantics.md) sistema.



| dcl \_ output \_ sgv oN *\[ .mask \]*, *systemValue* |
|-----------------------------------------------|



 



| Elemento                                                                                                                               | Descripción                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[en \] Un registro de datos de salida; *N* es un entero que denota el número de registro.<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*<br/>                                                         | \[en \] Opcional. Máscara de componente (.xyzw) que especifica cuál de los componentes de registro se va a usar.<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*<br/> | \[en El nombre del valor del sistema, que es una cadena (vea semántica del valor del \] [sistema](dx-graphics-hlsl-semantics.md)) sin el prefijo \_ "SV".<br/> |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo:


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





