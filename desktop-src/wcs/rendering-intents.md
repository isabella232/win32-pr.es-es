---
title: Intenciones de representación
description: El International color Consortium (ICC) ha definido cuatro valores distintos denominados representación del intents.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Sistema de color de Windows (WCS), representación de intenciones
- WCS (sistema de colores de Windows), representación de intenciones
- Administración del color de imagen, representación de intenciones
- Administración del color, representación de intenciones
- colores, representación de intenciones
- representación de intenciones
- International Color Consortium (ICC)
- IIC (International color Consortium)
- Intento de imagen
- Intención de gráficos
- Intento de prueba
- Intento de coincidencia
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721385"
---
# <a name="rendering-intents"></a>Intenciones de representación

El International color Consortium (ICC) ha definido cuatro valores distintos denominados *representación del intents*. Representan cuatro enfoques diferentes para crear una representación de color. Estas cuatro intenciones y las constantes que se usan para hacer referencia a ellas en el código son las siguientes.



| Intención                            | Nombre de ICC              | Descripción                    |
|-----------------------------------|-----------------------|--------------------------------|
| Imagen | Perceptual            | INTENCIÓN \_ perceptual             |
| Graphic | Saturación            | saturación de intención \_             |
| Prueba     | Colorimétrico relativo | \_referencia \_ colorimétrica relativa |
| Match     | Colorimétrico absoluto | INTENCIÓN \_ absoluta \_ colorimétrica |




 

La especificación de formato de Perfil de ICC versión 3,4, que describe estas intenciones, se puede descargar desde color.org.

## <a name="picture-intent"></a>Intento de imagen

Llamada perceptual en la cláusula 4,9 de la especificación de ICC, una intención de imagen hace que la [gama](./g.md) completa de la imagen se comprima o se expanda para rellenar la gama del dispositivo de destino, de modo que se conserve el equilibrio de gris, pero no se conserve la precisión de la colorimétrico.

En otras palabras, si ciertos colores de una imagen quedan fuera del intervalo de colores que el dispositivo de salida puede representar, el intento de imagen hará que se ajusten todos los colores de la imagen para que todos los colores de la imagen se encuentren dentro del intervalo que se puede representar y para que la relación entre los colores se conserve lo máximo posible.

Esta intención es más adecuada para la presentación de fotografías e imágenes, y suele ser la intención predeterminada.

## <a name="graphic-intent"></a>Intención de gráficos

La cláusula 4,12 de la especificación de ICC llama al gráfico como intención de [saturación](s.md) . Conserva el croma de los colores de la imagen con el posible gasto de [matiz](h.md) y [luminosidad](l.md).

La implementación de esta intención sigue siendo problemática y el ICC sigue trabajando en métodos para lograr los efectos deseados.

Esta intención es más adecuada para los gráficos empresariales, como los gráficos, donde es más importante que los colores sean intensos y contrasten bien entre sí, en lugar de con un color específico.

## <a name="proof-intent"></a>Intento de prueba

El intento de prueba, denominado el intento de colorimétrica en la especificación de ICC, se define de forma que los colores que se encuentran fuera del intervalo que el dispositivo de salida pueda representar se ajusten al color más cercano que se puede representar, mientras que todos los demás colores quedan inalterados.

El intento de prueba no conserva el [punto blanco](w.md).

Por ejemplo, el blanco más blanco de un papel es más amarillo que el blanco más blanco de un monitor de equipo. Una imagen convertida en la gama de la impresora con la intención colorimétrico relativo haría que todos los colores se convirtieran en más amarillo. El punto blanco de la imagen se mueve para que coincida con el punto blanco de la impresora. Todos los demás colores de la imagen mantienen su posición en relación con el punto blanco. Esto produce una imagen que refleja con más precisión el aspecto que tendrá la imagen impresa. Sin embargo, el usuario puede encontrarla desconcertado visualmente.

## <a name="match-intent"></a>Intento de coincidencia

En un intento de coincidencia, los colores que se encuentran fuera del intervalo que el dispositivo de salida puede representar se ajustan al color más cercano que se puede representar, mientras que todos los demás colores permanecen inalterados. La especificación ICC llama al intento de coincidencia de la intención de colorimétrico absoluto.

La intención de coincidencia conserva el punto blanco.

Por ejemplo, el blanco más blanco de un papel es más amarillo que el blanco más blanco de un monitor de equipo. Una imagen convertida en la [gama](./g.md) de la impresora con la intención de coincidencia haría que todos los colores se convirtieran y coincidían con la gama de la impresora. El punto blanco de la imagen no se mueve para que coincida con el punto blanco de la impresora. Por lo tanto, la distancia de los colores al punto blanco puede cambiar. Esto produce una imagen que es menos visualmente disparando al usuario, pero también es una representación menos precisa de la salida de la impresora.

 

 