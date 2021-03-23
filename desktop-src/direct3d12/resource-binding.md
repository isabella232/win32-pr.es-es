---
title: Enlace de recursos
description: El enlace es el proceso de vinculación de objetos de recursos a los sombreadores de la canalización de gráficos.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086a14beec32447cb91e2a345f4fecda8d5480fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549141"
---
# <a name="resource-binding"></a>Enlace de recursos

El enlace es el proceso de vinculación de objetos de recursos a los sombreadores de la canalización de gráficos.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Información general sobre el enlace de recursos](resource-binding-flow-of-control.md) | La clave para el enlace de recursos en DirectX 12 son los conceptos de un *descriptor*, *las tablas de descriptores*, los *montones de descriptores* y una *firma raíz*. |
| [Diferencias en el modelo de enlace de Direct3D 11](binding-model.md) | Una de las decisiones de diseño principales detrás del enlace de DirectX12 es separarlo de otras tareas de administración. Esto pone algunos requisitos en la aplicación para administrar ciertos peligros potenciales. |
| [Descriptores de](descriptors.md) | Los descriptores son la unidad principal de enlace para un único recurso de D3D12. |
| [Montones de descriptores](descriptor-heaps.md) | Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor. |
| [Tablas de descriptores](descriptor-tables.md) | Una tabla de descriptores es lógicamente una matriz de descriptores. |
| [Firmas raíz](root-signatures.md) | La firma raíz define los tipos de recursos que se enlazan a la canalización de gráficos. |
| [Consulta de funcionalidades](capability-querying.md) | La aplicación puede detectar el nivel de compatibilidad para el enlace de recursos y muchas otras características, con una llamada a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). |
| [Enlace de recursos en HLSL](resource-binding-in-hlsl.md) | En este tema se describen algunas características específicas del uso del [modelo de sombreador](/windows/desktop/direct3dhlsl/shader-model-5-1) del lenguaje HLSL (High Level Shader Language) 5,1 con Direct3D 12. Todo el hardware de Direct3D 12 admite el modelo de sombreador 5,1, por lo que la compatibilidad con este modelo no depende de cuál sea el nivel de características de hardware. |
| [Optimizaciones de UMA: texturas accesibles por CPU y swizzle estándar](default-texture-mapping.md) | Las GPU de arquitectura de memoria universal (UMA) ofrecen algunas ventajas de eficiencia frente a las GPU discretas, especialmente cuando se optimizan para dispositivos móviles. La concesión de recursos de acceso de CPU cuando la GPU es UMA puede reducir la cantidad de copia que se produce entre la CPU y la GPU. Aunque no se recomienda que las aplicaciones ofrezcan acceso a la CPU a todos los recursos de los diseños de UMA, existen oportunidades para mejorar las eficiencias proporcionando el acceso a la CPU de los recursos correctos. A diferencia de las GPU discretas, la CPU puede tener técnicamente un puntero a todos los recursos a los que puede tener acceso la GPU. |
| [Cargas de vista de acceso no ordenada con tipo](typed-unordered-access-view-loads.md) | La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con [**un \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)específico. |
| [Recursos en mosaico de volumen](volume-tiled-resources.md) | Las texturas de volumen (3D) se pueden usar como recursos en mosaico, teniendo en cuenta que la resolución de mosaicos es tridimensional. |
| [Subrecursos](subresources.md) | Describe cómo un recurso se divide en Subrecursos y cómo hacer referencia a un único, varios o un segmento de Subrecursos. |

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación de Direct3D 12](directx-12-programming-guide.md)
* [Tutoriales de vídeo de aprendizaje avanzado de DirectX: enlace de recursos en DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Administración de memoria](memory-management.md)