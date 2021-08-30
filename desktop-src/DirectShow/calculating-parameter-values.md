---
description: Cálculo de valores de parámetro
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Cálculo de valores de parámetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad23cb9c50413fed36dde205ef97be0139dd6152f0a301f230793ef2cb131684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057775"
---
# <a name="calculating-parameter-values"></a>Cálculo de valores de parámetro

Potencialmente, un búfer de entrada podría ser muy grande. Idealmente, cuando el DMO procesa el búfer, los parámetros seguirán exactamente sus curvas a lo largo de todo el lote de datos. Sin embargo, DMO tiene algún margen de margen en cómo calcula esos valores.

-   El enfoque más preciso es calcular el valor exacto de cada unidad atómica de datos. por ejemplo, cada muestra de audio. Este enfoque es el más costoso a nivel computacional.
-   Otro enfoque es segmentar los datos en unidades más pequeñas de algún tamaño fijo, como 100 muestras. Este enfoque crea un efecto de "escalón". Para algunos parámetros, podría ser aceptable. En los efectos de audio, podría crear artefactos de sonido.
-   Un riesgo es usar la técnica anterior, pero dentro de cada lote, realice una interpolación lineal del valor del parámetro para cada muestra.

Estos problemas son especialmente importantes para el procesamiento de audio. Un segundo de audio puede contener 48 000 muestras de audio por canal, lo que es una gran cantidad de cálculos para realizar, pero el oído es sensible a artefactos como el alias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 



