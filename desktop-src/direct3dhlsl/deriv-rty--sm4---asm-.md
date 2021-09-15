---
title: deriv_rty (sm4 - asm)
description: Render-target y equivalente de deriv \_ rtx.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573864"
---
# <a name="deriv_rty-sm4---asm"></a>deriv \_ rty (sm4 - asm)

Render-target y equivalente [de deriv \_ rtx](deriv-rtx--sm4---asm-.md).



| deriv \_ rty \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El componente de la operación.<br/>             |



 

## <a name="remarks"></a>Observaciones

Solo se calcula un único par derivado x,y para cada marca de 2 x 2 píxeles.

Esta operación depende del hardware.

Implementación de rasterizador de referencia para triángulos:

-   Sombreador de píxeles siempre ejecuta Sombreador en un cuadránxel de 2 x 2 píxeles en el paso de bloqueo (incluso a través del control de flujo, enmascaramiento de píxeles deshabilitados).
-   Los cuadránáxeles siempre tienen coordenadas de píxel numeradas (x e y) para el píxel superior izquierdo.
-   Los píxeles ficticios se ejecutan como primitivos si el primitivo es demasiado pequeño para rellenar un cuadrándice de 2x2.
-   [Deriv \_ rtx](deriv-rtx--sm4---asm-.md) se calcula eligiendo primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada y del cuadránxel. A continuación, el resultado se calcula como: *src0*(píxel x impar) - *src0*(incluso x píxeles) \[ por componente\]
-   **Deriv \_ rty se** calcula eligiendo primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada x del cuadránxel. A continuación, el resultado se calcula como: *src0*(píxel impar y) - *src0*(píxel y par) \[ por componente\]

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





