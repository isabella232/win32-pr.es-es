---
title: Acceso de canalización a recursos en mosaico
description: Los recursos en mosaico se pueden usar en las vistas de recursos del sombreador (SRV), las vistas de destino de representación (RTV), las vistas de estarcido de profundidad (DSV) y las vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como los enlaces de búfer de vértices.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793090"
---
# <a name="pipeline-access-to-tiled-resources"></a>Acceso de canalización a recursos en mosaico

Los recursos en mosaico se pueden usar en las vistas de recursos del sombreador (SRV), las vistas de destino de representación (RTV), las vistas de estarcido de profundidad (DSV) y las vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como los enlaces de búfer de vértices. Para obtener la lista de enlaces admitidos, consulte [parámetros de creación de recursos en mosaico](tiled-resource-creation-parameters.md). \*Las operaciones de copia también funcionan en recursos en mosaico.

Si varias coordenadas del mosaico de una o varias vistas están enlazadas a la misma ubicación de memoria, las lecturas y escrituras de diferentes rutas de acceso a la misma memoria se producirán en un orden no determinista y no repetible de accesos a la memoria.

Si todos los mosaicos detrás de una superficie de acceso a memoria desde un sombreador se asignan a mosaicos únicos, el comportamiento es idéntico en todas las implementaciones a la superficie que tiene el mismo contenido de memoria en un modo no mosaico.

En esta sección se proporciona más información sobre el acceso de canalización a los recursos en mosaico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                              | Descripción                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comportamiento SRV con iconos sin asignar](srv-behavior-with-non-mapped-tiles.md)<br/>                            | El comportamiento de las lecturas de vista de recursos del sombreador (SRV) que impliquen mosaicos no asignados depende del nivel de compatibilidad de hardware. <br/>                                          |
| [Comportamiento UAV con iconos sin asignar](uav-behavior-with-non-mapped-tiles.md)<br/>                            | El comportamiento de las lecturas y escrituras de la vista de acceso desordenado (UAV) depende del nivel de compatibilidad de hardware. <br/>                                                            |
| [Comportamiento de rasterizador con iconos sin asignar](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | En esta sección se describe el comportamiento de rasterizador con mosaicos no asignados.<br/>                                                                                              |
| [Limitaciones de acceso de iconos con asignaciones duplicadas](tile-access-limitations-with-duplicate-mappings-.md)<br/> | En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.<br/>                                                                                        |
| [Características de muestreo de textura de recursos en mosaico](tiled-resources-texture-sampling-features.md)<br/>              | En esta sección se describen las características de muestreo de textura de recursos en mosaico.<br/>                                                                                              |
| [Exposición de recursos en mosaico de HLSL](hlsl-tiled-resources-exposure.md)<br/>                                      | Se requiere una nueva sintaxis de lenguaje de sombreado de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en el [modelo de sombreador 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5). <br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

