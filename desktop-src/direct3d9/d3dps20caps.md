---
description: Marcas de capacidad del sombreador de píxeles.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153454"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Marcas de capacidad del sombreador de píxeles.



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                                     | Value          | Descripción                                                                                                                                                                                                       |
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      | (1 << 0) | Se admite permutación arbitrario.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Se admiten las instrucciones de degradado.                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION           | (1 << 2) | Se admite la instrucción predication. Consulte [SETP \_ COMP-PS](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | No hay ningún límite en el número de lecturas dependientes por instrucción.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT | (1 << 4) | No hay ningún límite en el número de instrucciones Tex.                                                                                                                                                              |
| D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH        | 24             | El nivel máximo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH        | 0              | Nivel mínimo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Max \_ NUMTEMPS                       | 32             | El controlador admitirá como máximo este número de registro temporal.                                                                                                                                                     |
| D3DPS20 \_ min \_ NUMTEMPS                       | 12             | El controlador admitirá al menos este registro temporal.                                                                                                                                                    |
| D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH         | 4              | La profundidad máxima del anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) . |
| D3DPS20 \_ min \_ STATICFLOWCONTROLDEPTH         | 1              | La profundidad mínima de anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) . |
| D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS            | 512            | El controlador admitirá como máximo estas muchas instrucciones.                                                                                                                                                           |
| D3DPS20 \_ min \_ NUMINSTRUCTIONSLOTS            | 96             | El controlador admitirá al menos estas muchas instrucciones.                                                                                                                                                          |



 

El \_ miembro D3DPSHADERCAPS2 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
