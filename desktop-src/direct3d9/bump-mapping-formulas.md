---
description: Direct3D aplica las siguientes fórmulas a los componentes DU y DV en cada píxel del mapa de rugosidad.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Fórmulas de asignación de rugosidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153577"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Fórmulas de asignación de rugosidad (Direct3D 9)

Direct3D aplica las siguientes fórmulas a los componentes D<sub>U</sub> y d<sub>V</sub> en cada píxel del mapa de rugosidad.

![fórmulas de transformaciones de matriz de asignación de rugosidad](images/dudv-transform.png)

En estas fórmulas, las variables D<sub>U</sub> y d<sub>V</sub> se toman directamente de un píxel de mapa de rugosidad y se transforman mediante una matriz de 2x2 para producir los valores Delta de salida D<sub>U</sub>' y d<sub>V</sub>'. El sistema utiliza los valores de salida para modificar las coordenadas de textura que abordan el mapa de entorno en la siguiente fase de textura. Los coeficientes de la matriz de transformación se establecen a través de los \_ Estados de fase D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 y D3DTSS \_ BUMPENVMAT11 Texture.

Además de los valores Delta y v, el sistema puede calcular un valor de luminancia que utiliza para modular el color del mapa de entorno en la siguiente fase de mezcla, como se muestra en la siguiente fórmula.

![fórmula para la luminancia de salida, calculada a partir del factor de escala y el desplazamiento](images/l-transform.png)

En esta fórmula, L ' es la luminancia de salida que se está calculando. La variable L es el valor de luminancia tomado de un píxel de mapa de rugosidad, que se multiplica por el factor de escala, S y el desplazamiento por el valor de la variable O. Los \_ Estados de la fase D3DTSS BUMPENVLSCALE y D3DTSS \_ BUMPENVLOFFSET Texture controlan los valores de las variables s y o de la fórmula. Esta fórmula solo se aplica cuando la operación de combinación de texturas de la fase que contiene el mapa de rugosidad está establecida en D3DTOP \_ BUMPENVMAPLUMINANCE. Cuando se usa D3DTOP \_ BUMPENVMAP, el sistema usa un valor de 1,0 para L '.

Después de calcular los valores Delta de salida D<sub>U</sub>' y d<sub>V</sub>', el sistema los agrega a las coordenadas de textura en la siguiente fase de textura y modula el color elegido por la luminancia para producir el color aplicado al polígono.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de rugosidad](bump-mapping.md)
</dt> </dl>

 

 



