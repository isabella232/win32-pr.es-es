---
title: Características de Direct3D 11.3
description: En las secciones siguientes se describe la funcionalidad que se ha agregado en Direct3D 11.3. Estas características también están disponibles en Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bfdead81de43cbe0391b661f450db0acfa402417148ed1d1731e4a22f05f1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099247"
---
# <a name="direct3d-113-features"></a>Características de Direct3D 11.3

En las secciones siguientes se describe la funcionalidad que se ha agregado en Direct3D 11.3. Estas características también están disponibles en Direct3D 12.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterización conservadora](conservative-rasterization.md)<br/>                             | La rasterización conservadora agrega cierta certeza a la representación de píxeles, lo que resulta útil en particular para los algoritmos de detección de colisiones.<br/>                                                                                                                                                                                                                                              |
| [Asignación de textura predeterminada](default-texture-mapping.md)<br/>                                   | El uso de la asignación de texturas predeterminada reduce el uso de la copia y la memoria al compartir datos de imagen entre la GPU y la CPU. Sin embargo, solo se debe usar en situaciones específicas. El diseño swzzle estándar evita copiar o deslizar datos en varios diseños.<br/>                                                                                                               |
| [Vistas de orden de rasterizador](rasterizer-order-views.md)<br/>                                     | Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque los enlaces UAV con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV. Esto permite que funcionen los algoritmos de transparencia independiente del orden (RSA), que dan resultados de representación mucho mejores cuando varios objetos transparentes están en línea entre sí en una vista. <br/> |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md)<br/> | La habilitación de sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control muy granular sobre las operaciones de galería de símbolos.<br/>                                                                                                                                                                                                              |
| [Cargas de la vista de acceso sin ordenar con tipo](typed-unordered-access-view-loads.md)<br/>               | La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad de un sombreador de leer desde un UAV con un FORMATO DXGI \_ específico.<br/>                                                                                                                                                                                                                                                               |
| [Arquitectura de memoria unificada](unified-memory-architecture.md)<br/>                           | Consultar si se admite la arquitectura de memoria unificada (UMA) puede ayudar a determinar cómo controlar algunos recursos.<br/>                                                                                                                                                                                                                                                              |
| [Recursos en mosaico de volumen](volume-tiled-resources.md)<br/>                                     | Las texturas de volumen (3D) se pueden usar como recursos en mosaico, y se debe tener en cuenta que la resolución de mosaicos es tridimensional.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





