---
description: La mayoría de las texturas, como los mapas de bits, son una matriz bidimensional de valores de color.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf4c886c187aaa2218508a180e23644a544739
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495772"
---
# <a name="texture-coordinates-direct3d-9"></a>Coordenadas de textura (Direct3D 9)

La mayoría de las texturas, como los mapas de bits, son una matriz bidimensional de valores de color. Las texturas del mapa del entorno cúbica son una excepción. Para obtener más información, vea [asignación de entorno cúbica (Direct3D 9)](cubic-environment-mapping.md). Los valores de color individuales se denominan elementos de textura o textura. Cada textura tiene una dirección única en la textura. La dirección se puede considerar como un número de columna y fila, que se etiquetan y v respectivamente en la siguiente ilustración.

![Ilustración de una dirección textura como números de columna y fila](images/uvcoordinates.jpg)

Las coordenadas de textura están en el espacio de textura. Es decir, son relativas a la ubicación (0,0) en la textura. Cuando se aplica una textura a una primitiva en el espacio 3D, sus direcciones textura deben estar asignadas a coordenadas de objetos. A continuación, se deben traducir en coordenadas de pantalla o en ubicaciones de píxeles.

## <a name="mapping-texels-to-screen-space"></a>Asignación de textura al espacio de pantalla

Direct3D asigna textura en el espacio de textura directamente a píxeles en el espacio de pantalla, omitiendo el paso intermedio para mayor eficacia. Este proceso de asignación es realmente una asignación inversa. Es decir, para cada píxel del espacio de pantalla, se calcula la posición textura correspondiente en el espacio de textura. Se muestrea el color de la textura en el punto o en torno a este. El proceso de muestreo se denomina filtrado de textura. Para obtener más información, vea [filtrado de textura (Direct3D 9)](texture-filtering.md).

Cada textura de una textura se puede especificar mediante su coordenada textura. Sin embargo, para asignar textura a primitivos, Direct3D requiere un intervalo de direcciones uniforme para todos los textura de todas las texturas. Por lo tanto, usa un esquema de direccionamiento genérico en el que todas las direcciones textura están en el intervalo de 0,0 a 1,0, ambos incluidos. Las aplicaciones de Direct3D especifican las coordenadas de textura en función de los valores de las coordenadas x, y, al igual que las coordenadas cartesianas 2D se especifican en términos de coordenadas x, y. Técnicamente, el sistema puede procesar realmente las coordenadas de textura fuera del intervalo de 0,0 y 1,0, y lo hace mediante los parámetros que se establecen para el direccionamiento de textura. Para obtener más información, vea [modos de direccionamiento de textura (Direct3D 9)](texture-addressing-modes.md).

El resultado es que las direcciones de textura idénticas se pueden asignar a distintas coordenadas textura en distintas texturas. En la ilustración siguiente, la dirección de la textura es (0.5, 1.0). Sin embargo, como las texturas tienen tamaños diferentes, la dirección de textura se asigna a diferentes textura. La textura 1, a la izquierda, es 5x5. La dirección de textura (0.5, 1.0) se asigna a textura (2, 4). La textura 2, a la derecha, es 7x7. La dirección de textura (0.5, 1.0) se asigna a textura (3, 6).

![Ilustración de la misma asignación de dirección de textura a diferentes textura en distintas texturas](images/texadr1.png)

En la siguiente ilustración se muestra una versión simplificada del proceso de asignación de textura. En realidad, este ejemplo es muy sencillo. Para obtener información más detallada, consulte [asignación directa de textura a píxeles (Direct3D 9)](directly-mapping-texels-to-pixels.md).

![Ilustración de píxel (un cuadrado de color) que está asignada al espacio de objeto](images/texadr2.png)

En este ejemplo, un píxel, que se muestra a la izquierda de la ilustración, es ideal en un cuadrado de color. Las direcciones de las cuatro esquinas del píxel se asignan al primitivo 3D en el espacio de objeto. La forma del píxel suele distorsionarse debido a la forma de la primitiva en el espacio 3D y debido al ángulo de visualización. Las esquinas del área expuesta en el primitivo que corresponden a las esquinas del píxel se asignan a un espacio de textura. El proceso de asignación distorsiona la forma del píxel de nuevo, lo que es común. El valor de color final del píxel se calcula a partir del textura de la región a la que se asigna el píxel. Puede determinar el método que Direct3D usa para llegar al color de píxel al establecer el método de filtrado de textura. Para obtener más información, vea [filtrado de textura (Direct3D 9)](texture-filtering.md).

La aplicación puede asignar coordenadas de textura directamente a los vértices. Esta funcionalidad le permite controlar qué parte de una textura se asigna a una primitiva. Por ejemplo, suponga que crea un primitivo rectangular que tiene exactamente el mismo tamaño que la textura de la siguiente ilustración. En este ejemplo, desea que la aplicación asigne la textura completa a toda la pared. La textura coordina la aplicación que se asigna a los vértices de la primitiva son (0,0, 0,0), (1,0, 0,0), (1,0, 1,0) y (0,0, 1,0).

![Ilustración de una pared asignada por textura](images/texadr3.png)

Si decide reducir la altura de la pared una vez a la mitad, puede distorsionar la textura para que quepa en la pared más pequeña, o puede asignar coordenadas de textura que hagan que Direct3D use la mitad inferior de la textura.

Si decide distorsionar o escalar la textura para que se ajuste a la pared más pequeña, el método de filtrado de textura que use influirá en la calidad de la imagen. Para obtener más información, vea [filtrado de textura (Direct3D 9)](texture-filtering.md).

Si, en su lugar, decide asignar coordenadas de textura para que Direct3D use la mitad inferior de la textura para la pared más pequeña, la textura coordina la aplicación que se asigna a los vértices de la primitiva en este ejemplo son (0,0, 0.5), (1,0, 0.5), (1.0, 1.0) y (0,0, 1,0). Direct3D aplica la mitad inferior de la textura a la pared.

Es posible que las coordenadas de textura de un vértice sean mayores que 1,0. Cuando se asignan coordenadas de textura a un vértice que no está en el intervalo de 0,0 a 1,0, ambos inclusive, también se debe establecer el modo de direccionamiento de textura. Para obtener más información, vea [modos de direccionamiento de textura (Direct3D 9)](texture-addressing-modes.md).

## <a name="texture-coordinates-and-texture-stages"></a>Coordenadas de textura y fases de textura

Las coordenadas de textura están asociadas a texturas mediante fases de textura. Las texturas se asignan a las fases de textura con SetTexture (stageIndex, pTexture). Vea [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Un código de formato de vértice flexible (FVF) puede definir hasta ocho conjuntos de coordenadas de textura. El usuario proporciona los datos de coordenadas de textura en los datos de vértices. Se hace referencia a los datos con un índice basado en cero: 0-7. Hay hasta ocho fases de fusión de texturas. Una textura se asocia a una fase determinada mediante SetTexture (stageIndex, pTexture).

Una vez hecho esto, cualquier fase puede utilizar cualquier conjunto de coordenadas de textura. Cada conjunto de coordenadas está asociado a una fase mediante SetTextureStageState (stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex). Vea [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). De este modo, las fases de fusión se pueden configurar para usar cualquier textura y cualquier coordenadas de textura. Más de una fase puede usar las mismas texturas o coordenadas de textura.

En los temas siguientes se incluye información adicional.

-   [Formatos de coordenadas de textura (Direct3D 9)](texture-coordinate-formats.md)
-   [Procesamiento de coordenadas de textura (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
