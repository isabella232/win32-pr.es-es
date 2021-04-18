---
description: Un bloque de estado se puede usar para capturar todos los Estados de dispositivo (consulte bloques de estado guardar y restaurar estado (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Guardar todos los Estados de los dispositivos con un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686378"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Guardar todos los Estados de los dispositivos con un StateBlock (Direct3D 9)

Un bloque de estado se puede usar para capturar todos los Estados de dispositivo (consulte [bloques de estado guardar y restaurar estado (Direct3D 9)](state-blocks-save-and-restore-state.md)). Los siguientes elementos de estado se incluyen en el estado del dispositivo:

-   Estado del vértice (vea [guardar los Estados de los vértices con un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Estado de píxel (consulte [almacenamiento del estado de los píxeles con un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Cada textura asignada a una muestra.
-   Cada textura de vértice.
-   Cada textura de mapa de desplazamiento.
-   Paleta de textura actual.
-   Para cada flujo de vértices: un puntero al búfer de vértices, cada argumento de [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api)y el divisor (si existe) de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Puntero al búfer de índice.
-   La ventanilla.
-   Rectángulo de tijeras.
-   Matrices del mundo, vista y proyección.
-   Transformaciones de textura.
-   Planos de recorte (si existen).
-   Material actual.

Para capturar todos los Estados de dispositivo con un bloque de estado, especifique D3DSBT \_ All al llamar a [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estado de guardado y restauración de bloques de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
