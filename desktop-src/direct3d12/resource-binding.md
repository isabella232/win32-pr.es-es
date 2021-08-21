---
title: Enlace de recursos
description: El enlace es el proceso de vincular objetos de recursos a los sombreadores de la canalización de gráficos.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93ca7fb75e65c58aee2b2dffbb220830e2911f2c8d7ce9186a09926fa11373f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912249"
---
# <a name="resource-binding"></a>Enlace de recursos

El enlace es el proceso de vincular objetos de recursos a los sombreadores de la canalización de gráficos.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Información general sobre el enlace de recursos](resource-binding-flow-of-control.md) | La clave para el enlace de recursos en DirectX 12 son los conceptos de un *descriptor*, tablas *de descriptores,* montones de *descriptores* y una *firma raíz*. |
| [Diferencias en el modelo de enlace de Direct3D 11](binding-model.md) | Una de las principales decisiones de diseño detrás del enlace de DirectX12 es separarlo de otras tareas de administración. Esto coloca algunos requisitos en la aplicación para administrar determinados riesgos potenciales. |
| [Descriptores de](descriptors.md) | Los descriptores son la unidad principal de enlace para un único recurso en D3D12. |
| [Montones de descriptores](descriptor-heaps.md) | Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor. |
| [Tablas de descriptores](descriptor-tables.md) | Una tabla de descriptores es lógicamente una matriz de descriptores. |
| [Firmas raíz](root-signatures.md) | La firma raíz define qué tipos de recursos están enlazados a la canalización de gráficos. |
| [Consulta de funcionalidades](capability-querying.md) | La aplicación puede detectar el nivel de compatibilidad con el enlace de recursos y muchas otras características, con una llamada a [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). |
| [Enlace de recursos en HLSL](resource-binding-in-hlsl.md) | En este tema se describen algunas características específicas del uso del modelo de sombreador hlsl (lenguaje de sombreador de alto nivel) [5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) con Direct3D 12. Todo el hardware de Direct3D 12 admite El modelo de sombreador 5.1, por lo que la compatibilidad con este modelo no depende del nivel de característica de hardware. |
| [Optimizaciones de UMA: texturas accesibles por CPU y referencias estándar](default-texture-mapping.md) | Las GPU de arquitectura de memoria universal (UMA) ofrecen algunas ventajas de eficiencia con respecto a las GPU discretas, especialmente cuando se optimizan para dispositivos móviles. Proporcionar a los recursos acceso a la CPU cuando la GPU es UMA puede reducir la cantidad de copia que se produce entre la CPU y la GPU. Aunque no se recomienda que las aplicaciones den acceso a la CPU a todos los recursos de los diseños de UMA, hay oportunidades para mejorar la eficacia al proporcionar a los recursos adecuados acceso a la CPU. A diferencia de las GPU discretas, la CPU puede tener técnicamente un puntero a todos los recursos a los que la GPU puede acceder. |
| [Cargas de la vista de acceso sin ordenar con tipo](typed-unordered-access-view-loads.md) | La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad de un sombreador de leer desde un UAV con un [**FORMATO DXGI \_ específico.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) |
| [Recursos en mosaico de volumen](volume-tiled-resources.md) | Las texturas de volumen (3D) se pueden usar como recursos en mosaico, y se debe tener en cuenta que la resolución de mosaicos es tridimensional. |
| [Subrecursos](subresources.md) | Describe cómo un recurso se divide en subcursos y cómo hacer referencia a un único, varios o segmentos de subrecursos. |

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación de Direct3D 12](directx-12-programming-guide.md)
* [Tutoriales de vídeo de aprendizaje avanzado de DirectX: Enlace de recursos en DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Administración de memoria](memory-management.md)