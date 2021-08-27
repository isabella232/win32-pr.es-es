---
title: Conversión de colores y coincidencia de color
description: El proceso de conversión de colores de un espacio de color a otro se denomina conversión de color.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Sistema de colores (WCS), conversión de color
- WCS (Windows de color),conversión de color
- administración de colores de imagen, conversión de colores
- administración de colores, conversión de colores
- colors,color conversion
- conversión de colores
- Windows Sistema de colores (WCS), coincidencia de colores
- WCS (Windows de color), coincidencia de colores
- administración del color de imagen, coincidencia de colores
- administración de colores, coincidencia de colores
- colores, coincidencia de colores
- coincidencia de colores
- Windows Sistema de colores (WCS), asignación de colores
- WCS (Windows de color), asignación de colores
- administración de colores de imagen, asignación de colores
- administración de colores, asignación de colores
- colors,color mapping
- asignación de colores
- punto blanco
- Colorantes
- corrección gamma
- Gama
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0071e15c2d572c134d61aee7a018b41c8d09507e87963eeeed1488909cdafeba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110805"
---
# <a name="color-conversion-and-color-matching"></a>Conversión de colores y coincidencia de color

El proceso de conversión de colores de un [espacio de colores](c.md) a otro se denomina conversión de *color.* Todos los colores de un espacio de colores se fijan en relación con el punto en blanco [del espacio de colores.](w.md) Puesto que el punto en blanco de un espacio de color varía de un dispositivo a otro, un color convertido debe coincidir con su color visualmente más cercano en el espacio de color de destino. Este proceso se denomina *asignación de colores.*

Por ejemplo, si tiene una imagen digital que creó en la pantalla, puede estar en un espacio de color RGB dependiente del dispositivo. Si desea imprimirla en una impresora, debe convertirse en el espacio de color de la impresora. Puesto que la impresora probablemente usa un espacio de colores CONVERT dependiente del dispositivo, todos los valores RGB deben convertirse a CYMK. Se trata de la [conversión de colores](c.md). Una vez especificados los valores en términos del espacio CYMK, deben coincidir con el color más cercano que puede producir la impresora. Esto se denomina asignación de colores o [color que coincide con](c.md).

Tanto la conversión de colores como la asignación de colores deben tener en cuenta una serie de factores específicos del dispositivo. Por ejemplo, los bloques de creación de imágenes de pantalla son píxeles. Cada píxel tiene un número establecido de bits para almacenar su valor de índice de color o color. El número de bits por píxel depende del tipo de adaptador para mostrar y mostrar que se usa y del modo en el que se establece el adaptador. La mayoría de los tipos de impresora [usan diferentes colores](c.md) e imprime con resoluciones concretas.

Además, las características de tono físico de un dispositivo suelen ser diferentes en distintos dispositivos. Por ejemplo, cuando los monitores de equipo producen colores, pueden parecer diferentes de los que tendrían si se hubieran producido en una impresión. Un factor de corrección, denominado *corrección gamma,* se usa con frecuencia para compensar estas diferencias.

El resultado de estos factores dependientes del dispositivo es que cada dispositivo de color tiene un conjunto determinado de colores que puede producir. Este conjunto de colores se conoce como *su gama*. Para realizar la conversión de colores y la asignación de colores, los colores de una imagen deben convertirse del espacio de colores y la gama del dispositivo de origen en el espacio de colores del dispositivo de destino. A continuación, se comparan con la gama del dispositivo de destino.

 

 




