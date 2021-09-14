---
description: Cálculo de valores de parámetro
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Cálculo de valores de parámetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161657"
---
# <a name="calculating-parameter-values"></a>Cálculo de valores de parámetro

Potencialmente, un búfer de entrada podría ser muy grande. Idealmente, cuando el DMO procesa el búfer, los parámetros seguirán exactamente sus curvas en todo el lote de datos. Sin embargo, un DMO tiene cierto margen en la forma en que calcula esos valores.

-   El enfoque más preciso es calcular el valor exacto de cada unidad atómica de datos. por ejemplo, cada ejemplo de audio. Este enfoque es el más costoso computacionalmente.
-   Otro enfoque es segmentar los datos en unidades más pequeñas de algún tamaño fijo, como 100 muestras. Este enfoque crea un efecto de "escalón". Para algunos parámetros, podría ser aceptable. En los efectos de audio, podría crear artefactos de audio.
-   Un riesgo consiste en usar la técnica anterior, pero dentro de cada lote, realice una interpolación lineal del valor del parámetro para cada muestra.

Estos problemas son especialmente importantes para el procesamiento de audio. Un segundo de audio puede contener 48 000 muestras de audio por canal, lo que es una gran cantidad de cálculos para realizar, pero el oído es sensible a artefactos como el alias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 



