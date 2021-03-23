---
title: Guía de programación de Direct3D 12
description: Direct3D 12 proporciona una API y una plataforma que permite a las aplicaciones aprovechar las ventajas de los gráficos y las capacidades de computación de los equipos equipados con una o varias GPU compatibles con Direct3D 12.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 94afd9125a2e73665e3783419651f34fd72285ca
ms.sourcegitcommit: bf6a52b91604d8a9432bf646097e3f31e44967d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/06/2019
ms.locfileid: "104549164"
---
# <a name="direct3d-12-programming-guide"></a>Guía de programación de Direct3D 12

Direct3D 12 proporciona una API y una plataforma que permite a las aplicaciones aprovechar las ventajas de los gráficos y las capacidades de computación de los equipos equipados con una o varias GPU compatibles con Direct3D 12.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [¿Qué es Direct3D 12?](what-is-directx-12-.md) | DirectX 12 presenta la siguiente versión de Direct3D, la API de gráficos 3D en el corazón de DirectX. Esta versión de Direct3D es más rápida y eficaz que cualquier versión anterior. Direct3D 12 permite escenas más enriquecidas, más objetos, efectos más complejos y uso completo del hardware de GPU moderno.  |
| [Novedades de Direct3D 12](new-releases.md) | Describe la nueva documentación más importante disponible con la versión más reciente del SDK. |
| [Descripción de Direct3D 12](directx-12-getting-started.md) | Para escribir juegos y aplicaciones 3D para Windows 10 y Windows 10 Mobile, debe comprender los aspectos básicos de la tecnología Direct3D 12 y cómo prepararse para usarlos en sus juegos y aplicaciones. |
| [Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md) | Para mejorar la eficacia de la CPU de las aplicaciones Direct3D, Direct3D 12 ya no admite un contexto inmediato asociado a un dispositivo. En su lugar, las aplicaciones registran y envían *listas de comandos*, que contienen llamadas de administración de dibujos y recursos. Estas listas de comandos se pueden enviar desde varios subprocesos a una o varias colas de comandos, que administran la ejecución de los comandos. Este cambio fundamental aumenta la eficacia de un solo subproceso, ya que permite a las aplicaciones calcular previamente el trabajo de representación para su reutilización posterior y aprovecha los sistemas de varios núcleos mediante la propagación del trabajo de representación entre varios subprocesos.  |
| [Enlace de recursos en Direct3D 12](resource-binding.md) | El enlace es el proceso de vinculación de objetos de recursos a los sombreadores de la canalización de gráficos.  |
| [Administración de la memoria en Direct3D 12](memory-management.md) | Pasar a D3D12 implica realizar la sincronización y administración adecuadas de la residencia de memoria. La administración de la residencia de memoria significa que se debe realizar aún más sincronización. En esta sección se tratan las estrategias de administración de memoria y la subasignación en montones y búferes.  |
| [Sistemas de varios adaptadores](multi-engine.md) | Describe la compatibilidad en Direct3D 12 para sistemas que tienen instalados varios adaptadores, que abarcan escenarios en los que la aplicación tiene como destino explícitamente varios adaptadores de GPU y escenarios en los que los controladores usan implícitamente varios adaptadores de GPU en nombre de la aplicación. |
| [Sincronización de varios motores](user-mode-heap-synchronization.md) | En este tema se describe la sincronización del acceso a varios motores independientes que se encuentran en la mayoría de las GPU modernas. |
| [Representación](rendering.md) | Esta sección contiene información sobre las características de representación nuevas de Direct3D 12 (y Direct3D 11,3). |
| [Contadores, consultas y medición de rendimiento](performance-measurement.md) | En las secciones siguientes se describen las características que se usan en las pruebas y mejoras de rendimiento, como consultas, contadores, temporización y predication. |
| [Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md) | En esta sección se describen las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API 11on12 de Direct3D y las instrucciones de portabilidad de Direct3D 11 a Direct3D 12. |
| [Ejemplos de trabajo](working-samples.md) | Los ejemplos de trabajo están disponibles para su descarga, mostrando el uso de una serie de características de Direct3D 12. |
| [Tutoriales de código D3D12](d3d12-code-walk-throughs.md) | En esta sección se proporciona código para escenarios de ejemplo. Muchos de los tutoriales proporcionan detalles sobre qué codificación se debe agregar a un ejemplo básico, para evitar repetir el código de componente básico para cada escenario. |
| [Depuración y diagnóstico con Direct3D 12](understanding-the-d3d12-debug-layer.md) | Incluye temas en los que se describe cómo hacer el mejor uso de la capa de depuración de Direct3D 12 con validación basada en GPU (GBV) y cómo usar los datos extendidos quitados del dispositivo (DRED). |

## <a name="related-topics"></a>Temas relacionados

* [Gráficos de Direct3D 12](direct3d-12-graphics.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
* [Tutoriales de vídeo de aprendizaje avanzado de DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
