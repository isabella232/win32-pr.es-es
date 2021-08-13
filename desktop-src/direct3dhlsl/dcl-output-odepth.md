---
title: dcl_output oDepth (sm4 - asm)
description: dcl \_ output oDepth (sm4 - asm)
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b343230d8f1ab488bd11410eddefbca58ebedd0f1ff7962f80049a8678833f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793151"
---
# <a name="dcl_output-odepth-sm4---asm"></a>dcl \_ output oDepth (sm4 - asm)

Declara que un sombreador de píxeles usará el registro de profundidad de salida.



| dcl \_ output oDepth |
|--------------------|



 

El valor del registro de profundidad de salida se usa durante una comparación de profundidad (si la comparación de profundidad está habilitada).

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestran algunos ejemplos.


```
dcl_output oDepth
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

 

 




