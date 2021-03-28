---
title: dcl_output oMask (SM5-ASM)
description: Declare un registro de salida para que lo escriba el sombreador.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419990"
---
# <a name="dcl_output-omask-sm5---asm"></a>\_oMask de salida de DCL (SM5-ASM)

Declare un registro de salida para que lo escriba el sombreador.



| salida de DCL \_ o \# \[ . Mask\] |
|--------------------------|



 



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*aceptar*<br/> | \[en \] el registro de salida.<br/> |



 

## <a name="remarks"></a>Observaciones


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Restricciones

-   La máscara de componentes puede ser cualquier subconjunto de \[ xyzw \] . Sin embargo, dejar huecos entre componentes desperdicia espacio.
-   Es legal declarar un supraconjunto de la máscara de componente declarada para la entrada en la siguiente fase. Sin embargo, no se permiten las máscaras mutuamente excluyentes. El sombreador de vértices que genera O3. XY significa que el sombreador de píxeles que inserta V3. z no es válido, pero la entrada V3. x o V3. y o V3. XY es válida.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





