---
description: Si solo pasa la esquina superior izquierda de una imagen al método DrawImage, Windows GDI+ podría escalar la imagen, lo que reduciría el rendimiento.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Mejorar el rendimiento evitando el escalado automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985163"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Mejorar el rendimiento evitando el escalado automático

Si solo pasa la esquina superior izquierda de una imagen al método **DrawImage** , Windows GDI+ podría escalar la imagen, lo que reduciría el rendimiento.

La siguiente llamada al método **DrawImage** especifica una esquina superior izquierda de (50, 30) pero no especifica un rectángulo de destino:


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Aunque esta es la versión más sencilla del método **DrawImage** en cuanto al número de argumentos necesarios, no es necesariamente el más eficaz. Si el número de puntos por pulgada en el dispositivo de pantalla actual es diferente del número de puntos por pulgada en el dispositivo en el que se creó la imagen, GDI+ escala la imagen para que su tamaño físico en el dispositivo de pantalla actual sea lo más cercano posible a su tamaño físico en el dispositivo en el que se creó.

Si desea evitar el escalado, pase el ancho y el alto de un rectángulo de destino al método **DrawImage** . En el ejemplo siguiente se dibuja la misma imagen dos veces. En el primer caso, no se especifican el ancho y el alto del rectángulo de destino, y la imagen se escala automáticamente. En el segundo caso, el ancho y el alto (medidos en píxeles) del rectángulo de destino se especifican de la misma forma que el ancho y el alto de la imagen original.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



En la ilustración siguiente se muestra la imagen representada dos veces.

![captura de pantalla de una ventana que contiene dos versiones de una imagen en diferentes escalas](images/scaledtexture1.png)

 

 



