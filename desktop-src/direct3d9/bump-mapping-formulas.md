---
description: Direct3D aplica las fórmulas siguientes a los componentes DU y DV en cada píxel de mapa de protuberancias.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Fórmulas de asignación de protuberancias (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569945"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Fórmulas de asignación de protuberancias (Direct3D 9)

Direct3D aplica las fórmulas siguientes a los componentes D<sub>U</sub> y D<sub>V</sub> en cada píxel del mapa de protuberancias.

![fórmulas de transformaciones de matriz de asignación de cambios](images/dudv-transform.png)

En estas fórmulas, las variables D<sub>U</sub> y D<sub>V</sub> se toman directamente de un píxel de mapa de incrementos y se transforman mediante una matriz 2x2 para generar los valores delta de salida D<sub>U</sub>' y D<sub>V</sub>'. El sistema usa los valores de salida para modificar las coordenadas de textura que direcciona el mapa de entorno en la siguiente fase de textura. Los coeficientes de la matriz de transformación se establecen a través de los estados de fase de textura D3DTSS \_ BUMPENVMAT00, D3DTSS \_ \_ BUMPENVMAT10, D3DTSS BUMPENVMAT01 y D3DTSS \_ BUMPENVMAT11.

Además de los valores delta you y v, el sistema puede calcular un valor de luminosidad que usa para modular el color del mapa de entorno en la siguiente fase de mezcla, como se muestra en la fórmula siguiente.

![fórmula para la luminosidad de salida, calculada a partir del factor de escala y el desplazamiento](images/l-transform.png)

En esta fórmula, L' es la luminosidad de salida que se está calculando. La variable L es el valor de luminosidad tomado de un píxel de mapa de protuberancia, que se multiplica por el factor de escala, S y el desplazamiento por el valor de la variable O. Los estados de fase de textura D3DTSS \_ BUMPENVLSCALE y D3DTSS BUMPENVLOFFSET controlan los valores de las variables S y O de \_ la fórmula. Esta fórmula solo se aplica cuando la operación de combinación de texturas para la fase que contiene el mapa de protuberancias se establece en D3DTOP \_ BUMPENVMAPLUMINANCE. Cuando se usa D3DTOP BUMPENVMAP, el sistema usa un \_ valor de 1,0 para L'.

Después de calcular los valores delta de salida D<sub>U</sub>' y D<sub>V</sub>', el sistema los agrega a las coordenadas de textura en la siguiente fase de textura y modular el color elegido por la luminosidad para generar el color aplicado al polígono.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de protuberancias](bump-mapping.md)
</dt> </dl>

 

 



