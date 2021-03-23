---
title: Representación (gráficos de Direct3D 12)
description: Esta sección contiene información sobre las características de representación nuevas de Direct3D 12 (y Direct3D 11,3).
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ad70a054881e9472ff27a76a62dca62fdf3653
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104549148"
---
# <a name="rendering-direct3d-12-graphics"></a>Representación (gráficos de Direct3D 12)

Esta sección contiene información sobre las características de representación nuevas de Direct3D 12 (y Direct3D 11,3).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterización conservadora](conservative-rasterization.md)<br/>                             | La rasterización conservadora agrega cierta certeza a la representación en píxeles, lo que resulta útil en especial a los algoritmos de detección de colisiones.<br/>                                                                                                                                                                                                                                              |
| [Dibujo indirecto](indirect-drawing.md)<br/>                                                 | El dibujo indirecto permite que algunos recorridos de escena y selección de ubicación se muevan de la CPU a la GPU, lo que puede mejorar el rendimiento. La CPU o la GPU pueden generar el búfer de comandos.<br/>                                                                                                                                                                                              |
| [Vistas ordenadas de rasterizador](rasterizer-order-views.md)<br/>                                   | Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs. Esto permite que funcionen los algoritmos de transparencia independiente de orden (OIT), que proporcionan resultados de representación mucho mejores cuando varios objetos transparentes están alineados entre sí en una vista. <br/> |
| [Valor de referencia de estarcido del sombreador especificado](shader-specified-stencil-reference-value.md)<br/> | Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.<br/>                                                                                                                                                                                                              |
| [Cadenas de intercambio](swap-chains.md)<br/>                                                           | Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación de gráficos.<br/>                                                                                                                                                                                                                                                                                            |



 

Los temas siguientes también son nuevos en Direct3D 12 y Direct3D 11,3:

-   [Asignación de textura predeterminada](default-texture-mapping.md)
-   [Cargas de vista de acceso no ordenada con tipo](typed-unordered-access-view-loads.md)
-   [Recursos en mosaico de volumen](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Gama de colores alto y ancho dinámico

Consulte la compatibilidad con un intervalo dinámico alto (mayor diferencia entre los blancos más brillantes y los negros más oscuros) y la gama de colores anchos (10 bits, en lugar de 8 bits, por color) descritas en las [mejoras de DXGI 1,5](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

