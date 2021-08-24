---
description: Se puede usar un bloque de estado para capturar todos los estados del dispositivo (vea State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Guardar todos los estados del dispositivo con un Bloque de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffda5b5d637a31c774e97af85ddeca78b0995ee53c015bb2dcd245b42277a4cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520086"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Guardar todos los estados del dispositivo con un Bloque de estado (Direct3D 9)

Se puede usar un bloque de estado para capturar todos los estados del dispositivo (vea State Blocks Save and Restore State (Direct3D 9) [Guardar y restaurar estado [(Direct3D 9)].](state-blocks-save-and-restore-state.md) Los siguientes elementos de estado se incluyen en el estado del dispositivo:

-   Estado de vértice (vea [Guardar estados de vértice con un Bloque de estado (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Estado de píxel (vea [Guardar el estado de píxel con un Bloque de estado (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Cada textura asignada a un muestreador.
-   Cada textura de vértice.
-   Textura de mapa de desplazamiento de cada desplazamiento.
-   Paleta de texturas actual.
-   Para cada secuencia de vértices: un puntero al búfer de vértices, cada argumento de [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api)y el divisor (si hay alguno) de [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Puntero al búfer de índice.
-   Ventanilla.
-   Rectángulo de las manos.
-   Matrices de mundo, vista y proyección.
-   La textura se transforma.
-   Planos de recorte (si los hay).
-   El material actual.

Para capturar todos los estados del dispositivo con un bloque de estado, especifique D3DSBT ALL al llamar a \_ [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estado: Guardar y restaurar estado de bloques de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
