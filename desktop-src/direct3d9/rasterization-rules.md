---
description: A menudo, los puntos especificados para los vértices no coinciden exactamente con los píxeles de la pantalla. Cuando esto sucede, Direct3D aplica reglas de rasterización de triángulo para decidir qué píxeles se aplican a un triángulo determinado.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Reglas de rasterización (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279716"
---
# <a name="rasterization-rules-direct3d-9"></a>Reglas de rasterización (Direct3D 9)

A menudo, los puntos especificados para los vértices no coinciden exactamente con los píxeles de la pantalla. Cuando esto sucede, Direct3D aplica reglas de rasterización de triángulo para decidir qué píxeles se aplican a un triángulo determinado.

-   [Reglas de rasterización de triángulos](#triangle-rasterization-rules)
-   [Reglas de punto y línea](#point-and-line-rules)
-   [Reglas de Sprite de punto](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Reglas de rasterización de triángulos

Direct3D usa una Convención de llenado superior izquierda para rellenar la geometría. Se trata de la misma Convención que se usa para los rectángulos en GDI y OpenGL. En Direct3D, el centro del píxel es el punto decisivo. Si el centro está dentro de un triángulo, el píxel es parte del triángulo. Los centros de píxeles están en coordenadas de enteros.

Esta descripción de las reglas de rasterización triangular que usa Direct3D no se aplica necesariamente a todo el hardware disponible. Las pruebas pueden revelar pequeñas variaciones en la implementación de estas reglas.

En la ilustración siguiente se muestra un rectángulo cuya esquina superior izquierda está en (0,0) y cuya esquina inferior derecha está en (5, 5). Este rectángulo rellena 25 píxeles, tal y como cabría esperar. El ancho del rectángulo se define como Right menos a la izquierda. El alto se define como inferior menos superior.

![Ilustración de un cuadrado numerado dividido en seis filas y columnas](images/pixmap.png)

En la Convención de llenado superior izquierda, la *parte superior* se refiere a la ubicación vertical de los intervalos horizontales y a la *izquierda* hace referencia a la ubicación horizontal de los píxeles dentro de un intervalo. Un borde no puede ser un borde superior a menos que sea horizontal. En general, la mayoría de los triángulos solo tienen bordes izquierdo y derecho. En la ilustración siguiente se muestra un borde superior y un borde derecho.

![Ilustración de un cuadrado numerado que contiene dos triángulos](images/triedge.png)

La Convención de llenado superior izquierda determina la acción realizada por Direct3D cuando un triángulo pasa a través del centro de un píxel. En la ilustración siguiente se muestran dos triángulos, uno en (0,0), (5, 0) y (5, 5), y el otro en (0, 5), (0, 0) y (5, 5). En este caso, el primer triángulo obtiene 15 píxeles (se muestra en negro), mientras que el segundo obtiene solo 10 píxeles (mostrados en gris) porque el borde compartido es el borde izquierdo del primer triángulo.

![Ilustración de un cuadrado numerado que muestra dos triángulos](images/twotris.png)

Si define un rectángulo con la esquina superior izquierda en (0,5, 0,5) y la esquina inferior derecha en (2,5, 4,5), el punto central de este rectángulo está en (1,5, 2,5). Cuando el rasterizador de Direct3D tessellates este rectángulo, el centro de cada píxel es inequívoca dentro de cada uno de los cuatro triángulos, y no es necesaria la Convención de llenado superior izquierda. En la ilustración siguiente se muestra esto. Los píxeles del rectángulo se etiquetan según el triángulo en el que Direct3D los incluye.

![Muestra un cuadrado numerado que contiene un rectángulo que se divide en cuatro triángulos.](images/noambig.png)

Si mueve el rectángulo de la ilustración anterior para que la esquina superior izquierda esté en (1,0, 1,0), la esquina inferior derecha en (3,0, 5,0) y su punto central en (2,0, 3,0), Direct3D aplica la Convención de llenado superior izquierda. La mayoría de los píxeles de este rectángulo ocupan el borde entre dos o más triángulos, como se muestra en la ilustración siguiente.

![Ilustración de un cuadrado numerado que contiene un rectángulo dividido en cuatro triángulos](images/fillrule.png)

En ambos rectángulos, los mismos píxeles se ven afectados, tal como se muestra en la siguiente ilustración.

![Ilustración de los píxeles afectados por los dos cuadrados numerados anteriores](images/samepix.png)

## <a name="point-and-line-rules"></a>Reglas de punto y línea

Los puntos se representan igual que los sprites de punto, que se representan como quadrilaterals alineados por pantalla y, por tanto, se ajustan a las mismas reglas que la representación de polígonos.

Las reglas de representación de líneas sin alias son exactamente iguales que las de [las líneas de GDI](../gdi/lines.md).

Para obtener información sobre la representación de líneas alisadas, vea [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Reglas de Sprite de punto

Los sprites de punto y los primitivos de revisión se rasterizan como si los primitivos estuviesen en primer lugar en triángulos y los triángulos resultantes se rasterizan. Para obtener más información, vea [sprites de punto (Direct3D 9)](point-sprites.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
