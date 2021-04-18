---
description: Constantes de mayúsculas del sombreador de vértices. El miembro VS20Caps de D3DCAPS9 usa estas constantes.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714845"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Constantes de mayúsculas del sombreador de vértices. El miembro VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.



| \#define                              | Value          | Descripción                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVS20CAPS \_ PREDICATION              | (1 << 0) | Se admite la instrucción predication. Consulte [SETP \_ COMP-vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH | 24             | El nivel máximo de anidamiento de instrucciones de control de flujo dinámico ([break-vs](../direct3dhlsl/break---vs.md), [break \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [If \_ COMP-vs](../direct3dhlsl/if-comp---vs.md), if \_ COMP-vs, [si es Pred-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH | 0              | El nivel mínimo de anidamiento de instrucciones de control de flujo dinámico ([break-vs](../direct3dhlsl/break---vs.md), [break \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [If \_ COMP-vs](../direct3dhlsl/if-comp---vs.md), if \_ COMP-vs, [si es Pred-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Max \_ NUMTEMPS                | 32             | Número máximo de registros temporales admitidos.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ min \_ NUMTEMPS                | 12             | El número mínimo de registros temporales admitidos.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH  | 4              | La profundidad máxima del anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .                                                                                           |
| D3DVS20 \_ min \_ STATICFLOWCONTROLDEPTH  | 1              | La profundidad mínima de anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .                                                                                           |



 

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
