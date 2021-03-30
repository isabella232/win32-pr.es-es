---
description: Direct3D 9 admite puntos, líneas, triángulos y primitivas de cuadrícula.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Primitivas Higher-Order (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67767dd955fa5c0c5c21315d7c1c510de422870c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805323"
---
# <a name="higher-order-primitives-direct3d-9"></a>Primitivas Higher-Order (Direct3D 9)

Direct3D 9 admite puntos, líneas, triángulos y primitivas de cuadrícula. Se han ampliado para admitir la interpolación de orden superior más allá lineal. Mientras que los triángulos y las líneas tienen una extensión espacial, hasta ahora se representan mediante la interpolación lineal. En Direct3D 9, Direct3D admite la representación de estos tipos primitivos con un orden superior, hasta Quinta. Además, ahora se admite un nuevo tipo primitivo cuádruple. Este nuevo tipo también se puede representar con una interpolación de orden superior. Esta característica se rige principalmente por los requisitos de animación y representación de caracteres. También se puede usar para otras superficies, como terreno o agua.

Los primitivos de orden superior admiten la interpolación de orden superior cuando se transmiten a la API como listas, tiras, ventiladores o mallas indexadas. Esto se logra mediante el uso de información adicional codificada en los propios vértices. Por ejemplo, los vectores normales se pueden usar para definir planos tangentes en los vértices para habilitar la interpolación cúbica. La mayoría de las implementaciones admiten la interpolación de orden superior mediante teselación en triángulos planos. El paso de teselación se aplica lógicamente antes de la etapa del sombreador de vértices. Dado que la API del sombreador de vértices no impone la semántica en sus datos de entrada, se proporciona un mecanismo especial para identificar el componente de flujo de vértices que representa la posición y, opcionalmente, el vector normal. Todos los demás componentes se interpolan en consecuencia.

En esta sección se presentan los primitivos de orden superior y se describe cómo se pueden usar en las aplicaciones. La información se divide en los temas siguientes.

-   [Mejora de la calidad mediante la mejora de la resolución](#improved-quality-through-resolution-enhancement)
-   [Asignación directa desde herramientas de Spline-Based](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Mejora de la calidad mediante la mejora de la resolución

Los primitivos actuales no son ideales para representar superficies suaves. Los métodos de interpolación de orden superior, como los polinómicos cúbicos, permiten realizar cálculos más precisos en la representación de formas curvas. Esto proporciona mayor realismo al reducir o eliminar los artefactos de facetas visibles en los bordes de silueta o en la iluminación especular de la superficie. Además, cuando se produce la teselación en el chip, los triángulos teselados no afectan al ancho de banda del bus. En muchos casos, una pequeña cantidad de teselación puede proporcionar mejoras en la calidad de la imagen con un impacto mínimo en el rendimiento.

Direct3D 9 proporciona una manera sencilla de aplicar la mejora de la resolución al contenido creado por las herramientas orientadas a polígonos y las canalizaciones de arte existentes. La aplicación solo necesita proporcionar un nivel de teselación deseado y transmitir los datos mediante la sintaxis de triángulo estándar que incluye vectores normales.

## <a name="direct-mapping-from-spline-based-tools"></a>Asignación directa desde herramientas de Spline-Based

Muchas herramientas de creación actuales admiten primitivas de orden superior para permitir operaciones de modelado más eficaces que las que se proporcionan normalmente para con mallas de triángulo planas. Cuando se usa de forma eficaz, de modo que el número de revisiones generadas es razonable, estas herramientas pueden generar contenido que la API puede representar directamente. Para cumplir este requisito, se ha agregado un nuevo punto de entrada que interpreta el flujo de datos de vértices entrantes como una matriz 2D de puntos de control y tessellates a la resolución deseada.

-   [Usar primitivas de Higher-Order (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 



