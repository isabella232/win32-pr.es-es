---
description: Si pasa solo la esquina superior izquierda de una imagen al método DrawImage, Windows GDI+ podría escalar la imagen, lo que reduciría el rendimiento.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Mejorar el rendimiento evitando el escalado automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac74fbf636f3f1cbdf088939ad76732907c15228e66662a7246b3f0c0313c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778735"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Mejorar el rendimiento evitando el escalado automático

Si pasa solo la esquina superior izquierda de una imagen al método **DrawImage,** Windows GDI+ escalar la imagen, lo que reduciría el rendimiento.

La siguiente llamada al **método DrawImage** especifica una esquina superior izquierda de (50, 30), pero no especifica un rectángulo de destino:


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Aunque esta es la versión más sencilla del método **DrawImage** en cuanto al número de argumentos necesarios, no es necesariamente la más eficaz. Si el número de puntos por pulgada en el dispositivo de pantalla actual es diferente del número de puntos por pulgada en el dispositivo donde se creó la imagen, GDI+ escala la imagen para que su tamaño físico en el dispositivo de pantalla actual sea lo más cercano posible a su tamaño físico en el dispositivo donde se creó.

Si desea evitar este escalado, pase el ancho y el alto de un rectángulo de destino al **método DrawImage.** En el ejemplo siguiente se dibuja la misma imagen dos veces. En el primer caso, no se especifican el ancho y el alto del rectángulo de destino y la imagen se escala automáticamente. En el segundo caso, el ancho y el alto (medidos en píxeles) del rectángulo de destino se especifican para que sean iguales que el ancho y alto de la imagen original.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



En la ilustración siguiente se muestra la imagen que se representa dos veces.

![captura de pantalla de una ventana que contiene dos versiones de una imagen a escalas diferentes](images/scaledtexture1.png)

 

 



