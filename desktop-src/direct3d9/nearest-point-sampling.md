---
description: No es necesario que las aplicaciones usen el filtrado de texturas.
ms.assetid: bba0e485-ac5a-4e43-9eb7-25cd0c90d316
title: Nearest-Point muestreo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8146ce8cfc2d5852cf3847233b431352d69b8bc1f0a52f41da5ac3c9a7c89d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119458768"
---
# <a name="nearest-point-sampling-direct3d-9"></a>Nearest-Point muestreo (Direct3D 9)

No es necesario que las aplicaciones usen el filtrado de texturas. Direct3D se puede establecer para que calcule la dirección de texel, que a menudo no se evalúa como enteros, y copia el color del texel con la dirección de entero más cercana. Este proceso se denomina muestreo de punto más cercano. Esta puede ser una manera rápida y eficaz de procesar texturas si el tamaño de la textura es similar al tamaño de la imagen de la primitiva en la pantalla. Si no es así, la textura debe ampliarse o minificarse. El resultado puede ser una imagen fragmentada, con alias o desenfoque.

La aplicación de C++ puede seleccionar el muestreo de punto más cercano llamando al [**método IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que va a seleccionar un método de filtrado de textura. Pase D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER para el segundo parámetro para establecer el filtro \_ \_ de ampliación, minificación o mipmapping. Pase D3DTEXF \_ POINT en el tercer parámetro.

Debe usar cuidadosamente el muestreo de punto más cercano, ya que a veces puede provocar artefactos gráficos cuando la textura se muestrea en el límite entre dos elementos de textura. Este límite es la posición a lo largo de la textura (u o v) en la que el texel muestreado pasa de un texel al siguiente. Cuando se usa el muestreo de punto, el sistema elige un texel de muestra u otro, y el resultado puede cambiar repentinamente de un texel al siguiente a medida que se cruza el límite. Este efecto puede aparecer como artefactos gráficos no deseados en la textura mostrada. Cuando se usa el filtrado lineal, el texel resultante se calcula a partir de los elementos de textura adyacentes y se mezcla sin problemas entre ellos a medida que el índice de textura se mueve a través del límite.

Este efecto se puede ver al asignar una textura muy pequeña a un polígono muy grande: una operación a menudo denominada ampliación. Por ejemplo, cuando se usa una textura similar a un tablero de comprobación, el muestreo de punto más cercano da como resultado un tablero de comprobación más grande que muestra bordes distintos. Por el contrario, el filtrado de textura lineal da como resultado una imagen en la que los colores del tablero de comprobación varían sin problemas en el polígono.

En la mayoría de los casos, las aplicaciones reciben los mejores resultados evitando el ejemplo de punto más cercano siempre que sea posible. La mayoría del hardware actual está optimizado para el filtrado lineal, por lo que la aplicación no debe sufrir un rendimiento degradado. Si el efecto que desea requiere absolutamente el uso del muestreo de punto más cercano (por ejemplo, cuando se usan texturas para mostrar caracteres de texto legibles), la aplicación debe tener mucho cuidado para evitar el muestreo en los límites del texel, lo que podría producir efectos no deseados. En la ilustración siguiente se muestra el aspecto que pueden tener estos artefactos.

![ilustración de un cuadro de seis secciones con líneas horizontales no pertinentes en los dos cuadrados superior derecho](images/ptrtfct.png)

Observe que los dos cuadrados de la esquina superior derecha del grupo aparecen diferentes de sus vecinos, con desplazamientos diagonales que se ejecutan a través de ellos. Para evitar artefactos gráficos como estos, debe estar familiarizado con las reglas de muestreo de textura de Direct3D para el filtrado de punto más cercano. Direct3D asigna una coordenada de textura de punto flotante que va de \[ 0,0, 1,0 (0,0 a 1,0, ambos incluidos) a un valor de espacio de textura entero comprendido entre \] \[ - 0,5, n - 0,5 , donde n es el número de elementos de textura de una dimensión determinada en la \] textura. El índice de textura resultante se redondea al entero más cercano. Esta asignación puede introducir imprecisiones de muestreo en límites de textura.

Para obtener un ejemplo sencillo, imagine una aplicación que representa polígonos con el modo de direccionamiento de textura D3DTADDRESS \_ WRAP. Con la asignación empleada por Direct3D, el índice de textura u se asigna como se muestra en el diagrama siguiente para una textura con un ancho de 4 elementos de textura.

![diagrama de coordenadas de textura 0,0 y 1,0 en el límite entre los elementos de textura](images/ptsmpprb.png)

Observe que las coordenadas de textura, 0,0 y 1,0 para esta ilustración, están exactamente en el límite entre los elementos de textura. Con el método por el que Direct3D asigna valores, las coordenadas de textura oscilan entre \[ - 0,5, 4 - 0,5 , donde 4 es el ancho de la \] textura. En este caso, el texel muestreado es el 0 texel para un índice de textura de 1,0. Sin embargo, si la coordenada de textura solo fuera ligeramente inferior a 1,0, el texel muestreado sería el texel n en lugar del 0.

La implicación de esto es que la lupa de una textura pequeña mediante coordenadas de textura de exactamente 0,0 y 1,0 con filtrado de punto más cercano en un triángulo alineado de espacio de pantalla da como resultado píxeles para los que el mapa de textura se muestrea en el límite entre los texturas. Las imprecisiones en el cálculo de coordenadas de textura, aunque pequeñas, tienen como resultado artefactos a lo largo de las áreas de la imagen representada que corresponden a los bordes de textura del mapa de textura.

Realizar esta asignación de coordenadas de textura de punto flotante a elementos texeles enteros con precisión perfecta es difícil, requiere mucho tiempo y, por lo general, no es necesario. La mayoría de las implementaciones de hardware usan un enfoque iterativo para calcular las coordenadas de textura en cada ubicación de píxel dentro de un triángulo. Los enfoques iterativos tienden a ocultar estas imprecisiones porque los errores se acumulan uniformemente durante la iteración.

El rasterizador de referencia de Direct3D usa un enfoque de evaluación directa para calcular los índices de textura en cada ubicación de píxeles. La evaluación directa difiere del enfoque iterativo en que cualquier imprecisión en la operación presenta una distribución de errores más aleatoria. El resultado es que los errores de muestreo que se producen en los límites pueden ser más evidentes porque el rasterizador de referencia no realiza esta operación con una precisión perfecta.

El mejor enfoque es usar el filtrado de punto más cercano solo cuando sea necesario. Cuando deba usarlo, se recomienda desplazar ligeramente las coordenadas de textura de las posiciones de límite para evitar artefactos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de textura](texture-filtering.md)
</dt> </dl>

 

 
