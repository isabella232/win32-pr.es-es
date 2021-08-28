---
title: Intenciones de representación
description: International Color Consortium (ICC) ha definido cuatro valores diferentes denominados intenciones de representación.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Sistema de colores (WCS), intenciones de representación
- WCS (Windows color), intenciones de representación
- administración del color de imagen, intenciones de representación
- administración de colores, intenciones de representación
- colors,rendering intents
- intenciones de representación
- International Color Consortium (ICC)
- IIC (International Color Consortium)
- Intención de imagen
- Intención gráfica
- Intención de prueba
- Coincidencia de intención
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f25159eaa50a9d7d28b582d72401da116f729af38f57f99a9ccaf5bb3877c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670788"
---
# <a name="rendering-intents"></a>Intenciones de representación

International Color Consortium (ICC) ha definido cuatro valores diferentes denominados *intenciones de representación.* Representan cuatro enfoques diferentes para crear una representación de color. Estas cuatro intenciones y las constantes usadas para hacer referencia a ellas en el código son las siguientes.



| Intención                            | Nombre DE LA CPI              | Descripción                    |
|-----------------------------------|-----------------------|--------------------------------|
| Imagen | Perceptivo            | \_PERCEPTUAL DE INTENCIÓN             |
| Graphic | Saturación            | SATURACIÓN \_ DE INTENCIÓN             |
| Prueba     | Colorimétrico relativo | \_ \_ COLORIMETRIC RELATIVO DE INTENCIÓN |
| Match     | Colorimétrico absoluto | \_ \_ COLORIMETRIC ABSOLUTO DE INTENCIÓN |




 

La especificación de formato de perfil DE LA VERSIÓN 3.4, que describe estas intenciones, se puede descargar desde color.org.

## <a name="picture-intent"></a>Intención de imagen

Llamada intención perceptual en la cláusula 4.9 de [](./g.md) la especificación DE ACUERDO, una intención Picture hace que la gama completa de la imagen se comprima o expanda para rellenar la gama del dispositivo de destino, de modo que se conserve el equilibrio de grises pero no se conserve la precisión colorimétrica.

En otras palabras, si determinados colores de una imagen quedan fuera del intervalo de colores que puede representar el dispositivo de salida, la intención de la imagen hará que todos los colores de la imagen se ajusten para que todos los colores de la imagen se encuentran dentro del intervalo que se puede representar y para que la relación entre los colores se conserve tanto como sea posible.

Esta intención es más adecuada para mostrar fotografías e imágenes, y suele ser la intención predeterminada.

## <a name="graphic-intent"></a>Intención gráfica

La cláusula de especificación 4.12 DE LA CLÁUSULA DE LA CLÁUSULA 4.12 llama a la intención Gráfico una intención [de saturación.](s.md) Conserva la capa de colores de la imagen [](h.md) a costa de la matiz [y la lumíz posibles.](l.md)

La implementación de esta intención sigue siendo un poco problemática y LA CPI sigue trabajando en métodos para lograr los efectos deseados.

Esta intención es más adecuada para gráficos empresariales, como gráficos, en los que es más importante que los colores sean muy claros y contrasten bien entre sí, en lugar de un color específico.

## <a name="proof-intent"></a>Intención de prueba

La intención Proof, denominada intención colorimétrica en la especificación DE C#, se define de forma que los colores que se encuentran fuera del intervalo que puede representar el dispositivo de salida se ajusten al color más cercano que se puede representar, mientras que el resto de colores se mantienen sin cambios.

La intención de prueba no conserva el [punto blanco](w.md).

Por ejemplo, el blanco más blanco de un papel es más amarillo que el blanco más blanco de un monitor de equipo. Una imagen convertida en la gama de la impresora con intención colorimétrica relativa daría lugar a que todos los colores se vuelvan más amarillos. El punto blanco de la imagen se mueve para que coincida con el punto blanco de la impresora. Todos los demás colores de la imagen mantienen su posición con respecto al punto blanco. Esto genera una imagen que refleja con mayor precisión el aspecto de la imagen impresa. Sin embargo, es posible que el usuario lo encuentre visualmente desconcertante.

## <a name="match-intent"></a>Intención de coincidencia

En una intención Match, los colores que se encuentran fuera del intervalo que puede representar el dispositivo de salida se ajustan al color más cercano que se puede representar, mientras que todos los demás colores se mantienen sin cambios. La especificación DECN llama a la intención de coincidencia intención colorimétrica absoluta.

La intención de coincidencia conserva el punto blanco.

Por ejemplo, el blanco más blanco de un papel es más amarillo que el blanco más blanco de un monitor de equipo. Una imagen convertida en la [gama](./g.md) de la impresora mediante la intención de coincidencia daría lugar a que todos los colores se conviertan y coincidan con la gama de la impresora. El punto blanco de la imagen no se mueve para que coincida con el punto blanco de la impresora. Por lo tanto, la distancia de los colores hasta el punto blanco puede cambiar. Esto genera una imagen que es menos desconcertante visualmente para el usuario, pero también es una representación menos precisa de la salida de la impresora.

 

 