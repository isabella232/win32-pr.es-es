---
description: Calcular valores de parámetros
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calcular valores de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659275"
---
# <a name="calculating-parameter-values"></a>Calcular valores de parámetros

Potencialmente, un búfer de entrada podría ser muy grande. Idealmente, cuando DMO procesa el búfer, los parámetros seguirán exactamente sus curvas en todo el lote de datos. Sin embargo, un DMO tiene algunos libertad en cómo calcula esos valores.

-   El enfoque más preciso consiste en calcular el valor exacto de cada unidad atómica de datos; por ejemplo, cada ejemplo de audio. Este enfoque es el más costoso.
-   Otro enfoque consiste en segmentar los datos en unidades más pequeñas de un tamaño fijo, como ejemplos de 100. Este enfoque crea un efecto de "paso de escalera". En algunos parámetros, podría ser aceptable. En efectos de audio, podría crear artefactos auditivos.
-   Un compromiso es usar la técnica anterior, pero dentro de cada lote, realice una interpolación lineal del valor del parámetro para cada ejemplo.

Estos problemas son especialmente importantes para el procesamiento de audio. Un segundo de audio puede contener 48.000 muestras de audio por canal, que es una gran cantidad de cálculos para realizar, pero la lengüeta es sensible a los artefactos como el alias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 



