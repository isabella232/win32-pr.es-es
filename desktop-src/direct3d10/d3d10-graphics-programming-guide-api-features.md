---
description: La canalización de gráficos de Direct3D 10 representa un cambio de arquitectura fundamental, recompilado desde el principio en hardware y software para dar potencia a la próxima generación de juegos y aplicaciones multimedia 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Características de API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 416018fcddf2643ba9fbc8e633ec2f636b8158ff329780a55205034e5dbbe240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858665"
---
# <a name="api-features-direct3d-10"></a>Características de API (Direct3D 10)

La canalización de gráficos de Direct3D 10 representa un cambio de arquitectura fundamental, recompilado desde el principio en hardware y software para dar potencia a la próxima generación de juegos y aplicaciones multimedia 3D. Usa el modelo Windows display driver model (WDDM), que permite mejoras de rendimiento y comportamiento, como la memoria de GPU virtual.

Los desarrolladores familiarizados con Direct3D 9 detectarán una serie de mejoras funcionales y mejoras de rendimiento en Direct3D 10, entre las que se incluyen:

-   La capacidad de procesar primitivas enteras en la nueva fase [del sombreador de geometría.](/previous-versions//bb205146(v=vs.85))
-   La capacidad de generar datos de vértice generados por la canalización en la memoria mediante la [fase stream-output](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organización del estado de canalización en 5 objetos de [estado](d3d10-graphics-programming-guide-api-features-state-objects.md)inmutables, lo que permite una configuración rápida de la canalización.
-   Organización de constantes de sombreador en [búferes constantes,](d3d10-graphics-programming-guide-resources-types.md)lo que minimiza la sobrecarga de ancho de banda para proporcionar datos constantes de sombreador.
-   La capacidad de realizar el intercambio y la configuración de material por primitiva mediante un sombreador de geometría.
-   Nuevos [tipos de recursos](d3d10-graphics-programming-guide-resources-types.md) (incluidas matrices de textura que se pueden indexar a partir de sombreadores) y formatos de recursos.
-   Se ha aumentado la generalización del acceso a los recursos mediante [una vista](d3d10-graphics-programming-guide-resources-access-views.md).
-   Los bits de funcionalidad de hardware heredados (límites) se han quitado en favor de un amplio conjunto de funcionalidades garantizadas, que tiene como destino el hardware de 10 clases de Direct3D (mínimo).
-   [Tiempo](d3d10-graphics-programming-guide-api-features-layers.md) de ejecución por capas: la API de Direct3D 10 se construye con capas, empezando por la funcionalidad básica en el núcleo y creando funcionalidades opcionales y de ayuda para el desarrollador (depuración, etc.) en capas externas.
-   Integración completa de HLSL: todos los sombreadores de Direct3D 10 se escriben en HLSL y se implementan con el [núcleo de sombreador común](../direct3dhlsl/dx-graphics-hlsl-common-core.md).
-   Un aumento en el número de destinos de representación, texturas y muestreadores. Tampoco hay ningún límite de longitud del sombreador.
-   Operaciones de sombreador entero y bit a bit.
-   Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.
-   Compatibilidad multimuestreo de alfa a cobertura.

Hay diferencias de comportamiento adicionales que los desarrolladores de Direct3D 9 también deben tener en cuenta (consulte Consideraciones de [Direct3D 9 a Direct3D 10).](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)

Esta es una lista de características de Direct3D 9 que ya no se admiten o que se han revisado en Direct3D 10 (consulte Características en [desuso).](d3d10-graphics-programming-guide-api-features-deprecated.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
