---
description: Las texturas siempre se abordan linealmente desde (0,0, 0,0) en la esquina superior izquierda hasta (1,0, 1,0) en la esquina inferior derecha, como se muestra en la ilustración siguiente.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtrado de textura bilineal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566148"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a>Filtrado de textura bilineal (Direct3D 9)

Las texturas siempre se abordan linealmente desde (0,0, 0,0) en la esquina superior izquierda hasta (1,0, 1,0) en la esquina inferior derecha, como se muestra en la ilustración siguiente.

![ilustración de textura 4x4 con bloques sólidos de color](images/bilinear-fig7a.png)

Las texturas normalmente se representan como si estuvieran compuestas de bloques sólidos de color, pero en realidad es más correcto pensar en texturas de la misma manera que debería pensar en la presentación de trama: cada texel se define en el centro exacto de una celda de cuadrícula, como se muestra en la ilustración siguiente.

![ilustración de textura 4x4 con elementos de textura definidos en el centro de las celdas de cuadrícula](images/bilinear-fig7b.png)

Si le pide al muestreador de textura el color de esta textura en coordenadas UV (0,375, 0,375), tendrá un rojo sólido (255, 0, 0). Esto tiene un sentido perfecto porque el centro exacto de la celda de texel rojo está en UV (0,375, 0,375). ¿Qué ocurre si pide al muestreador el color de la textura en UV (0,25, 0,25)? Esto no es tan fácil, ya que el punto de UV (0,25, 0,25) se encuentra en la esquina exacta de 4 elementos de textura.

El esquema más sencillo es simplemente hacer que el muestreador devuelva el color del elemento de textura más cercano; esto se denomina Filtrado de puntos (consulte Muestreo de punto más cercano [(Direct3D 9) )](nearest-point-sampling.md)y normalmente no se desea debido a resultados de grano o bloques. El muestreo de punto de nuestra textura en UV (0,25, 0,25) muestra otro problema sutil con el filtrado de punto más cercano: hay cuatro elementos de textura equidistantes desde el punto de muestreo, por lo que no hay ningún único texel más cercano. Uno de esos cuatro elementos de textura se elegirá como color devuelto, pero la selección depende de cómo se redondee la coordenada, lo que puede introducir artefactos de desmontaje (consulte el artículo muestreo de Nearest-Point en el SDK).

Un esquema de filtrado ligeramente más preciso y más común es calcular la media ponderada de los 4 elementos de textura más cercanos al punto de muestreo. Esto se denomina filtrado bilineal y el costo de cálculo adicional suele ser insignificante porque esta rutina se implementa en hardware gráfico moderno. Estos son los colores que se obtienen en algunos puntos de ejemplo diferentes mediante el filtrado bilineal:


```
UV: (0.5, 0.5)
```



Este punto se encuentra en el borde exacto entre los elementos de textura rojo, verde, azul y blanco. El color que devuelve el muestreador es gris:


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



Este punto está en el punto medio del borde entre los elementos de textura rojo y verde. El color que devuelve el muestreador es amarillo-gris (tenga en cuenta que las contribuciones de los elementos de textura azul y blanco se escalan a 0):


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



Esta es la dirección del texel rojo, que es el color devuelto (todos los demás elementos de textura del cálculo de filtrado se ponderan en 0):


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



Compare estos cálculos con la ilustración siguiente, que muestra lo que sucede si el cálculo de filtrado bilineal se realiza en cada dirección de textura en la textura 4x4.

![ilustración de textura 4x4 con filtrado bilineal realizado en cada dirección de textura](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de texturas](texture-filtering.md)
</dt> </dl>

 

 



