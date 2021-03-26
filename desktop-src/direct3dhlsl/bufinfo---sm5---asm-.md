---
title: bufinfo (SM5-ASM)
description: Consultar el recuento de elementos en un búfer (pero no en el búfer de constantes).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996905"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (SM5-ASM)

Consultar el recuento de elementos en un búfer (pero no en el búfer de constantes).



| bufinfo dest \[ . Mask \] , srcResource |
|------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección de los resultados.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] búfer, que no sea un búfer de constantes, en un SRV (t \# ) o UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Observaciones

Todos los componentes de *dest* reciben el número entero de elementos de la vista de recursos del sombreador del búfer. El número de elementos depende de los parámetros de vista, como el formato de memoria.

En el caso de un búfer con tipo SRV o UAV, el valor devuelto es el número de elementos de la vista (donde un elemento es una unidad del formato con tipo).

En el caso de un búfer sin formato SRV o UAV, el valor devuelto es el número de bytes de la vista.

Para un búfer estructurado SRV o UAV, el valor devuelto es el número de estructuras de la vista.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





