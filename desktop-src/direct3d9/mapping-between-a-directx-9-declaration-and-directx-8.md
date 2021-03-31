---
title: Asignación entre declaraciones de D3D9 y D3D8
description: En esta tabla se asignan miembros de una declaración de D3DVERTEXELEMENT9 a una declaración de Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805312"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Asignación entre declaraciones de D3D9 y D3D8

En esta tabla se asignan miembros de una declaración de [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) a una declaración de Direct3D 8.



| Uso de Direct3D 9           | Índice de uso de Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| \_Posición D3DDECLUSAGE     | 0                      | \_Posición D3DVSDE     |
| \_Posición D3DDECLUSAGE     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ normal       | 0                      | D3DVSDE \_ normal       |
| D3DDECLUSAGE \_ normal       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ PSIZE        | 0                      | D3DVSDE \_ PSIZE        |
| COLOR de D3DDECLUSAGE \_        | 0                      | \_Difusión D3DVSDE      |
| COLOR de D3DDECLUSAGE \_        | 1                      | \_Reflejo D3DVSDE     |
| D3DDECLUSAGE \_ TEXCOORD     | n                      | D3DVSDE \_ TEXCOORDn    |



 

Cuando se usa una declaración con el procesamiento de vértices de hardware en un controlador de Direct3D 7, el tiempo de ejecución de Direct3D lo convierte en un FVF con las siguientes reglas:

-   Solo se debe usar Stream 0 (evidente desde el extremo MaxStreams).
-   El orden de los elementos de vértice debe ser el mismo que el orden de los bits de FVF.
-   No se permiten espacios en las coordenadas de textura.
-   Cualquier elemento de vértice no descrito en la tabla no se puede convertir en un FVF válido para todos los controladores anteriores a DirectX 8 y, por lo tanto, no se puede usar en esos controladores.
-   Solo \_ se permite D3DDECLTYPE FLOAT2 para los elementos de vértice con D3DDECLUSAGE \_ TEXCOORD si el dispositivo no establece ninguno de los límites de D3DPTEXTURECAPS \_ previsto o D3DPTEXTURECAPS \_ mapa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declaración de vértice](vertex-declaration.md)
</dt> </dl>

 

 



