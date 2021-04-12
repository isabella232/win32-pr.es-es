---
description: 'Tenga en cuenta lo siguiente al decidir cuándo y cómo usar el objeto divisor en una aplicación:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Otras consideraciones del divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277780"
---
# <a name="other-divider-considerations"></a>Otras consideraciones del divisor

Tenga en cuenta lo siguiente al decidir cuándo y cómo usar el objeto [**divisor**](inkdivider-class.md) en una aplicación:

-   El objeto [**divisor**](inkdivider-class.md) está diseñado para separar dibujos y bloques de escritura a mano, pero no para reconocer niveles más altos de estructura, como tablas o columnas.
-   El objeto [**divisor**](inkdivider-class.md) no proporciona interfaces específicamente para la corrección de los resultados del análisis de diseño.
-   El uso del tiempo de espera y el número de heurísticas de trazo para agregar o quitar varios trazos a la vez desde los trazos del objeto de [**divisor**](inkdivider-class.md) pueden mejorar el rendimiento.

## <a name="reanalysis-considerations"></a>Consideraciones de análisis

Si está pensando en utilizar el objeto [**divisor**](inkdivider-class.md) en una aplicación en la que el objeto **divisor** puede tener que volver a analizar grandes cantidades de tinta, tenga en cuenta lo siguiente.

### <a name="retaining-copies-of-ink-and-strokes"></a>Conservar copias de lápiz y trazos

Una aplicación puede mantener copias de los objetos [**Ink**](inkdisp-class.md) y [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) de los elementos de la aplicación que se pueden revisar posteriormente en la sesión de la aplicación. Esto elimina la necesidad de volver a analizar el objeto de **entrada manuscrita** si el usuario vuelve al elemento. Este enfoque se desaconseja de la memoria para mejorar el rendimiento.

### <a name="data-reduction-heuristics"></a>Heurística de reducción de datos

Es posible que pueda grabar los resultados del análisis como datos de la aplicación e implementar la heurística para determinar cuándo se debe volver a analizar un conjunto de trazos. Esta práctica reduciría la necesidad de volver a analizar toda la tinta de la aplicación entre sesiones de aplicación. Sin embargo, se debe tener cuidado para conservar los límites de los elementos estructurales o para volver a analizar todos los trazos de los elementos afectados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Clase InkDivider**](inkdivider-class.md)
</dt> <dt>

[Clase Microsoft. Ink. divisor](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
