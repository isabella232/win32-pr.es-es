---
description: El sombreador de vértices encapsa las constantes. El miembro VS20Caps de D3DCAPS9 usa estas constantes.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342950"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

El sombreador de vértices encapsa las constantes. El miembro VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.



| \#Definir                              | Valor          | Descripción                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PREDICADO D3DVS20CAPS \_              | (1 << 0) | Se admite el predicado de instrucciones. Vea [setp \_ comp - vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH | 24             | El nivel máximo de anidamiento de instrucciones de control de flujo dinámico[(break - vs](../direct3dhlsl/break---vs.md), [break comp - \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH | 0              | El nivel mínimo de anidamiento de instrucciones de control de flujo dinámico[(break - vs](../direct3dhlsl/break---vs.md), [break comp - \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| NÚMERO MÁXIMO DE \_ NUMTEMPS D3DVS20 \_                | 32             | Número máximo de registros temporales admitidos.                                                                                                                                                                                                                                                        |
| NUMTEMPS DE D3DVS20 \_ \_ MIN                | 12             | Número mínimo de registros temporales admitidos.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH  | 4              | La profundidad máxima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions).                                                                                           |
| D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH  | 1              | La profundidad mínima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions).                                                                                           |



 

## <a name="constant-information"></a>Información constante



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
