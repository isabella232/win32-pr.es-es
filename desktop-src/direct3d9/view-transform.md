---
description: En esta sección se presentan los conceptos básicos de la transformación de vista y se proporcionan detalles sobre cómo configurar una matriz de transformación de vistas en una aplicación de Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Transformación de vista (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb184cb75f84a1d28ed6f03f2e65113ea65292fd6ca1871d517d472614f64a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118545"
---
# <a name="view-transform-direct3d-9"></a>Transformación de vista (Direct3D 9)

En esta sección se presentan los conceptos básicos de la transformación de vista y se proporcionan detalles sobre cómo configurar una matriz de transformación de vistas en una aplicación de Direct3D.

La transformación de vista localiza el visor en el espacio del mundo, transformando los vértices en el espacio de la cámara. En el espacio de la cámara, la cámara o el visor se encuentra en el origen, mirando en la dirección Z positiva. Recuerde que Direct3D usa un sistema de coordenadas izquierdo, por lo que z es positivo en una escena. La matriz de vistas reubica los objetos del mundo alrededor de la posición de una cámara (el origen del espacio de la cámara) y la orientación.

Hay muchas maneras de crear una matriz de vistas. En todos los casos, la cámara tiene cierta posición lógica y orientación en el espacio mundial que se usa como punto de partida para crear una matriz de vistas que se aplicará a los modelos de una escena. La matriz de vistas traduce y gira objetos para colocarlos en el espacio de la cámara, donde la cámara está en el origen. Una manera de crear una matriz de vistas es combinar una matriz de traducción con matrices de rotación para cada eje. En este enfoque, se aplica la siguiente ecuación de matriz general.

![ecuación de la transformación de vista](images/viewtran.png)

En esta fórmula, V es la matriz de vista que se crea, T es una matriz de traducción que reposiciones objetos en el mundo y Rₓ a través de R<sub>z</sub> son matrices de rotación que giran objetos a lo largo de los ejes X, Y y Z. Las matrices de traducción y rotación se basan en la posición lógica y la orientación de la cámara en el espacio mundial. Por lo tanto, si la posición lógica de la cámara en el mundo es <10 20 100>, el objetivo de la matriz de traducción es mover objetos -10 unidades a lo largo del eje X, -20 unidades a lo largo del eje Y y -100 unidades a lo largo del eje Z. Las matrices de rotación de la fórmula se basan en la orientación de la cámara, en términos de cuánto se giran los ejes del espacio de la cámara fuera de alineación con el espacio mundial. Por ejemplo, si la cámara mencionada anteriormente apunta directamente hacia abajo, su eje Z está a 90 grados (pi/2 radianes) fuera de alineación con el eje Z del espacio mundial, como se muestra en la ilustración siguiente.

![ilustración del espacio de vista de la cámara en comparación con el espacio mundial](images/camtop.png)

Las matrices de rotación aplican rotaciones de magnitud igual, pero opuesta, a los modelos de la escena. La matriz de vistas de esta cámara incluye una rotación de -90 grados alrededor del eje X. La matriz de rotación se combina con la matriz de traducción para crear una matriz de vista que ajuste la posición y la orientación de los objetos de la escena para que su parte superior esté orientada a la cámara, lo que da la apariencia de que la cámara está por encima del modelo.

## <a name="setting-up-a-view-matrix"></a>Configuración de una matriz de vistas

Las [**funciones auxiliares D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) y [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) crean una matriz de vistas basada en la ubicación de la cámara y un punto de vista.

En el ejemplo siguiente se crea una matriz de vistas para coordenadas de mano izquierda.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D usa el mundo y las matrices de vistas para configurar varias estructuras de datos internas. Cada vez que se establece una nueva matriz de mundo o vista, el sistema vuelve a calcular las estructuras internas asociadas. Establecer estas matrices con frecuencia lleva mucho tiempo. Puede minimizar el número de cálculos necesarios concatenando el mundo y ver matrices en una matriz de vista mundial que estableció como matriz de mundo y, a continuación, estableciendo la matriz de vistas en la identidad. Mantenga copias almacenadas en caché de un mundo individual y vea matrices que puede modificar, concatenar y restablecer la matriz mundial según sea necesario. Para mayor claridad, los ejemplos rara vez emplean esta optimización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transformaciones](transforms.md)
</dt> </dl>

 

 



