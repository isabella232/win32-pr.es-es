---
description: A menudo, los puntos especificados para los vértices no coinciden exactamente con los píxeles de la pantalla. Cuando esto sucede, Direct3D aplica reglas de rasterización de triángulos para decidir qué píxeles se aplican a un triángulo determinado.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Reglas de rasterización (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d241248f5a69262129f60fc005582dc5e03b2a6931cf024bc4613d81558cdb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746706"
---
# <a name="rasterization-rules-direct3d-9"></a>Reglas de rasterización (Direct3D 9)

A menudo, los puntos especificados para los vértices no coinciden exactamente con los píxeles de la pantalla. Cuando esto sucede, Direct3D aplica reglas de rasterización de triángulos para decidir qué píxeles se aplican a un triángulo determinado.

-   [Reglas de rasterización de triángulos](#triangle-rasterization-rules)
-   [Reglas de punto y línea](#point-and-line-rules)
-   [Reglas de sprite de punto](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Reglas de rasterización de triángulos

Direct3D usa una convención de relleno de la parte superior izquierda para rellenar la geometría. Se trata de la misma convención que se usa para los rectángulos de GDI y OpenGL. En Direct3D, el centro del píxel es el punto de decisión. Si el centro está dentro de un triángulo, el píxel forma parte del triángulo. Los centros de píxeles están en coordenadas enteras.

Esta descripción de las reglas de rasterización de triángulos usadas por Direct3D no se aplica necesariamente a todo el hardware disponible. Las pruebas pueden descubrir pequeñas variaciones en la implementación de estas reglas.

En la ilustración siguiente se muestra un rectángulo cuya esquina superior izquierda está en (0, 0) y cuya esquina inferior derecha está en (5, 5). Este rectángulo rellena 25 píxeles, tal y como se esperaría. El ancho del rectángulo se define como derecha menos izquierda. El alto se define como inferior menos superior.

![ilustración de un cuadrado numerado dividido en seis filas y columnas](images/pixmap.png)

En la convención de relleno superior izquierdo, *la* parte superior  hace referencia a la ubicación vertical de los intervalos horizontales y la izquierda hace referencia a la ubicación horizontal de píxeles dentro de un intervalo. Un borde no puede ser un borde superior a menos que sea horizontal. En general, la mayoría de los triángulos solo tienen bordes izquierdo y derecho. En la ilustración siguiente se muestra un borde superior y un borde derecho.

![ilustración de un cuadrado numerado que contiene dos triángulos](images/triedge.png)

La convención de relleno de la parte superior izquierda determina la acción realizada por Direct3D cuando un triángulo pasa por el centro de un píxel. En la ilustración siguiente se muestran dos triángulos, uno en (0, 0), (5, 0) y (5, 5) y el otro en (0, 5), (0, 0) y (5, 5). En este caso, el primer triángulo obtiene 15 píxeles (que se muestra en negro), mientras que el segundo obtiene solo 10 píxeles (se muestra en gris) porque el borde compartido es el borde izquierdo del primer triángulo.

![ilustración de un cuadrado numerado que muestra dos triángulos](images/twotris.png)

Si define un rectángulo con su esquina superior izquierda en (0,5, 0,5) y su esquina inferior derecha en (2,5, 4,5), el punto central de este rectángulo está en (1,5, 2,5). Cuando el rasterizador de Direct3D tesola este rectángulo, el centro de cada píxel se encuentra inequívocamente dentro de cada uno de los cuatro triángulos y no se necesita la convención de relleno de la parte superior izquierda. En la ilustración siguiente se muestra esto. Los píxeles del rectángulo se etiquetan según el triángulo en el que Direct3D los incluye.

![Muestra un cuadrado numerado que contiene un rectángulo dividido en cuatro triángulos.](images/noambig.png)

Si mueve el rectángulo de la ilustración anterior para que su esquina superior izquierda esté en (1.0, 1.0), su esquina inferior derecha en (3.0, 5.0) y su punto central en (2.0, 3.0), Direct3D aplica la convención de relleno superior izquierdo. La mayoría de los píxeles de este rectángulo delimitan el borde entre dos o más triángulos, como se muestra en la ilustración siguiente.

![ilustración de un cuadrado numerado que contiene un rectángulo dividido en cuatro triángulos](images/fillrule.png)

En ambos rectángulos, se ven afectados los mismos píxeles, como se muestra en la ilustración siguiente.

![ilustración de píxeles afectados por los dos cuadrados numerados anteriores](images/samepix.png)

## <a name="point-and-line-rules"></a>Reglas de punto y línea

Los puntos se representan igual que los sprites de punto, que se representan como cuadráteros alineados con la pantalla y, por tanto, se adhieren a las mismas reglas que la representación de polígonos.

Las reglas de representación de líneas no suavizadas son exactamente las mismas que las de las [líneas GDI.](../gdi/lines.md)

Para obtener información sobre la representación de líneas suavizadas, vea [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Reglas de sprite de punto

Los sprites de punto y los primitivos de revisión se rasterizan como si los primitivos se hubieran teselado primero en triángulos y los triángulos resultantes se rasterizaran. Para obtener más información, [vea Sprites de punto (Direct3D 9).](point-sprites.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
