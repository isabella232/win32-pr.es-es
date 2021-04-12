---
description: Las texturas siempre se dirigen linealmente desde (0,0, 0,0) en la esquina superior izquierda a (1,0, 1,0) en la esquina inferior derecha, tal como se muestra en la siguiente ilustración.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtrado de textura bilineal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423455"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a>Filtrado de textura bilineal (Direct3D 9)

Las texturas siempre se dirigen linealmente desde (0,0, 0,0) en la esquina superior izquierda a (1,0, 1,0) en la esquina inferior derecha, tal como se muestra en la siguiente ilustración.

![Ilustración de textura 4x4 con bloques sólidos de color](images/bilinear-fig7a.png)

Normalmente, las texturas se representan como si estuviesen compuestas de bloques sólidos de color, pero es realmente más correcto pensar en las texturas de la misma manera que debería pensar en la presentación de trama: cada textura se define en el centro exacto de una celda de la cuadrícula, como se muestra en la siguiente ilustración.

![Ilustración de textura 4x4 con textura definidos en el centro de las celdas de la cuadrícula](images/bilinear-fig7b.png)

Si pide al muestrario de texturas el color de esta textura en coordenadas UV (0,375, 0,375), obtendrá rojo sólido (255, 0,0). Esto resulta perfecto porque el centro exacto de la celda textura roja está en UV (0,375, 0,375). ¿Qué ocurre si pide al muestreador el color de la textura en UV (0,25, 0,25)? Eso no es tan fácil, porque el punto en UV (0,25, 0,25) se encuentra en la esquina exacta de 4 textura.

El esquema más sencillo es simplemente hacer que la muestra devuelva el color del textura más cercano; Esto se conoce como filtrado de puntos (vea el [muestreo de punto más cercano (Direct3D 9)](nearest-point-sampling.md)) y normalmente no es deseable debido a resultados granulares o bloqueados. Muestreo de puntos nuestra textura en UV (0,25, 0,25) muestra otro problema sutil con filtrado de punto más cercano: hay cuatro textura equidistantes desde el punto de muestreo, por lo que no hay una sola textura más cercana. Una de esas cuatro textura se elegirá como el color devuelto, pero la selección depende de cómo se redondee la coordenada, lo que puede producir artefactos de desgarro (vea el artículo de muestreo de Nearest-Point en el SDK).

Un esquema de filtrado ligeramente más preciso y más común consiste en calcular el promedio ponderado de 4 textura más cercano al punto de muestreo; Esto se denomina filtrado bilineal y el costo computacional adicional suele ser insignificante, ya que esta rutina se implementa en el hardware de gráficos moderno. Estos son los colores que obtenemos en algunos puntos de ejemplo diferentes mediante el filtrado bilineal:


```
UV: (0.5, 0.5)
```



Este punto se encuentra en el borde exacto entre el textura rojo, verde, azul y blanco. El color que devuelve el muestreador es gris:


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



Este punto está en el punto medio del borde entre el textura rojo y el verde. El color que devuelve la muestra es amarillo-gris (tenga en cuenta que las contribuciones del textura azul y blanco se escalan a 0):


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



Se trata de la dirección del textura rojo, que es el color devuelto (el resto de textura en el cálculo de filtrado se pondera en 0):


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



Compare estos cálculos con la siguiente ilustración, que muestra lo que sucede si se realiza el cálculo de filtrado bilineal en cada dirección de textura a través de la textura 4x4.

![Ilustración de textura 4x4 con filtrado bilineal realizado en cada dirección de textura](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de textura](texture-filtering.md)
</dt> </dl>

 

 



