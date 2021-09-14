---
description: La mayoría de las texturas, como los mapas de bits, son una matriz bidimensional de valores de color.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf4c886c187aaa2218508a180e23644a544739
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358868"
---
# <a name="texture-coordinates-direct3d-9"></a>Coordenadas de textura (Direct3D 9)

La mayoría de las texturas, como los mapas de bits, son una matriz bidimensional de valores de color. Las texturas de mapa de entorno cúbicas son una excepción. Para obtener más información, [vea Asignación de entorno cúbica (Direct3D 9).](cubic-environment-mapping.md) Los valores de color individuales se denominan elemento de textura o texel. Cada texel tiene una dirección única en la textura. La dirección se puede pensar en como un número de columna y fila, que se etiquetan como usted y v respectivamente en la ilustración siguiente.

![ilustración de una dirección de texel como números de columna y fila](images/uvcoordinates.jpg)

Las coordenadas de textura están en el espacio de textura. Es decir, son relativos a la ubicación (0,0) de la textura. Cuando se aplica una textura a una primitiva en un espacio 3D, sus direcciones de textura se deben asignar a coordenadas de objeto. A continuación, deben traducirse en coordenadas de pantalla o ubicaciones de píxeles.

## <a name="mapping-texels-to-screen-space"></a>Asignación de elementos de textura al espacio de pantalla

Direct3D asigna los elementos de textura del espacio de textura directamente a píxeles en el espacio de pantalla, omitiendo el paso intermedio para una mayor eficacia. Este proceso de asignación es realmente una asignación inversa. Es decir, para cada píxel del espacio de pantalla, se calcula la posición de textura correspondiente en el espacio de textura. Se muestrea el color de textura en o alrededor de ese punto. El proceso de muestreo se denomina filtrado de textura. Para obtener más información, vea [Filtrado de texturas (Direct3D 9).](texture-filtering.md)

Cada texel de una textura se puede especificar mediante su coordenada de texel. Sin embargo, para asignar elementos de textura a primitivos, Direct3D requiere un intervalo uniforme de direcciones para todos los elementos de textura de todas las texturas. Por lo tanto, usa un esquema de direccionamiento genérico en el que todas las direcciones de textura se encuentran en el intervalo de 0,0 a 1,0, ambos inclusive. Las aplicaciones direct3D especifican coordenadas de textura en términos de los valores de you,v, de forma muy parecido a las coordenadas cartesianas 2D que se especifican en términos de coordenadas x,y. Técnicamente, el sistema puede procesar las coordenadas de textura fuera del intervalo de 0.0 y 1.0, y lo hace mediante los parámetros establecidos para el direccionamiento de textura. Para obtener más información, vea [Modos de direccionamiento de textura (Direct3D 9).](texture-addressing-modes.md)

Como resultado, las direcciones de textura idénticas se pueden asignar a diferentes coordenadas de texel en diferentes texturas. En la ilustración siguiente, la dirección de textura es (0.5,1.0). Sin embargo, dado que las texturas tienen tamaños diferentes, la dirección de textura se asigna a diferentes elementos de textura. La textura 1, a la izquierda, es 5x5. La dirección de textura (0,5,1.0) se asigna a texel (2,4). La textura 2, a la derecha, es 7x7. La dirección de textura (0,5,1.0) se asigna a texel (3,6).

![ilustración de la misma asignación de direcciones de textura a diferentes elementos de textura en diferentes texturas](images/texadr1.png)

En la ilustración siguiente se muestra una versión simplificada del proceso de asignación de elementos de textura. Es cierto que este ejemplo es muy sencillo. Para obtener información más detallada, vea [Asignación directa de texeles a píxeles (Direct3D 9).](directly-mapping-texels-to-pixels.md)

![ilustración de píxel (un cuadrado de color) que se asigna al espacio de objetos](images/texadr2.png)

En este ejemplo, un píxel, que se muestra a la izquierda de la ilustración, se idealiza en un cuadrado de color. Las direcciones de las cuatro esquinas del píxel se asignan a la primitiva 3D en el espacio de objetos. La forma del píxel suele estar distorsionada debido a la forma de la primitiva en el espacio 3D y al ángulo de visualización. A continuación, las esquinas del área de superficie de la primitiva que corresponden a las esquinas del píxel se asignan al espacio de textura. El proceso de asignación vuelve a distorsionar la forma del píxel, que es común. El valor de color final del píxel se calcula a partir de los elementos de textura de la región a la que se asigna el píxel. Al establecer el método de filtrado de textura, se determina el método que usa Direct3D para llegar al color de píxel. Para obtener más información, vea [Filtrado de texturas (Direct3D 9).](texture-filtering.md)

La aplicación puede asignar coordenadas de textura directamente a los vértices. Esta funcionalidad proporciona control sobre qué parte de una textura se asigna a una primitiva. Por ejemplo, supongamos que crea una primitiva rectangular que tiene exactamente el mismo tamaño que la textura de la ilustración siguiente. En este ejemplo, quiere que la aplicación asigne toda la textura a toda la pared. Las coordenadas de textura que la aplicación asigna a los vértices de la primitiva son (0.0,0.0), (1.0,0.0), (1.0,1.0) y (0.0,1.0).

![ilustración de una pared asignada a textura](images/texadr3.png)

Si decide reducir la altura de la pared a la mitad, puede distorsionar la textura para ajustarla a la pared más pequeña, o puede asignar coordenadas de textura que hacen que Direct3D use la mitad inferior de la textura.

Si decide distorsionar o escalar la textura para ajustarla a la pared más pequeña, el método de filtrado de texturas que use influirá en la calidad de la imagen. Para obtener más información, vea [Filtrado de texturas (Direct3D 9).](texture-filtering.md)

Si, en su lugar, decide asignar coordenadas de textura para que Direct3D use la mitad inferior de la textura para la pared más pequeña, las coordenadas de textura que la aplicación asigna a los vértices de la primitiva en este ejemplo son (0.0,0.5), (1.0,0.5), (1.0,1.0) y (0.0,1.0). Direct3D aplica la mitad inferior de la textura a la pared.

Es posible que las coordenadas de textura de un vértice sean mayores que 1,0. Al asignar coordenadas de textura a un vértice que no está en el intervalo de 0,0 a 1,0 inclusive, también debe establecer el modo de direccionamiento de textura. Para obtener más información, vea [Modos de direccionamiento de textura (Direct3D 9).](texture-addressing-modes.md)

## <a name="texture-coordinates-and-texture-stages"></a>Coordenadas de textura y fases de textura

Las coordenadas de textura se asocian a texturas mediante fases de textura. Las texturas se asignan a las fases de textura con SetTexture(stageIndex, pTexture). Vea [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Un código de formato de vértice flexible (FVF) puede definir hasta ocho conjuntos de coordenadas de textura. El usuario utiliza los datos de coordenadas de textura en los datos del vértice. Se hace referencia a los datos con un índice de base cero: 0 - 7. Hay hasta ocho fases de mezcla de textura. Una textura está asociada a una fase determinada mediante SetTexture( stageIndex, pTexture).

Una vez hecho esto, cualquier fase puede usar cualquier conjunto de coordenadas de textura. Cada conjunto de coordenadas está asociado a una fase mediante SetTextureStageState( stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex ). Vea [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). De este modo, las fases de mezcla se pueden configurar para usar cualquier textura y cualquier coordenadas de textura. Más de una fase puede usar las mismas texturas o coordenadas de textura.

En los temas siguientes se incluye información adicional.

-   [Formatos de coordenadas de textura (Direct3D 9)](texture-coordinate-formats.md)
-   [Procesamiento de coordenadas de textura (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
