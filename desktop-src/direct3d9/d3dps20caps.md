---
description: Marcas de funcionalidad del sombreador de píxeles.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4eed8fb6c7a5c4c4da31185dc4cc8c1661f7109
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343120"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Marcas de funcionalidad del sombreador de píxeles.



| \#Definir                                     | Valor          | Descripción                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWAPILE      | (1 << 0) | Se admite el desdobado arbitrario.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Se admiten instrucciones de degradado.                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION           | (1 << 2) | Se admite el predicado de instrucciones. Consulte [setp \_ comp - ps](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | No hay ningún límite en el número de lecturas dependientes por instrucción.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTESTRUCTIONLIMIT | (1 << 4) | No hay ningún límite en el número de instrucciones de texas.                                                                                                                                                              |
| D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH        | 24             | El nivel máximo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH        | 0              | El nivel mínimo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MAX \_ NUMTEMPS                       | 32             | El controlador admitirá como máximo este gran número de registros temporales.                                                                                                                                                     |
| D3DPS20 \_ MIN \_ NUMTEMPS                       | 12             | El controlador admitirá al menos este número de registros temporales.                                                                                                                                                    |
| D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH         | 4              | La profundidad máxima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions. |
| D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH         | 1              | La profundidad mínima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions). |
| D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS            | 512            | El controlador admitirá como máximo estas muchas instrucciones.                                                                                                                                                           |
| D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS            | 96             | El controlador admitirá al menos estas muchas instrucciones.                                                                                                                                                          |



 

El miembro D3DPSHADERCAPS2 0 de \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|  Requisito                        | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
