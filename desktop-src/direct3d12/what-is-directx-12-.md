---
title: Qué es Direct3D 12
description: DirectX 12 presenta la versión siguiente de Direct3D; la API de gráficos 3D en el corazón de DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: b3ff1896372719b011b283e3ff1f5426db9e13d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104352"
---
# <a name="what-is-direct3d-12"></a>¿Qué es Direct3D 12?

DirectX 12 presenta la siguiente versión de Direct3D, &mdash; la API de gráficos 3D en el corazón de DirectX. Direct3D 12 es más rápido y eficaz que cualquier versión anterior. Direct3D 12 permite escenas más enriquecidas, más objetos, efectos más complejos y uso completo del hardware de GPU moderno.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>¿Cómo puede Direct3D 12 ser mucho más rápido y eficaz?

Direct3D 12 es único, ya que proporciona un nivel inferior de abstracción de hardware que las versiones anteriores, lo que permite mejorar significativamente el escalado de CPU de varios núcleos del título (u otra aplicación). Por un lado, con Direct3D 12, el título es responsable de su propia [Administración de memoria](memory-management.md). Además, con Direct3D 12, los títulos y las aplicaciones se benefician de la sobrecarga de GPU reducida a través de características como [colas de comandos y listas](command-queues-and-command-lists.md), [tablas de descriptores](descriptor-tables.md)y [objetos de estado de canalización](managing-graphics-pipeline-state-in-direct3d-12.md)concisos.

Direct3D 12 y Direct3D 11,3 presentan un conjunto de nuevas características para la canalización de representación.

- [Rasterización conservadora](../direct3d11/conservative-rasterization.md) para habilitar la detección de aciertos confiable.
- [Los recursos en mosaico de volumen](../direct3d11/volume-tiled-resources.md) permiten tratar los recursos tridimensionales transmitidos como si estuvieran todos en la memoria de vídeo.
- [Vistas ordenadas por rasterizador](../direct3d11/volume-tiled-resources.md) para habilitar la representación de transparencia confiable.
- Establecer la referencia de la galería de símbolos en un sombreador para habilitar el sombreado especial y otros efectos.
- Asignación de textura mejorada y cargas de vista de acceso no ordenado (UAV) con tipo.

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>¿Con qué profundidad debo invertir en Direct3D 12?

Direct3D 12 proporciona cuatro ventajas principales a los desarrolladores de gráficos (en comparación con Direct3D 11).

- Reducción de la sobrecarga de la CPU.
- Consumo de energía significativamente reducido.
- Hasta aproximadamente un 20% de mejora en la eficiencia de la GPU.
- Desarrollo multiplataforma para un dispositivo Windows 10 (PC, tableta, consola, móvil).

Direct3D 12 está diseñado para que lo usen los programadores de gráficos avanzados. Requiere una gran experiencia de gráficos y un alto nivel de ajuste. Direct3D 12 está diseñado para hacer un uso completo de multithreading, una sincronización cuidadosa de CPU/GPU y la transición y reutilización de los recursos de un propósito a otro. Se trata de técnicas que requieren una cantidad considerable de conocimientos de programación en el nivel de memoria.

Otra ventaja que ofrece Direct3D 12 es su pequeña superficie de API. Hay alrededor de 200 funciones; y aproximadamente un tercio de los mismos hacen todo el trabajo pesado. Esto significa que usted, como desarrollador de gráficos, debe ser capaz de educar &mdash; y dominar &mdash; el conjunto completo de API sin tener que memorizar demasiados nombres de API.

Direct3D 11 sigue siendo una opción viable junto con Direct3D 12. Muchas de las nuevas características de representación de Direct3D 12 están disponibles en [direct3d 11,3](../direct3d11/direct3d-11-3-features.md). Direct3D 11,3 es una API de motor de gráficos de bajo nivel; y Direct3D 12 va incluso más profundo.

Hay al menos dos maneras de que el equipo de desarrollo pueda abordar un título de Direct3D 12.

### <a name="use-direct3d-12-exclusively"></a>Usar Direct3D 12 exclusivamente

En el caso de un proyecto que aproveche al máximo las ventajas de Direct3D 12, debe desarrollar un motor de Direct3D 12 muy personalizado desde cero.

Si, como desarrollador de gráficos, comprende el uso y reutilización de los recursos de los títulos, y puede aprovechar esto minimizando la carga y la copia, podrá desarrollar y personalizar un motor muy eficaz para esos títulos. Las mejoras de rendimiento pueden ser muy considerables, liberar tiempo de CPU para aumentar el número de llamadas a Draw y, por tanto, agregar más clúster a los gráficos.

La inversión en programación es importante, por lo que debe considerar la depuración e instrumentación del proyecto desde el principio. Los errores de procesamiento de subprocesos, sincronización y otros tiempos pueden ser desafiantes.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Usar Direct3D 12 en concierto con Direct3D 11

Un enfoque a corto plazo sería abordar los cuellos de botella conocidos en el título de Direct3D 11. Puede tratarlas mediante las técnicas de [interoperabilidad de Direct3D 12 y/o D3D11On12](direct3d-12-interop.md) , lo que permite que las dos versiones de API funcionen juntas. Este enfoque minimiza los cambios necesarios para un motor de gráficos de Direct3D 11 existente. Sin embargo, las mejoras de rendimiento se limitarán a la liberación del cuello de botella que aborda el código de Direct3D 12.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Vídeos de Microsoft DirectX 12 (y aprendizaje de gráficos)

[Educación mejorada para desarrolladores de gráficos](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA). En estos vídeos se tratan temas como modos de presentación, migración a DirectX 12, rasterización conservadora, herramientas de gráficos, ángulo, Win2D y eventos como GDC, compilación, etc. El contenido técnico de DirectX 12 está precedido de *DirectX 12*. Aquí encontrará sugerencias y trucos directamente del equipo de características de Direct3D 12. Queremos ayudarle a usar nuestras versiones y herramientas más recientes para que el juego sea lo mejor posible.

## <a name="conclusion"></a>Conclusión

Direct3D 12 es todo sobre el rendimiento del motor de gráficos espectacular. La facilidad de desarrollo, las construcciones de alto nivel y la compatibilidad del compilador se han escalado de nuevo para habilitar esto. La compatibilidad con controladores y la facilidad de depuración permanecen en un par con Direct3D 11.

Direct3D 12 es el nuevo territorio. Territorio que está esperando a que el experto en inquisitive se encuentre y explore.
