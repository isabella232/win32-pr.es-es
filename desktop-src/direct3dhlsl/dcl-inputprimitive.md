---
title: dcl_inputPrimitive (sm4 - asm)
description: dcl \_ inputPrimitive (sm4 - asm)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0660fe4da14a20f074e4f04de8891fc0848f2597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479901"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>dcl \_ inputPrimitive (sm4 - asm)

Declara el tipo primitivo para las entradas del sombreador de geometría.



| dcl \_ inputPrimitive *type* |
|----------------------------|



 




| Elemento | Descripción | 
|------|-------------|
| <span id="type"></span><span id="TYPE"></span><em>Tipo</em><br /> | [in] Tipo primitivo de datos de entrada, que es uno de los siguientes: <br /><ul><li><em>point</em> - point list</li><li><em>line</em> - line list</li><li><em>triangle:</em> lista de triángulos</li><li><em>line_adj:</em> lista de líneas con datos de adyacencia</li><li><em>triangle_adj:</em> lista de triángulos con datos de adyacencia</li></ul> | 




 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo:


```
dcl_inputPrimitive triangle
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

[Ensamblado del modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





