---
title: Guía de programación de Direct3D 12
description: Direct3D 12 proporciona una API y una plataforma que permiten a las aplicaciones aprovechar las funcionalidades de gráficos y computación de equipos equipados con una o varias GPU compatibles con Direct3D 12.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: c7dfaf55b44da4a05616db7b7f64c262a3c5b6920ab2c0665e1196d70b539215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045493"
---
# <a name="direct3d-12-programming-guide"></a>Guía de programación de Direct3D 12

Direct3D 12 proporciona una API y una plataforma que permiten a las aplicaciones aprovechar las funcionalidades de gráficos y computación de equipos equipados con una o varias GPU compatibles con Direct3D 12.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [¿Qué es Direct3D 12?](what-is-directx-12-.md) | DirectX 12 presenta la siguiente versión de Direct3D, la API de gráficos 3D en el núcleo de DirectX. Esta versión de Direct3D es más rápida y eficaz que cualquier versión anterior. Direct3D 12 permite escenas más enriquecciones, más objetos, efectos más complejos y un uso completo del hardware de GPU moderno.  |
| [Novedades de Direct3D 12](new-releases.md) | Describe la documentación nueva más importante disponible con la versión más reciente del SDK. |
| [Descripción de Direct3D 12](directx-12-getting-started.md) | Para escribir juegos y aplicaciones en 3D para Windows 10 y Windows 10 Mobile, debe comprender los conceptos básicos de la tecnología Direct3D 12 y cómo prepararse para usarlo en sus juegos y aplicaciones. |
| [Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md) | Para mejorar la eficacia de la CPU de las aplicaciones de Direct3D, Direct3D 12 ya no admite un contexto inmediato asociado a un dispositivo. En su lugar, las aplicaciones registran y envían listas *de comandos*, que contienen llamadas de administración de recursos y dibujos. Estas listas de comandos se pueden enviar desde varios subprocesos a una o varias colas de comandos, que administran la ejecución de los comandos. Este cambio fundamental aumenta la eficacia de un solo subproceso al permitir que las aplicaciones preprocesen el trabajo de representación para su posterior uso, y aprovecha las ventajas de los sistemas de varios núcleos al distribuir el trabajo de representación entre varios subprocesos.  |
| [Enlace de recursos en Direct3D 12](resource-binding.md) | El enlace es el proceso de vincular objetos de recursos a los sombreadores de la canalización de gráficos.  |
| [Administración de memoria en Direct3D 12](memory-management.md) | El traslado a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria. La administración de la residencia de memoria significa que se debe realizar aún más sincronización. En esta sección se tratan las estrategias de administración de memoria y la suballocation dentro de montones y búferes.  |
| [Sistemas de varios adaptadores](multi-engine.md) | Describe la compatibilidad de Direct3D 12 con sistemas que tienen varios adaptadores instalados, que abarca escenarios en los que la aplicación tiene como destino explícitamente varios adaptadores de GPU y escenarios en los que los controladores usan implícitamente varios adaptadores de GPU en nombre de la aplicación. |
| [Sincronización de varios motores](user-mode-heap-synchronization.md) | En este tema se describe la sincronización del acceso a los varios motores independientes que se encuentran en las GPU más modernas. |
| [Representación](rendering.md) | Esta sección contiene información sobre las características de representación nuevas de Direct3D 12 (y Direct3D 11.3). |
| [Contadores, consultas y medidas de rendimiento](performance-measurement.md) | En las secciones siguientes se describen las características que se usan en las pruebas de rendimiento y la mejora, como consultas, contadores, control de tiempo y predicado. |
| [Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md) | En esta sección se tratan las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API Direct3D 11on12 y las directrices de porte de Direct3D 11 a Direct3D 12. |
| [Ejemplos de trabajo](working-samples.md) | Hay ejemplos de trabajo disponibles para su descarga, que muestran el uso de una serie de características de Direct3D 12. |
| [Recorridos del código D3D12](d3d12-code-walk-throughs.md) | En esta sección se proporciona código para escenarios de ejemplo. Muchos de los recorridos proporcionan detalles sobre qué codificación es necesario agregar a un ejemplo básico, para evitar repetir el código de componente básico para cada escenario. |
| [Depuración y diagnóstico con Direct3D 12](understanding-the-d3d12-debug-layer.md) | Incluye temas que describen cómo usar mejor la capa de depuración de Direct3D 12 con validación basada en GPU (GBV) y cómo usar datos extendidos eliminados por dispositivos (DRED). |

## <a name="related-topics"></a>Temas relacionados

* [Gráficos de Direct3D 12](direct3d-12-graphics.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
* [Tutoriales de vídeo de aprendizaje avanzado de DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
