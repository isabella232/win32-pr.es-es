---
title: Acceso de canalización a recursos en mosaico
description: Los recursos en mosaico se pueden usar en vistas de recursos de sombreador (SRV), vistas de destino de representación (RTV), vistas de galería de símbolos de profundidad (DSV) y vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como enlaces de búfer de vértices.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a8e4656247a1ad59d053ea9871314f9370ff00930cf24a452e363775101f58d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119375825"
---
# <a name="pipeline-access-to-tiled-resources"></a>Acceso de canalización a recursos en mosaico

Los recursos en mosaico se pueden usar en vistas de recursos de sombreador (SRV), vistas de destino de representación (RTV), vistas de galería de símbolos de profundidad (DSV) y vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como enlaces de búfer de vértices. Para obtener la lista de enlaces admitidos, vea [Parámetros de creación de recursos en mosaico.](tiled-resource-creation-parameters.md) Las operaciones \* de copia también funcionan en recursos en mosaico.

Si varias coordenadas de mosaico de una o varias vistas están enlazadas a la misma ubicación de memoria, las lecturas y escrituras de distintas rutas de acceso a la misma memoria se producirán en un orden no determinista y no repetible de accesos a memoria.

Si todos los iconos detrás de una superficie de acceso a memoria de un sombreador se asignan a iconos únicos, el comportamiento es idéntico en todas las implementaciones a la superficie que tiene el mismo contenido de memoria en un modo no en mosaico.

En esta sección se proporciona más información sobre el acceso de canalización a los recursos en mosaico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                              | Descripción                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comportamiento SRV con iconos sin asignar](srv-behavior-with-non-mapped-tiles.md)<br/>                            | El comportamiento de las lecturas de la vista de recursos de sombreador (SRV) que implican iconos no asignados depende del nivel de compatibilidad de hardware. <br/>                                          |
| [Comportamiento UAV con iconos sin asignar](uav-behavior-with-non-mapped-tiles.md)<br/>                            | El comportamiento de las lecturas y escrituras de la vista de acceso no ordenado (UAV) depende del nivel de compatibilidad con hardware. <br/>                                                            |
| [Comportamiento de rasterizador con iconos sin asignar](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | En esta sección se describe el comportamiento del rasterizador con iconos no asignados.<br/>                                                                                              |
| [Limitaciones de acceso de iconos con asignaciones duplicadas](tile-access-limitations-with-duplicate-mappings-.md)<br/> | En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.<br/>                                                                                        |
| [Características de muestreo de textura de recursos en mosaico](tiled-resources-texture-sampling-features.md)<br/>              | En esta sección se describen las características de muestreo de textura de recursos en mosaico.<br/>                                                                                              |
| [Exposición de recursos en mosaico hlsl](hlsl-tiled-resources-exposure.md)<br/>                                      | Se requiere una nueva sintaxis de Lenguaje de sombreador de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en [el modelo de sombreador 5.](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5) <br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

