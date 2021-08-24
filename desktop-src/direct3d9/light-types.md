---
description: La propiedad de tipo de luz define qué tipo de fuente de luz está usando.
ms.assetid: 7718383a-6e49-4ad2-acc1-fc8fec0d4844
title: Tipos de luz (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd451fcf45e67f1d789b7481fcc1884282d2018db98ab26d27481bec5277031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674433"
---
# <a name="light-types-direct3d-9"></a>Tipos de luz (Direct3D 9)

La propiedad de tipo de luz define qué tipo de fuente de luz está usando. El tipo de luz se establece mediante un valor de la enumeración [**D3DLIGHTTYPE**](./d3dlighttype.md) de C++ en el miembro Type de la estructura [**D3DLIGHT9 de**](d3dlight9.md) la luz. Hay tres tipos de luces en Direct3D: luces puntuales, focos destacados y luces direccionales. Cada tipo ilustra los objetos de una escena de forma diferente, con distintos niveles de sobrecarga computacional.

## <a name="point-light"></a>Luz puntual

Las luces de punto tienen color y posición dentro de una escena, pero no una sola dirección. Apagan la luz por igual en todas las direcciones, como se muestra en la ilustración siguiente.

![ilustración de la luz de punto](images/ptlight.png)

Una bombilla es un buen ejemplo de una luz de punto. Las luces de punto se ven afectadas por la atenuación y el intervalo, y encienden una malla en una base de vértice a vértice. Durante la iluminación, Direct3D usa la posición de la luz de punto en el espacio mundial y las coordenadas del vértice que se enciende para derivar un vector para la dirección de la luz y la distancia que ha recorrido la luz. Ambos se usan, junto con el vértice normal, para calcular la contribución de la luz a la iluminación de la superficie.

## <a name="directional-light"></a>Luz direccional

Las luces direccionales solo tienen color y dirección, no una posición. Emiten luz paralela. Esto significa que toda la luz generada por las luces direccionales viaja a través de una escena en la misma dirección. Imagine una luz direccional como una fuente de luz a una distancia casi infinita, como el sol. Las luces direccionales no se ven afectadas por la atenuación ni el intervalo, por lo que la dirección y el color que especifique son los únicos factores que se tienen en cuenta cuando Direct3D calcula los colores de los vértices. Debido al pequeño número de factores de iluminación, se trata de las luces que consumen menos cálculos.

## <a name="spotlight"></a>Foco

Los destacados tienen color, posición y dirección en los que emiten luz. La luz emitida a partir de un foco destacado se forma de un cono interior brillante y un cono exterior más grande, con la intensidad de la luz disminuyendo entre los dos, como se muestra en la ilustración siguiente.

![ilustración de un destacado con un cono interno y un cono externo](images/spotlt.png)

Los focos se ven afectados por la caída, atenuación e intervalo. Estos factores, así como la distancia que la luz recorre a cada vértice, se tienen en cuenta al calcular los efectos de iluminación de los objetos de una escena. Calcular estos efectos para cada vértice hace que los focos consuman más tiempo computacionalmente de todas las luces de Direct3D.

La [**estructura D3DLIGHT9**](d3dlight9.md) de C++ contiene tres miembros que solo usan los destacados. Estos miembros (Falloff, Theta y Phi) controlan lo grandes o pequeños que son los conos internos y externos de un objeto spotlight y cómo disminuye la luz entre ellos.

El valor de Theta es el ángulo radián del cono interno del foco, y el valor de Phi es el ángulo del cono exterior de la luz. El valor Falloff controla cómo disminuye la intensidad de la luz entre el borde exterior del cono interno y el borde interno del cono exterior. La mayoría de las aplicaciones establecen Falloff en 1.0 para crear una reserva que se produce uniformemente entre los dos conos, pero puede establecer otros valores según sea necesario.

En la ilustración siguiente se muestra la relación entre los valores de estos miembros y cómo pueden afectar a los conos de luz internos y externos de un foco.

![ilustración de cómo los valores de phi y theta se relacionan con los conos destacados](images/spotlt2.png)

Los focos emiten un cono de luz que tiene dos partes: un cono interno brillante y un cono exterior. La luz es más brillante en el cono interno y no está presente fuera del cono exterior, con atenuación de la intensidad de la luz entre las dos áreas. Este tipo de atenuación se conoce normalmente como "falloff".

La cantidad de luz que recibe un vértice se basa en la ubicación del vértice en los conos internos o externos. Direct3D calcula el producto de puntos del vector de dirección (L) del spotlight y el vector de la luz al vértice (D). Este valor es igual al coseno del ángulo entre los dos vectores y sirve como indicador de la posición del vértice que se puede comparar con los ángulos de cono de la luz para determinar dónde podría encontrarse el vértice en los conos internos o externos. En la ilustración siguiente se proporciona una representación gráfica de la asociación entre estos dos vectores.

![ilustración del vector de dirección de spotlight y el vector desde el vértice hasta el punto de destacado](images/spotalg1.png)

El sistema compara este valor con el coseno de los ángulos de cono interno y externo del foco. En la estructura [**D3DLIGHT9**](d3dlight9.md) de la luz, los miembros Theta y Phi representan los ángulos de cono totales para los conos internos y externos. Dado que la atenuación se produce a medida que el vértice se vuelve más alejado del centro de iluminación (en lugar del ángulo de cono total), el tiempo de ejecución divide estos ángulos de cono a la mitad antes de calcular sus cosenos.

Si el producto de puntos de los vectores L y D es menor o igual que el coseno del ángulo exterior del cono, el vértice se encuentra más allá del cono exterior y no recibe ninguna luz. Si el producto de puntos de L y D es mayor que el coseno del ángulo del cono interno, el vértice está dentro del cono interno y recibe la cantidad máxima de luz, teniendo en cuenta aún la atenuación a lo largo de la distancia. Si el vértice está en algún lugar entre las dos regiones, la reserva se calcula con la ecuación siguiente.

![fórmula para la intensidad de la luz en el vértice, después de la caída](images/falloff.png)

Donde:

-   I <sub>f es</sub> de intensidad ligera después de la caída
-   Alfa es el ángulo entre los vectores L y D
-   Theta es el ángulo de cono interno
-   Phi es el ángulo exterior del cono
-   p es la reserva

Esta fórmula genera un valor entre 0,0 y 1,0 que escala la intensidad de la luz en el vértice para tener en cuenta la caída. También se aplica la atenuación como factor de la distancia del vértice con respecto a la luz. En el gráfico siguiente se muestra cómo distintos valores de reserva pueden afectar a la curva de reserva.

![gráfico de intensidad de la luz frente a la distancia del vértice desde la luz](images/fallgraf.png)

El efecto de varios valores falloff en la iluminación real es sutil y se incurre en una pequeña penalización del rendimiento al dar forma a la curva de reserva con valores de reserva distintos de 1,0. Por estos motivos, este valor normalmente se establece en 1.0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 
