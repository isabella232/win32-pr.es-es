---
description: La propiedad Light Type define el tipo de fuente de luz que se está usando.
ms.assetid: 7718383a-6e49-4ad2-acc1-fc8fec0d4844
title: Tipos de luz (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ae2c7fd5380b0f604181f36d784afe3f3fc3ff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079876"
---
# <a name="light-types-direct3d-9"></a>Tipos de luz (Direct3D 9)

La propiedad Light Type define el tipo de fuente de luz que se está usando. El tipo de luz se establece mediante un valor de la enumeración de [**D3DLIGHTTYPE**](./d3dlighttype.md) C++ en el miembro de tipo de la estructura [**D3DLIGHT9**](d3dlight9.md) de la luz. Hay tres tipos de luces en las luces de punto de Direct3D, los focos y las luces direccionales. Cada tipo ilumina los objetos de una escena de forma diferente, con distintos niveles de sobrecarga computacional.

## <a name="point-light"></a>Luz puntual

Las luces puntuales tienen color y posición dentro de una escena, pero no una dirección única. Declaran de forma similar en todas las direcciones, tal como se muestra en la siguiente ilustración.

![Ilustración de luz puntual](images/ptlight.png)

Una bombilla es un buen ejemplo de una luz puntual. Las luces de punto se ven afectadas por la atenuación y el intervalo, y iluminan una malla en cada vértice. Durante la iluminación, Direct3D usa la posición de la luz de punto en el espacio universal y las coordenadas del vértice que se iluminan para derivar un vector para la dirección de la luz y la distancia que la luz ha viajado. Ambos se usan, junto con el vértice normal, para calcular la contribución de la luz a la iluminación de la superficie.

## <a name="directional-light"></a>Luz direccional

Las luces direccionales solo tienen color y dirección, no posición. Emiten luz paralela. Esto significa que toda la luz generada por las luces direccionales viaja a través de una escena en la misma dirección. Imagínese una luz direccional como fuente de luz casi infinita, como el sol. Las luces direccionales no se ven afectadas por la atenuación o el intervalo, por lo que la dirección y el color que especifique son los únicos factores que se tienen en cuenta cuando Direct3D calcula los colores de los vértices. Debido al pequeño número de factores de iluminación, se trata de las luces menos intensivas de cálculo que se usan.

## <a name="spotlight"></a>Principales

Los Spotlight tienen color, posición y dirección en los que emiten luz. La luz procedente de un foco se compone de un cono interior brillante y un cono exterior más grande, con la intensidad de la luz que disminuye entre los dos, tal como se muestra en la siguiente ilustración.

![Ilustración de un foco con un cono interior y un cono exterior](images/spotlt.png)

Los focos se ven afectados por la disminución, la atenuación y el intervalo. Estos factores, así como la luz de distancia que viaja hacia cada vértice, se indican al calcular los efectos de iluminación de los objetos de una escena. Al calcular estos efectos para cada vértice, se destaca la mayor parte del tiempo de cálculo de todas las luces de Direct3D.

La estructura de C++ [**D3DLIGHT9**](d3dlight9.md) contiene tres miembros que solo usan los focos. Estos miembros (deducciones, Theta y PHI) controlan el tamaño de los conos internos y exteriores de un objeto de la luz y el modo en que se reduce la luz.

El valor Theta es el ángulo en radianes del cono interior del foco y el valor de la PHI es el ángulo del cono exterior de la luz. El valor de difuminación controla cómo se reduce la intensidad de la luz entre el borde exterior del cono interior y el borde interno del cono exterior. La mayoría de las aplicaciones establecen la disminución en 1,0 para crear una caída que se produce uniformemente entre los dos conos, pero puede establecer otros valores según sea necesario.

En la ilustración siguiente se muestra la relación entre los valores de estos miembros y cómo pueden afectar a los conos internos y exteriores de la luz.

![Ilustración de cómo se relacionan los valores de Phi y Theta con los conos destacados](images/spotlt2.png)

Los focos emiten un cono de luz que tiene dos partes: un cono interior brillante y un cono exterior. La luz es más brillante en el cono interior y no está presente fuera del cono exterior, con una luminosidad de intensidad clara entre las dos áreas. Este tipo de atenuación se conoce comúnmente como disminución.

La cantidad de luz que recibe un vértice se basa en la ubicación del vértice en los conos internos o externos. Direct3D calcula el producto de punto del vector de dirección (L) del foco y el vector de la luz al vértice (D). Este valor es igual al coseno del ángulo entre los dos vectores y sirve como indicador de la posición del vértice que se puede comparar con los ángulos cónicos de la luz para determinar dónde podría encontrarse el vértice en los conos internos o externos. En la ilustración siguiente se proporciona una representación gráfica de la asociación entre estos dos vectores.

![Ilustración del vector de dirección de Spotlight y el vector desde el vértice hasta el foco](images/spotalg1.png)

El sistema compara este valor con el coseno de los ángulos de cono interno y externo del foco. En la estructura [**D3DLIGHT9**](d3dlight9.md) de la luz, los miembros de Theta y Phi representan los ángulos de cono totales de los conos internos y exteriores. Dado que la atenuación se produce cuando el vértice se vuelve más alejado del centro de iluminación (en lugar de en el ángulo total del cono), el tiempo de ejecución divide estos ángulos cónicos a la mitad antes de calcular sus cosenos.

Si el producto del punto de vectores L y D es menor o igual que el coseno del ángulo del cono externo, el vértice está más allá del cono exterior y no recibe luz. Si el producto del punto de L y D es mayor que el coseno del ángulo del cono interno, el vértice está dentro del cono interior y recibe la cantidad máxima de luz, lo que sigue teniendo en cuenta la atenuación a través de la distancia. Si el vértice está en alguna parte entre las dos regiones, la caída se calcula con la siguiente ecuación.

![fórmula para la intensidad de la luz en el vértice, después de la caída](images/falloff.png)

Donde:

-   I <sub>f</sub> es la intensidad de la luz después de la caída
-   Alfa es el ángulo entre vectores L y D
-   Theta es el ángulo del cono interior
-   La PHI es el ángulo de cono externo
-   p es la disminución

Esta fórmula genera un valor entre 0,0 y 1,0 que escala la intensidad de la luz en el vértice para tener en cuenta la disminución. También se aplica la atenuación como factor de la distancia del vértice a la luz. En el gráfico siguiente se muestra cómo diferentes valores de difuminación pueden afectar a la curva de difuminación.

![gráfico de intensidad de la luz frente a la distancia del vértice de la luz](images/fallgraf.png)

El efecto de los distintos valores de difuminación en la iluminación real es sutil, y se incurre en una pequeña reducción del rendimiento dando forma a la curva de difuminación con valores de disminución distintos de 1,0. Por estos motivos, este valor se establece normalmente en 1,0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 
