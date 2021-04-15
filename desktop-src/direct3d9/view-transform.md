---
description: En esta sección se presentan los conceptos básicos de la transformación vista y se proporcionan detalles sobre cómo configurar una matriz de transformación de vistas en una aplicación Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Transformación de vista (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537582"
---
# <a name="view-transform-direct3d-9"></a>Transformación de vista (Direct3D 9)

En esta sección se presentan los conceptos básicos de la transformación vista y se proporcionan detalles sobre cómo configurar una matriz de transformación de vistas en una aplicación Direct3D.

La transformación de vista busca el visor en el espacio universal, transformando los vértices en el espacio de la cámara. En el espacio de la cámara, la cámara o el visor, está en el origen y busca en la dirección z positiva. Recuerde que Direct3D usa un sistema de coordenadas a la izquierda, por lo que z es positivo en una escena. La matriz de la vista reubica los objetos del mundo en torno a la posición de una cámara: el origen del espacio de la cámara y la orientación.

Hay muchas maneras de crear una matriz de vista. En todos los casos, la cámara tiene una posición lógica y una orientación en el espacio universal que se usa como punto de partida para crear una matriz de vistas que se aplicará a los modelos de una escena. La matriz de la vista traduce y gira los objetos para colocarlos en el espacio de la cámara, donde la cámara está en el origen. Una manera de crear una matriz de vistas es combinar una matriz de traslación con matrices de rotación para cada eje. En este enfoque, se aplica la siguiente ecuación de matriz general.

![ecuación de la transformación de vista](images/viewtran.png)

En esta fórmula, V es la matriz de vistas que se está creando, T es una matriz de traducción que recoloca objetos en el mundo y R ₓ a R<sub>z</sub> son matrices de rotación que giran objetos a lo largo de los ejes x-, y-y z. Las matrices de traslación y rotación se basan en la posición lógica y la orientación de la cámara en el espacio universal. Por lo tanto, si la posición lógica de la cámara en el mundo es <10, 20100>, el objetivo de la matriz de traslación es mover objetos-10 unidades a lo largo del eje x,-20 unidades a lo largo del eje y, y-100 unidades a lo largo del eje z. Las matrices de rotación de la fórmula se basan en la orientación de la cámara, en cuanto a la cantidad de ancho de los ejes del espacio de la cámara que se giran con el espacio universal. Por ejemplo, si la cámara mencionada anteriormente apunta hacia abajo, su eje z es 90 grados (pi/2 radianes) fuera de la alineación con el eje z del espacio universal, tal como se muestra en la siguiente ilustración.

![Ilustración del espacio de vista de la cámara en comparación con el espacio universal](images/camtop.png)

Las matrices de rotación aplican rotaciones de la misma magnitud, pero opuestas, a los modelos de la escena. La matriz de la vista de esta cámara incluye un giro de-90 grados alrededor del eje x. La matriz de rotación se combina con la matriz de traslación para crear una matriz de vista que ajusta la posición y la orientación de los objetos de la escena para que su parte superior esté orientada a la cámara, lo que proporciona la apariencia de que la cámara está por encima del modelo.

## <a name="setting-up-a-view-matrix"></a>Configurar una matriz de vistas

Las funciones auxiliares [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) y [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) crean una matriz de vista basada en la ubicación de la cámara y un punto de búsqueda.

En el ejemplo siguiente se crea una matriz de vista para las coordenadas de la izquierda.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D usa el mundo y las matrices de vistas para configurar varias estructuras de datos internas. Cada vez que se establece un nuevo mundo o una matriz de vistas, el sistema vuelve a calcular las estructuras internas asociadas. Establecer estas matrices con frecuencia es un proceso que consume mucho tiempo. Puede minimizar el número de cálculos necesarios concatenando el mundo y ver las matrices en una matriz de vista mundial que establezca como la matriz universal y, a continuación, estableciendo la matriz de la vista en la identidad. Mantenga copias en caché de matrices de mundo y vistas individuales que puede modificar, concatenar y restablecer la matriz universal según sea necesario. Para mayor claridad, los ejemplos raramente emplean esta optimización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transformaciones](transforms.md)
</dt> </dl>

 

 



