---
description: Direct3D 9 admite puntos, líneas, triángulos y primitivas de cuadrícula.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Higher-Order primitivos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36ee67cfe4d4a802303091288f3906778e6cb3cdc1ad811602a80bc161d0a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122126"
---
# <a name="higher-order-primitives-direct3d-9"></a>Higher-Order primitivos (Direct3D 9)

Direct3D 9 admite puntos, líneas, triángulos y primitivas de cuadrícula. Se han ampliado para admitir la interpolación de orden superior más allá de lineal. Aunque los triángulos y las líneas tienen extensión espacial, hasta ahora ambos se representaron mediante interpolación lineal. En Direct3D 9, Direct3D admite la representación de estos tipos primitivos mediante un orden superior, hasta la interpolación. Además, ahora se admite un nuevo tipo primitivo quad. Este nuevo tipo también se puede representar con interpolación de orden superior. Esta característica se basa principalmente en los requisitos de animación y representación de caracteres. También se puede usar para otras superficies, como el terreno o el agua.

Las primitivas de orden superior admiten la interpolación de orden superior cuando se transmiten a la API como listas, bandas, ventiladores o mallas indexadas. Esto se consigue mediante el uso de información adicional codificada en los propios vértices. Por ejemplo, se pueden usar vectores normales para definir planos tangentes en los vértices para habilitar la interpolación cúbica. La mayoría de las implementaciones admiten la interpolación de orden superior mediante teselación en triángulos planas. El paso de teselación se aplica lógicamente antes de la fase del sombreador de vértices. Dado que la API del sombreador de vértices no impone semántica en sus datos de entrada, se proporciona un mecanismo especial para identificar el componente de flujo de vértice que representa la posición y, opcionalmente, el vector normal. Todos los demás componentes se interpolan en consecuencia.

En esta sección se presentan primitivas de orden superior y se describe cómo se pueden usar en las aplicaciones. La información se divide en los temas siguientes.

-   [Mejora de la calidad a través de la resolución](#improved-quality-through-resolution-enhancement)
-   [Asignación directa desde Spline-Based Tools](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Mejora de la calidad a través de la resolución

Las primitivas actuales no son ideales para representar superficies suavizadas. Los métodos de interpolación de orden superior, como los polinómicos cúbicos, permiten cálculos más precisos en la representación de formas curvas. Esto proporciona un mayor realismo mediante la reducción o eliminación de artefactos de faceting visibles en los bordes de las aristas o en la iluminación de la superficie especular. Además, cuando se produce la teselación en el chip, los triángulos teselados no afectan al ancho de banda del bus. En muchos casos, una pequeña cantidad de teselación puede proporcionar mejoras en la calidad de la imagen con un impacto mínimo en el rendimiento.

Direct3D 9 proporciona una manera sencilla de aplicar la mejora de resolución al contenido creado por las herramientas y canalizaciones de arte orientadas a polígonos existentes. La aplicación solo necesita proporcionar un nivel deseado de teselación y transmitir los datos mediante la sintaxis de triángulo estándar que incluye vectores normales.

## <a name="direct-mapping-from-spline-based-tools"></a>Asignación directa desde Spline-Based Tools

Muchas herramientas de creación actuales admiten primitivas de orden superior para permitir operaciones de modelado más eficaces de las que se proporcionan normalmente con mallas de triángulo planas. Cuando se usan de forma eficaz, de modo que el número de revisiones generadas sea razonable, estas herramientas pueden generar contenido que la API puede representar directamente. Para cumplir este requisito, se ha agregado un nuevo punto de entrada que interpreta el flujo de datos de vértices entrantes como una matriz 2D de puntos de control y lo tessola en la resolución deseada.

-   [Usar Higher-Order primitivos (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 



