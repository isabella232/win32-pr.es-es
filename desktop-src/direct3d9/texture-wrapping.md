---
description: En Resumen, el ajuste de textura cambia la manera básica en que Direct3D rasteriza los polígonos con textura mediante las coordenadas de textura especificadas para cada vértice.
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Ajuste de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7c0f8cb6d7793536999d5f3df128849572d3dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537216"
---
# <a name="texture-wrapping-direct3d-9"></a>Ajuste de textura (Direct3D 9)

En Resumen, el ajuste de textura cambia la manera básica en que Direct3D rasteriza los polígonos con textura mediante las coordenadas de textura especificadas para cada vértice. Mientras se rasteriza un polígono, el sistema se interpola entre las coordenadas de textura de cada uno de los vértices del polígono para determinar el textura que se debe usar para cada píxel del polígono. Normalmente, el sistema trata la textura como un plano 2D, interpolando New textura tomando la ruta más corta del punto A dentro de una textura al punto B. Si el punto A representa la posición u, v (0,8, 0,1) y el punto B está en (0.1, 0.1), la línea de interpolación es similar al diagrama siguiente.

![diagrama de una línea de interpolación entre dos puntos](images/interp1.png)

Tenga en cuenta que la distancia más corta entre A y B en esta ilustración se ejecuta aproximadamente a la mitad de la textura. La habilitación del ajuste de coordenadas u-textura o v-Texture cambia el modo en que Direct3D percibe la ruta más corta entre las coordenadas de textura en la dirección u y la dirección de v. Por definición, el ajuste de textura hace que el rasterizador tome la ruta más corta entre los conjuntos de coordenadas de textura, suponiendo que 0,0 y 1,0 son coincidentes. El último bit es la parte complicada: puede imaginar que habilitar el ajuste de textura en una dirección hace que el sistema trate una textura como si estuviera encapsulada alrededor de un cilindro. Por ejemplo, considere el siguiente diagrama.

![diagrama de una textura y dos puntos rodeados por un cilindro](images/interp2.png)

En la ilustración anterior se muestra cómo el ajuste en la dirección u afecta al modo en que el sistema interpola las coordenadas de textura. Con los mismos puntos que en el ejemplo de texturas normales, o no ajustadas, puede ver que la ruta más corta entre los puntos A y B ya no se encuentra en medio de la textura; ahora se encuentra en el borde donde 0,0 y 1,0 existen juntos. El ajuste en la dirección v es similar, con la salvedad de que ajusta la textura en torno a un cilindro que está en su lado. El ajuste en la dirección u y en la dirección de v es más complejo. En esta situación, puede imaginar la textura como un toroide o un toroide.

La aplicación práctica más común para el ajuste de textura es realizar la asignación de entorno. Normalmente, un objeto con textura con un mapa de entorno parece muy reflectante y muestra una imagen reflejada del entorno del objeto en la escena. En este debate, Imagínese una habitación con cuatro paredes, cada una pintada con una letra R, G, B, y y los colores correspondientes: rojo, verde, azul y amarillo. El mapa de entorno para este tipo de espacio sencillo podría ser similar al de la siguiente ilustración.

![Ilustración de las franjas verticales de rojo, verde, azul y amarillo](images/envmap.png)

Imagine que el límite superior de la habitación se mantiene en un pilar perfectamente reflectante de cuatro lados. Asignar la textura del mapa del entorno al pilar es sencilla; la apariencia del Pilar es tan sencilla como para reflejar las letras y los colores. En el diagrama siguiente se muestra un fotograma de conexión del pilar con las coordenadas de textura aplicables que aparecen cerca de los vértices superiores. Los marinos en los que se cruzarán los bordes de la textura se muestran con una línea de puntos.

![diagrama de un rectángulo con una línea de puntos bisección](images/seam.png)

Con el ajuste habilitado en la dirección u, el pilar con textura muestra los colores y los símbolos del mapa del entorno adecuadamente y, en las costuras de la parte delantera de la textura, el rasterizador elige correctamente la ruta más corta entre las coordenadas de textura, suponiendo que las coordenadas u 0,0 y 1,0 compartan la misma ubicación. El pilar con textura tiene un aspecto similar al de la siguiente ilustración.

![Ilustración de un pilar compuesto por cuadrantes rojo, verde, azul y amarillo](images/tex-seam.png)

Si el ajuste de textura no está habilitado, el rasterizador no se interpola en la dirección necesaria para generar una imagen reflejada más increíble. En su lugar, el área de la parte delantera del Pilar contiene una versión comprimida horizontalmente de la textura entre las coordenadas u 0,175 y 0,875, a medida que pasan a través del centro de la textura. El efecto de ajuste es Ruined.

## <a name="using-texture-wrapping"></a>Usar el ajuste de textura

Para habilitar el ajuste de textura, llame al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) tal y como se muestra en el ejemplo de código siguiente.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



El primer parámetro aceptado por [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) es un estado de representación que se va a establecer. Especifique uno de los \_ valores enumerados de D3DRS WRAP0 a D3DRS \_ WRAP7 que especifican el nivel de textura para el que se va a establecer el ajuste. Especifique las marcas de D3DWRAPCOORD \_ 0 a D3DWRAPCOORD \_ 3 en el segundo parámetro para habilitar el ajuste de textura en la dirección correspondiente o combínelo para habilitar el ajuste en varias direcciones. Si omite una marca, se deshabilita el ajuste de textura en la dirección correspondiente. Para deshabilitar el ajuste de textura para un conjunto de coordenadas de textura, establezca el valor del estado de representación correspondiente en 0.

No confunda el ajuste de textura con los modos de direccionamiento de textura con el mismo nombre. El ajuste de textura se realiza antes del direccionamiento de textura. Asegúrese de que los datos de ajuste de textura no contengan ninguna coordenadas de textura fuera del intervalo de \[ 0,0, 1,0, ya que esto producirá \] resultados no definidos. Para obtener más información sobre el direccionamiento de textura, vea [modos de direccionamiento de textura (Direct3D 9)](texture-addressing-modes.md).

## <a name="displacement-map-wrapping"></a>Ajuste del mapa de desplazamiento

El motor tesselation interpola los mapas de desplazamiento. Dado que no se puede especificar el modo de ajuste para el motor de teselación, no se puede realizar el ajuste de textura con los mapas de desplazamiento. Una aplicación puede utilizar un conjunto de vértices que fuerza la interpolación en cualquier dirección. La aplicación también puede especificar la interpolación que se va a realizar como una interpolación lineal simple.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
