---
title: Qué es Direct3D 12
description: DirectX 12 presenta la siguiente versión de Direct3D; la API de gráficos 3D en el centro de DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: f82b01ba33cfa6660f266a481b2eaaab20ade236
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359374"
---
# <a name="what-is-direct3d-12"></a>¿Qué es Direct3D 12?

DirectX 12 presenta la siguiente versión de Direct3D, la API de gráficos &mdash; 3D en el núcleo de DirectX. Direct3D 12 es más rápido y eficaz que cualquier versión anterior. Direct3D 12 permite escenas más enriquecciones, más objetos, efectos más complejos y un uso completo del hardware de GPU moderno.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>¿Cómo puede Direct3D 12 ser mucho más rápido y eficaz?

Direct3D 12 es único, ya que proporciona un nivel inferior de abstracción de hardware que las versiones anteriores, lo que permite mejorar significativamente el escalado de CPU de varios núcleos del título (u otra aplicación). Por un lado, con Direct3D 12, el título es responsable de su propia administración [de memoria.](memory-management.md) Además, al usar Direct3D 12, los títulos y las aplicaciones se benefician de una menor sobrecarga de GPU a través de características como colas de comandos y [listas,](command-queues-and-command-lists.md)tablas [descriptoras](descriptor-tables.md)y objetos de estado de canalización concisos. [](managing-graphics-pipeline-state-in-direct3d-12.md)

Direct3D 12 y Direct3D 11.3 presentan un conjunto de nuevas características para la canalización de representación.

- [Rasterización conservadora para](../direct3d11/conservative-rasterization.md) habilitar la detección de acceso confiable.
- [Recursos en mosaico de](../direct3d11/volume-tiled-resources.md) volumen para permitir que los recursos tridimensionales transmitidos se traten como si estuvieran todos en la memoria de vídeo.
- [Vistas ordenadas por rasterizador para](../direct3d11/rasterizer-order-views.md) habilitar la representación de transparencia confiable.
- Establecer la referencia de galería de símbolos dentro de un sombreador para habilitar el sombreado especial y otros efectos.
- Asignación de textura mejorada y cargas de vista de acceso sin ordenar (UAV) con tipo.

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>¿En qué profundidad debo invertir en Direct3D 12?

Direct3D 12 proporciona cuatro ventajas principales para los desarrolladores de gráficos (en comparación con Direct3D 11).

- Sobrecarga de CPU muy reducida.
- Consumo de energía significativamente reducido.
- Mejora de hasta (aproximadamente) un 20 % en la eficiencia de GPU.
- Desarrollo multiplataforma para un Windows 10 (PC, tableta, consola, móvil).

Direct3D 12 está diseñado para que lo usen programadores avanzados de gráficos. Requiere una gran experiencia en gráficos y un alto nivel de ajuste. Direct3D 12 está diseñado para hacer un uso completo de multiproceso, una cuidadosa sincronización de CPU/GPU y la transición y el nuevo uso de recursos de un propósito a otro. Se trata de técnicas que requieren una cantidad considerable de aptitudes de programación de nivel de memoria.

Otra ventaja que tiene Direct3D 12 es su pequeña superficie de API. Hay alrededor de 200 funciones; y aproximadamente un tercio de ellos hacen todo el trabajo pesado. Esto significa que usted, como desarrollador de gráficos, debe ser capaz de formar y dominar el conjunto de API completo sin tener que memoriar demasiados nombres &mdash; &mdash; de API.

Direct3D 11 sigue siendo una opción viable junto con Direct3D 12. Muchas de las nuevas características de representación de Direct3D 12 están disponibles en [Direct3D 11.3.](../direct3d11/direct3d-11-3-features.md) Direct3D 11.3 es una API de motor de gráficos de bajo nivel; y Direct3D 12 son aún más profundos.

Hay al menos dos maneras de que el equipo de desarrollo pueda abordar un título de Direct3D 12.

### <a name="use-direct3d-12-exclusively"></a>Uso exclusivo de Direct3D 12

Para un proyecto que aproveche al máximo todas las ventajas de Direct3D 12, debe desarrollar un motor de Direct3D 12 muy personalizado desde cero.

Si, como desarrollador de gráficos, comprende el uso y el uso de recursos dentro de los títulos, y puede aprovecharlo minimizando la carga y copia, puede desarrollar y personalizar un motor muy eficaz para esos títulos. Las mejoras de rendimiento pueden ser muy considerables, lo que libera tiempo de CPU para aumentar el número de llamadas a draw y, por tanto, agrega más luster a los gráficos.

La inversión en programación es significativa y debe considerar la depuración y la instrumentación del proyecto desde el principio. El subproceso, la sincronización y otros errores de control de tiempo pueden ser complicados.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Uso de Direct3D 12 junto con Direct3D 11

Un enfoque a corto plazo sería abordar cuellos de botella conocidos en el título de Direct3D 11. Puede solucionar esos problemas mediante técnicas de interoperabilidad de [Direct3D 12 o D3D11On12,](direct3d-12-interop.md) que permiten que las dos versiones de API funcionen juntas. Este enfoque minimiza los cambios necesarios en un motor de gráficos existente de Direct3D 11. Sin embargo, las mejoras de rendimiento se limitarán al resalte del cuello de botella que aborda el código de Direct3D 12.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Vídeos de Microsoft DirectX 12 (y educación de gráficos)

[Educación mejorada para desarrolladores de gráficos.](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA) En estos vídeos se tratan temas como modos de presentación, porte a DirectX 12, rasterización conservadora, herramientas de gráficos, Angle, Win2D y eventos como GDC, Build, etc. El contenido técnico de DirectX 12 está precedido de *DirectX 12.* Ven aquí para obtener sugerencias y trucos directamente del equipo de características de Direct3D 12. Queremos ayudarle a usar nuestras últimas versiones y herramientas para que el juego sea lo mejor posible.

## <a name="conclusion"></a>Conclusión

Direct3D 12 trata sobre el rendimiento del motor gráfico drástico. La facilidad de desarrollo, las construcciones de alto nivel y la compatibilidad con el compilador se han escalado de nuevo para habilitar esto. La compatibilidad con controladores y la facilidad de depuración permanecen a la par que Direct3D 11.

Direct3D 12 es un nuevo territorio. Territorio que está esperando a que el experto inquisitivo se encuentre y explore.
