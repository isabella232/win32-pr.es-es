---
title: Conversión de colores y coincidencia de color
description: El proceso de conversión de colores de un espacio de colores a otro se denomina conversión de color.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Sistema de color de Windows (WCS), conversión de color
- WCS (sistema de color de Windows), conversión de color
- Administración del color de imagen, conversión de color
- Administración del color, conversión de color
- colores, conversión de color
- conversión de color
- Sistema de color de Windows (WCS), coincidencia de color
- WCS (sistema de colores de Windows), coincidencia de color
- Administración del color de imagen, coincidencia de color
- Administración del color, coincidencia de color
- colores, coincidencia de color
- coincidencia de color
- Sistema de color de Windows (WCS), asignación de colores
- WCS (sistema de colores de Windows), asignación de colores
- Administración del color de imagen, asignación de colores
- Administración del color, asignación de colores
- colores, asignación de colores
- asignación de colores
- punto blanco
- colorants
- corrección gamma
- espectro
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721130"
---
# <a name="color-conversion-and-color-matching"></a>Conversión de colores y coincidencia de color

El proceso de conversión de colores de un [espacio de colores](c.md) a otro se denomina conversión de *color*. Todos los colores de un espacio de colores son fijos en relación con el [punto blanco](w.md)del espacio de colores. Dado que el punto blanco de un espacio de colores varía de un dispositivo a otro, un color convertido debe coincidir con su color visualmente más cercano en el espacio de colores de destino. Este proceso se denomina *asignación de colores*.

Por ejemplo, si tiene una imagen digital que ha creado en la pantalla, puede que esté en un espacio de colores RGB dependiente del dispositivo. Si desea imprimirlo en una impresora, debe convertirse en el espacio de colores de la impresora. Dado que es probable que la impresora use un espacio de colores CMYK dependiente del dispositivo, todos los valores RGB se deben convertir a CYMK. Esta es la [conversión de color](c.md). Una vez que los valores se especifican en términos del espacio CYMK, tienen que coincidir con el color más cercano que puede producir la impresora. Esto se denomina asignación de colores o [coincidencia de color](c.md).

Tanto la conversión de color como la asignación de colores deben tener en cuenta varios factores específicos del dispositivo. Por ejemplo, los bloques de creación de las imágenes de pantalla son píxeles. Cada píxel tiene un número de bits establecido para almacenar su valor de índice de color o color. El número de bits por píxel depende del tipo de adaptador de pantalla y de pantalla que se use, y del modo en el que se establece el adaptador. La mayoría de los tipos de impresora utiliza diferentes [Colorants](c.md) e imprime en determinadas resoluciones.

Además, las características de tono físico de un dispositivo suelen ser diferentes en distintos dispositivos. Por ejemplo, cuando los monitores de equipo generan colores, pueden aparecer diferentes de lo que si se hubieran producido en una imprenta. Un factor de corrección, denominado *corrección Gamma*, se usa con frecuencia para compensar tales diferencias.

El resultado de estos factores dependientes del dispositivo es que cada dispositivo de color tiene un conjunto determinado de colores que puede generar. Este conjunto de colores se conoce como su *gama*. Para realizar la conversión de colores y la asignación de colores, los colores de una imagen se deben convertir del espacio de colores y la gama del dispositivo de origen en el espacio de colores del dispositivo de destino. Después, se asocian a la gama del dispositivo de destino.

 

 




