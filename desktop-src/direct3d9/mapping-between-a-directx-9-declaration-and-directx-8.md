---
title: Asignación entre declaraciones D3D9 y D3D8
description: Esta tabla asigna miembros de una declaración D3DVERTEXELEMENT9 a una declaración de Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e6c94836499a6f2bf5dc4e88c76b822ef3143278581a4020e76dba16c9869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069035"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Asignación entre declaraciones D3D9 y D3D8

Esta tabla asigna miembros de una [**declaración D3DVERTEXELEMENT9**](d3dvertexelement9.md) a una declaración de Direct3D 8.



| Uso de Direct3D 9           | Índice de uso de Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| POSICIÓN DE D3DDECLUSAGE \_     | 0                      | POSICIÓN DE D3DVSDE \_     |
| POSICIÓN DE D3DDECLUSAGE \_     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ NORMAL       | 0                      | D3DVSDE \_ NORMAL       |
| D3DDECLUSAGE \_ NORMAL       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ PSIZE        | 0                      | D3DVSDE \_ PSIZE        |
| D3DDECLUSAGE \_ COLOR        | 0                      | D3DVSDE \_ DIFUSO      |
| D3DDECLUSAGE \_ COLOR        | 1                      | ESPECULAR D3DVSDE \_     |
| D3DDECLUSAGE \_ TEXCOORD     | n                      | D3DVSDE \_ TEXCOORDn    |



 

Cuando se usa una declaración con el procesamiento de vértices de hardware en un controlador Direct3D 7, el tiempo de ejecución de Direct3D la convierte en una FVF con las reglas siguientes:

-   Solo se debe usar la secuencia 0 (evidente desde el límite MaxStreams).
-   El orden de los elementos de vértice debe ser el mismo que el orden de los bits FVF.
-   No se permiten espacios en coordenadas de textura.
-   Cualquier elemento de vértice no descrito la tabla no se puede convertir en una FVF válida para todos los controladores previos a DirectX 8 y, por lo tanto, no se puede usar en esos controladores.
-   Solo se permite D3DDECLTYPE FLOAT2 para elementos de vértice con D3DDECLUSAGE TEXCOORD si el dispositivo no establece ninguno de los \_ \_ límites D3DPTEXTURECAPS PROJECTED o \_ D3DPTEXTURECAPS \_ CUBEMAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declaración de vértice](vertex-declaration.md)
</dt> </dl>

 

 



