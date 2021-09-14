---
title: Acceso de canalización a recursos en mosaico
description: Los recursos en mosaico se pueden usar en vistas de recursos de sombreador (SRV), representar vistas de destino (RTV), vistas de galería de símbolos de profundidad (DSV) y vistas de acceso no ordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como enlaces de búfer de vértice.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060812"
---
# <a name="pipeline-access-to-tiled-resources"></a>Acceso de canalización a recursos en mosaico

Los recursos en mosaico se pueden usar en vistas de recursos de sombreador (SRV), representar vistas de destino (RTV), vistas de galería de símbolos de profundidad (DSV) y vistas de acceso no ordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como enlaces de búfer de vértice. Para obtener la lista de enlaces admitidos, consulte [Parámetros de creación de recursos en mosaico.](tiled-resource-creation-parameters.md) Las operaciones \* de copia también funcionan en recursos en mosaico.

Si varias coordenadas de mosaico de una o varias vistas están enlazadas a la misma ubicación de memoria, las lecturas y escrituras de rutas de acceso diferentes a la misma memoria se producirán en un orden no determinista y no repetible de accesos a memoria.

Si todos los iconos detrás de una superficie de acceso a memoria de un sombreador se asignan a iconos únicos, el comportamiento es idéntico en todas las implementaciones a la superficie que tiene el mismo contenido de memoria en un modo sin mosaico.

En esta sección se proporciona más información sobre el acceso de canalización a los recursos en mosaico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                              | Descripción                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comportamiento SRV con iconos sin asignar](srv-behavior-with-non-mapped-tiles.md)<br/>                            | El comportamiento de las lecturas de vista de recursos de sombreador (SRV) que implican iconos no asignados depende del nivel de compatibilidad de hardware. <br/>                                          |
| [Comportamiento UAV con iconos sin asignar](uav-behavior-with-non-mapped-tiles.md)<br/>                            | El comportamiento de las lecturas y escrituras de la vista de acceso no ordenado (UAV) depende del nivel de compatibilidad con hardware. <br/>                                                            |
| [Comportamiento de rasterizador con iconos sin asignar](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | En esta sección se describe el comportamiento del rasterizador con iconos no asignados.<br/>                                                                                              |
| [Limitaciones de acceso de iconos con asignaciones duplicadas](tile-access-limitations-with-duplicate-mappings-.md)<br/> | En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.<br/>                                                                                        |
| [Características de muestreo de textura de recursos en mosaico](tiled-resources-texture-sampling-features.md)<br/>              | En esta sección se describen las características de muestreo de textura de recursos en mosaico.<br/>                                                                                              |
| [Exposición de recursos en mosaico HLSL](hlsl-tiled-resources-exposure.md)<br/>                                      | Se requiere una nueva sintaxis del Lenguaje de sombreador de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en [el modelo 5 de sombreador.](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5) <br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

