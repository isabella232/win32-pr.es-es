---
title: Espacios de color HLS
description: Los artistas también usan los espacios de colores HLS. Sus componentes de color son matiz, luminosidad y saturación (croma).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Sistema de color de Windows (WCS), espacios de color HLS
- WCS (sistema de colores de Windows), espacios de color HLS
- Administración del color de imagen, espacios de color HLS
- Administración del color, espacios de color HLS
- colores, espacios de color HLS
- espacios de colores, HLS
- Espacios de color HLS
- altera
- satura
- luminosidad
- saturación cero
- saturación de luminosidad de matiz (HLS)
- HLS (saturación de luminosidad de matiz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613a62d4a998b51f9bfb22bd7431dd8645a72f3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721119"
---
# <a name="hls-color-spaces"></a>Espacios de color HLS

Los artistas también usan los [espacios de colores](c.md) HLS. Sus componentes de color son matiz, luminosidad y saturación (croma).

Hue tiene el mismo significado que el modelo HSV, salvo que un ángulo de matiz de 0 corresponde a Blue en este modelo. Magenta está en 60, el rojo está en 120. Al igual que con el modelo HSV, los colores complementarios están separados por 180.

La luminosidad es la cantidad de blanco o negro en un color. Aumentar la luminosidad agrega blanco al matiz. Al reducir la luminosidad, se agrega negro al matiz.

La [saturación](s.md) del modelo HLS es una medida de la "pureza" de un matiz. A medida que se reduce la saturación, el matiz se vuelve más gris. Un valor de saturación de cero da como resultado un valor de escala de grises.

La siguiente ilustración es un dibujo de línea del espacio HLS, que es un doble hexcone. Cualquier sección transversal horizontal del espacio de colores HLS es un hexágono. HLS es un espacio de colores normalizado. Es decir, los valores de luminosidad y saturación van de 0,0 a 1,0, ambos incluidos. Hue varía entre 0 y 360, ambos inclusive.

![espacio de color HLS](images/hlsline.png)

Los espacios de colores HLS pueden ser dependientes del dispositivo o independientes del dispositivo.

 

 




