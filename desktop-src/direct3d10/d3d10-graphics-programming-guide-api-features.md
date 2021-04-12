---
description: La canalización de gráficos de Direct3D 10 representa un cambio fundamental en la arquitectura, que se vuelve a crear desde el principio del hardware y el software para potenciar la próxima generación de juegos y aplicaciones multimedia 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Características de la API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274892"
---
# <a name="api-features-direct3d-10"></a>Características de la API (Direct3D 10)

La canalización de gráficos de Direct3D 10 representa un cambio fundamental en la arquitectura, que se vuelve a crear desde el principio del hardware y el software para potenciar la próxima generación de juegos y aplicaciones multimedia 3D. Usa Windows Display Driver Model (WDDM), que permite mejorar el rendimiento y el comportamiento, como la memoria virtual de la GPU.

Los desarrolladores familiarizados con Direct3D 9 detectarán una serie de mejoras funcionales y mejoras de rendimiento en Direct3D 10, entre las que se incluyen:

-   La capacidad de procesar primitivas enteras en la nueva [fase de sombreador de geometría](/previous-versions//bb205146(v=vs.85)).
-   La capacidad de generar datos de vértices generados por la canalización en la memoria mediante la [fase de flujo de salida](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organización del estado de la canalización en cinco [objetos de estado](d3d10-graphics-programming-guide-api-features-state-objects.md)inmutables, lo que permite una configuración rápida de la canalización.
-   Organización de constantes de sombreador en [búferes de constantes](d3d10-graphics-programming-guide-resources-types.md), lo que minimiza la sobrecarga de ancho de banda para proporcionar datos de constantes de sombreador.
-   La capacidad de realizar el intercambio y la configuración de materiales por primitivo mediante un sombreador de geometría.
-   Nuevos [tipos de recursos](d3d10-graphics-programming-guide-resources-types.md) (incluidas las matrices de texturas que se pueden indizar a partir de sombreadores) y formatos de recursos.
-   Mayor generalización del acceso a los recursos mediante una [vista](d3d10-graphics-programming-guide-resources-access-views.md).
-   Los bits de capacidad de hardware heredado (Cap) se han quitado en favor de un amplio conjunto de funcionalidades garantizadas, cuyo destino es hardware de clase de Direct3D 10 (mínimo).
-   [Runtime en capas](d3d10-graphics-programming-guide-api-features-layers.md) : la API de Direct3D 10 se construye con capas, comenzando con la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para desarrolladores (depuración, etc.) en capas externas.
-   Integración de HLSL completa: todos los sombreadores de Direct3D 10 están escritos en HLSL e implementados con [Common-Shader Core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).
-   Aumento en el número de destinos de representación, texturas y muestreadores. Tampoco hay ningún límite de longitud de sombreador.
-   Operaciones de sombreador Integer y bit a bit.
-   Readback de una superficie de estarcido o profundidad o un recurso de muestreo multimuestreado, una vez que ya no está enlazado como destino de representación.
-   Compatibilidad con Alpha-to-Coverage multimuestreado.

Existen diferencias de comportamiento adicionales que los desarrolladores de Direct3D 9 también deben tener en cuenta (consulte [consideraciones de Direct3D 9 a Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).

Esta es una lista de características de Direct3D 9 que ya no se admiten o que se han revisado en Direct3D 10 (consulte [características desusadas](d3d10-graphics-programming-guide-api-features-deprecated.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
