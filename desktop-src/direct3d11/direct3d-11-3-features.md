---
title: Características de Direct3D 11,3
description: En las secciones siguientes se describe la funcionalidad que se ha agregado en Direct3D 11,3. Estas características también están disponibles en Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421658"
---
# <a name="direct3d-113-features"></a>Características de Direct3D 11,3

En las secciones siguientes se describe la funcionalidad que se ha agregado en Direct3D 11,3. Estas características también están disponibles en Direct3D 12.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterización conservadora](conservative-rasterization.md)<br/>                             | La rasterización conservadora agrega cierta certeza a la representación en píxeles, lo que resulta útil en especial a los algoritmos de detección de colisiones.<br/>                                                                                                                                                                                                                                              |
| [Asignación de textura predeterminada](default-texture-mapping.md)<br/>                                   | El uso de la asignación de texturas predeterminada reduce la copia y el uso de memoria mientras se comparten datos de imagen entre la GPU y la CPU. Sin embargo, solo se debe usar en situaciones específicas. El diseño de swizzle estándar evita copiar o permutación datos en varios diseños.<br/>                                                                                                               |
| [Vistas de orden de rasterizador](rasterizer-order-views.md)<br/>                                     | Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs. Esto permite que funcionen los algoritmos de transparencia independiente de orden (OIT), que proporcionan resultados de representación mucho mejores cuando varios objetos transparentes están alineados entre sí en una vista. <br/> |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md)<br/> | Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.<br/>                                                                                                                                                                                                              |
| [Cargas de vista de acceso no ordenada con tipo](typed-unordered-access-view-loads.md)<br/>               | La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con un formato de DXGI específico \_ .<br/>                                                                                                                                                                                                                                                               |
| [Arquitectura de memoria unificada](unified-memory-architecture.md)<br/>                           | La consulta de si se admite la arquitectura de memoria unificada (UMA) puede ayudar a determinar cómo administrar algunos recursos.<br/>                                                                                                                                                                                                                                                              |
| [Recursos en mosaico de volumen](volume-tiled-resources.md)<br/>                                     | Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





