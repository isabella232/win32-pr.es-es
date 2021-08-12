---
title: bufinfo (sm5 - asm)
description: Consultar el recuento de elementos en un búfer (pero no el búfer constante).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107896973e7457b4bf596843ec77934d95675d50a146190a7f9f40e1c2ce3c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287588"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (sm5 - asm)

Consultar el recuento de elementos en un búfer (pero no el búfer constante).



| bufinfo dest \[ .mask \] , srcResource |
|------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección de los resultados.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Buffer, que no sea un búfer constante, en un SRV (t \# ) o UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Comentarios

Todos los componentes *de reciben el* número entero de elementos en la vista de recursos del sombreador del búfer. El número de elementos depende de los parámetros de vista, como el formato de memoria.

Para un búfer con tipo SRV o UAV, el valor devuelto es el número de elementos de la vista (donde un elemento es una unidad del formato con tipo).

Para un búfer sin formato SRV o UAV, el valor devuelto es el número de bytes de la vista.

Para un SRV o UAV de búfer estructurado, el valor devuelto es el número de estructuras de la vista.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible. |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





