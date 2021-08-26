---
title: Espacios de color HLS
description: Los espacios de colores HLS también son ampliamente utilizados por los intérpretes. Sus componentes de color son matiz, lumura y saturación (croma).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Windows Sistema de colores (WCS), espacios de colores HLS
- WCS (Windows de colores), espacios de color HLS
- administración de colores de imagen, espacios de colores HLS
- administración de colores, espacios de colores HLS
- colors,HLS color spaces
- espacios de colores, HLS
- Espacios de colores HLS
- Hue
- Saturación
- Ligereza
- saturación cero
- saturación de matiz (HLS)
- HLS (saturación de matiz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0dc0c47555f5358360a1ac81faf113c0fd6e98572c4d0c96852070a1749073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934975"
---
# <a name="hls-color-spaces"></a>Espacios de color HLS

Los espacios [de colores HLS](c.md) también son ampliamente utilizados por los intérpretes. Sus componentes de color son matiz, lumura y saturación (croma).

Hue tiene el mismo significado que el modelo HSV, salvo que un ángulo de matiz de 0 corresponde al azul de este modelo. La marca Descilaz está en 60 y la roja en 120. Al igual que con el modelo HSV, los colores complementarios tienen una diferencia de 180.

La lumura es la cantidad de blanco o negro en un color. El aumento de la lightness agrega blanco al matiz. La disminución de la lightness agrega negro al matiz.

[La](s.md) saturación en el modelo HLS es una medida de la "puridad" de un matiz. A medida que se reduce la saturación, el matiz se vuelve más gris. Un valor de saturación de cero da como resultado un valor de escala de grises.

La ilustración siguiente es un dibujo de línea del espacio HLS, que es un hexadecimal doble. Cualquier sección transversal horizontal del espacio de colores HLS es un hexágono. HLS es un espacio de colores normalizado. Es decir, los valores de lumez y saturación oscilan entre 0,0 y 1,0 inclusive. Hue varía de 0 a 360 inclusive.

![espacio de colores hls](images/hlsline.png)

Los espacios de color HLS pueden ser dependientes del dispositivo o independientes del dispositivo.

 

 




