---
title: Representación (gráficos de Direct3D 12)
description: Esta sección contiene información sobre las características de representación nuevas de Direct3D 12 (y Direct3D 11.3).
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ad70a054881e9472ff27a76a62dca62fdf3653
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072894"
---
# <a name="rendering-direct3d-12-graphics"></a>Representación (gráficos de Direct3D 12)

Esta sección contiene información sobre las características de representación nuevas de Direct3D 12 (y Direct3D 11.3).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterización conservadora](conservative-rasterization.md)<br/>                             | La rasterización conservadora agrega cierta certeza a la representación de píxeles, lo que resulta útil en particular para los algoritmos de detección de colisiones.<br/>                                                                                                                                                                                                                                              |
| [Dibujo indirecto](indirect-drawing.md)<br/>                                                 | El dibujo indirecto permite mover parte del recorrido de la escena y la selección de la CPU a la GPU, lo que puede mejorar el rendimiento. La CPU o la GPU pueden generar el búfer de comandos.<br/>                                                                                                                                                                                              |
| [Vistas ordenadas por el rasterizador](rasterizer-order-views.md)<br/>                                   | Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque los enlaces UAV con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV. Esto permite que funcionen los algoritmos de transparencia independiente de pedidos (RSA), que dan resultados de representación mucho mejores cuando varios objetos transparentes están en línea entre sí en una vista. <br/> |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md)<br/> | La habilitación de sombreadores de píxeles para generar el valor de referencia de galería de símbolos, en lugar de usar el especificado por la API, permite un control muy específico sobre las operaciones de galería de símbolos.<br/>                                                                                                                                                                                                              |
| [Cadenas de intercambio](swap-chains.md)<br/>                                                           | Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación de gráficos.<br/>                                                                                                                                                                                                                                                                                            |



 

Los temas siguientes también son nuevos para Direct3D 12 y Direct3D 11.3:

-   [Asignación de textura predeterminada](default-texture-mapping.md)
-   [Cargas de vista de acceso sin ordenar con tipo](typed-unordered-access-view-loads.md)
-   [Recursos en mosaico de volumen](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Alto rango dinámico y gama de colores anchos

Consulte la compatibilidad con Alto rango dinámico (mayor diferencia entre los colores más claros y los más oscuros) y Wide Color Gamut (10 bits, en lugar de 8 bits, por color) que se describe en [Mejoras de DXGI 1.5.](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

