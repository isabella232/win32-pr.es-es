---
description: En resumen, el ajuste de textura cambia la forma básica en que Direct3D rasteriza los polígonos con textura mediante las coordenadas de textura especificadas para cada vértice.
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Ajuste de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c29ebe78bcfa237f46eacb247432185adedd1e53ae0774e767807269bb3bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984759"
---
# <a name="texture-wrapping-direct3d-9"></a>Ajuste de textura (Direct3D 9)

En resumen, el ajuste de textura cambia la forma básica en que Direct3D rasteriza los polígonos con textura mediante las coordenadas de textura especificadas para cada vértice. Al rasterizar un polígono, el sistema interpola entre las coordenadas de textura en cada uno de los vértices del polígono para determinar los elementos de textura que se deben usar para cada píxel del polígono. Normalmente, el sistema trata la textura como un plano 2D, interpolando los nuevos elementos de textura tomando la ruta más corta desde el punto A dentro de una textura hasta el punto B. Si el punto A representa la posición u, v (0.8, 0.1) y el punto B está en (0.1,0.1), la línea de interpolación será similar al diagrama siguiente.

![diagrama de una línea de interpolación entre dos puntos](images/interp1.png)

Tenga en cuenta que la distancia más corta entre A y B en esta ilustración se ejecuta aproximadamente a través del centro de la textura. La habilitación del ajuste de coordenadas de u-texture o v-texture cambia la forma en que Direct3D percibe la ruta más corta entre las coordenadas de textura en la dirección U y la dirección V. Por definición, el ajuste de textura hace que el rasterizador tome la ruta más corta entre los conjuntos de coordenadas de textura, suponiendo que 0,0 y 1,0 sean coincidentes. El último bit es la parte complicada: Puede imaginar que habilitar el ajuste de textura en una dirección hace que el sistema trate una textura como si estuviera encapsulada alrededor de un cilindro. Por ejemplo, considere el siguiente diagrama.

![diagrama de una textura y dos puntos encapsulados alrededor de un cilindro](images/interp2.png)

En la ilustración anterior se muestra cómo el ajuste en la dirección u - afecta a cómo el sistema interpola las coordenadas de textura. Con los mismos puntos que en el ejemplo para texturas normales o no encapsuladas, puede ver que la ruta más corta entre los puntos A y B ya no se encuentra en el centro de la textura. ahora está a través del borde donde 0.0 y 1.0 existen juntos. El ajuste en la dirección v es similar, salvo que encapsula la textura alrededor de un cilindro que se encuentra a su lado. El ajuste tanto en la dirección U como en la dirección V es más complejo. En esta situación, puede imaginar la textura como un torus o un anillo.

La aplicación práctica más común para el ajuste de texturas es realizar la asignación de entorno. Normalmente, un objeto con textura con un mapa de entorno aparece muy reflectante y muestra una imagen reflejada del entorno del objeto en la escena. Para esta discusión, imagine una sala con cuatro paredes, cada una con una letra R, G, B, Y y los colores correspondientes: rojo, verde, azul y amarillo. El mapa de entorno de una sala tan sencilla podría ser parecido a la ilustración siguiente.

![ilustración de franjas verticales de rojo, verde, azul y amarillo](images/envmap.png)

Imagine que el límite superior de la sala está retenido por un pilar perfectamente reflectante, de cuatro lados. Asignar la textura del mapa de entorno al pilar es sencillo; hacer que el pilar parezca que refleja las letras y los colores no es tan fácil. En el diagrama siguiente se muestra un marco de conexión del pilar con las coordenadas de textura aplicables enumeradas cerca de los vértices superiores. La siam donde el ajuste cruzará los bordes de la textura se muestra con una línea de puntos.

![diagrama de un rectángulo con una línea de puntos de forma bisectante](images/seam.png)

Con el ajuste habilitado en la dirección U, el pilar con textura muestra los colores y símbolos del mapa de entorno correctamente y, en la coordenada de la parte delantera de la textura, el rasterizador elige correctamente la ruta más corta entre las coordenadas de textura, suponiendo que las coordenadas U 0.0 y 1.0 comparten la misma ubicación. El pilar con textura tiene un aspecto similar al de la ilustración siguiente.

![ilustración de un pilar que consta de cuadrantes rojos, verdes, azules y amarillos](images/tex-seam.png)

Si el ajuste de textura no está habilitado, el rasterizador no se interpola en la dirección necesaria para generar una imagen reconocible y reflejada. En su lugar, el área de la parte delantera del pilar contiene una versión comprimida horizontalmente de los elementos de textura entre las coordenadas u 0,175 y 0,875, a medida que pasan por el centro de la textura. El efecto de encapsulado se ha desenlazado.

## <a name="using-texture-wrapping"></a>Usar ajuste de textura

Para habilitar el ajuste de textura, llame al método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) como se muestra en el ejemplo de código siguiente.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



El primer parámetro aceptado por [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) es un estado de representación que se va a establecer. Especifique uno de los valores enumerados de D3DRS WRAP0 a \_ D3DRS WRAP7 que especifique el nivel de textura para el que \_ establecer el ajuste. Especifique las marcas D3DWRAPCOORD 0 a \_ D3DWRAPCOORD 3 en el segundo parámetro para habilitar el ajuste de textura en la dirección correspondiente o combinarlas para habilitar el ajuste en varias \_ direcciones. Si omite una marca, el ajuste de textura en la dirección correspondiente se deshabilita. Para deshabilitar el ajuste de textura para un conjunto de coordenadas de textura, establezca el valor del estado de representación correspondiente en 0.

No confunda el ajuste de textura con los modos de direccionamiento de textura con un nombre similar. El ajuste de textura se realiza antes del direccionamiento de textura. Asegúrese de que los datos de ajuste de textura no contienen ninguna coordenadas de textura fuera del intervalo de \[ 0,0, 1,0, ya que esto producirá \] resultados indefinidos. Para obtener más información sobre el direccionamiento de textura, vea [Modos de direccionamiento de textura (Direct3D 9).](texture-addressing-modes.md)

## <a name="displacement-map-wrapping"></a>Ajuste de mapa de desplazamiento

Los mapas de desplazamiento se interpolan mediante el motor de tesselation. Dado que no se puede especificar el modo de ajuste para el motor de teselación, el ajuste de textura no se puede realizar con mapas de desplazamiento. Una aplicación puede usar un conjunto de vértices que obligan a la interpolación a ajustarse en cualquier dirección. La aplicación también puede especificar la interpolación que se va a realizar como una interpolación lineal simple.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
