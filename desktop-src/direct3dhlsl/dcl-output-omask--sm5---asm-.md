---
title: dcl_output oMask (sm5 - asm)
description: Declare un registro de salida que va a escribir el sombreador.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a6860904b557bc21a5202bbfd60105852adc260580457afb02b4fe6d92352b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068515"
---
# <a name="dcl_output-omask-sm5---asm"></a>dcl \_ output oMask (sm5 - asm)

Declare un registro de salida que va a escribir el sombreador.



| dcl \_ output o \# \[ .mask\] |
|--------------------------|



 



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*o*<br/> | \[en \] El registro de salida.<br/> |



 

## <a name="remarks"></a>Comentarios


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Restricciones

-   La máscara de componente puede ser cualquier subconjunto de \[ \] xyzw. Sin embargo, dejar espacios entre componentes desperdicia espacio.
-   Es legal declarar un superconjunto de la máscara de componente declarada para la entrada en la fase siguiente. Sin embargo, no se permiten máscaras mutuamente excluyentes. El sombreador de vértices que genera o3.xy significa que la entrada del sombreador de píxeles v3.z no es válida, pero la entrada de v3.x o v3.y o v3.xy es válida.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





