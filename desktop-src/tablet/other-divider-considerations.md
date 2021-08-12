---
description: 'Tenga en cuenta lo siguiente al decidir cuándo y cómo usar el objeto Divider en una aplicación:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Otras consideraciones del divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3328fd553a16aeee1e1dfa5459b78a45732a55494e0481950d730dab7ce0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449365"
---
# <a name="other-divider-considerations"></a>Otras consideraciones del divisor

Tenga en cuenta lo siguiente al decidir cuándo y cómo usar el objeto [**Divider**](inkdivider-class.md) en una aplicación:

-   El [**objeto Divider**](inkdivider-class.md) está diseñado para separar dibujos y bloques de escritura a mano, pero no para reconocer niveles superiores de estructura, como tablas o columnas.
-   El [**objeto Divider**](inkdivider-class.md) no proporciona interfaces específicamente para la corrección de los resultados del análisis de diseño.
-   El uso del tiempo de espera y el número de heurísticas de trazo para agregar o quitar varios trazos a la vez de los trazos del objeto [**Divisor**](inkdivider-class.md) puede mejorar el rendimiento.

## <a name="reanalysis-considerations"></a>Consideraciones sobre el reanálisis

Si está pensando en usar el objeto [**Divider**](inkdivider-class.md) en una aplicación en la que es posible que el objeto **Divisor** tenga que volver a analizar grandes cantidades de lápiz, tenga en cuenta lo siguiente.

### <a name="retaining-copies-of-ink-and-strokes"></a>Conservar copias de lápiz y trazos

Una aplicación puede mantener copias de los [**objetos Ink**](inkdisp-class.md) y [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) para los elementos de la aplicación que se pueden volver a visitar más adelante en la sesión de la aplicación. Esto elimina la necesidad de volver aanalizar el objeto **Ink** si el usuario vuelve al elemento . Este enfoque negocia la memoria para mejorar el rendimiento.

### <a name="data-reduction-heuristics"></a>Heurística de reducción de datos

Puede registrar los resultados del análisis como datos de la aplicación e implementar heurística para determinar cuándo se debe volver a analizar un conjunto de trazos. Esta práctica reduciría la necesidad de volver aanalizar toda la entrada de lápiz de la aplicación entre sesiones de aplicación. Sin embargo, se debe tener cuidado para conservar los límites de elementos estructurales o para volver aanalizar todos los trazos de los elementos afectados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InkDivider (clase)**](inkdivider-class.md)
</dt> <dt>

[Clase Microsoft.Ink.Divider](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
