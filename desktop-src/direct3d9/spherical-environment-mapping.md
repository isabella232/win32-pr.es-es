---
description: Los mapas de entorno esféricos, o mapas de esferas, son texturas especiales que contienen una imagen de la escena que rodea un objeto o los efectos de iluminación alrededor del objeto.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Asignación de entorno esférico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b0e7aaa123478ecc7cc327dca0b13a8aae3d0c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677141"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Asignación de entorno esférico (Direct3D 9)

Los mapas de entorno esféricos, o mapas de esferas, son texturas especiales que contienen una imagen de la escena que rodea un objeto o los efectos de iluminación alrededor del objeto. A diferencia de los mapas de entorno cúbicos, los mapas de esfera no representan directamente el entorno de un objeto. En el tema de la imagen de tetera en la [asignación de entorno (Direct3D 9)](environment-mapping.md) se muestran los efectos de reflexión que se pueden lograr con la asignación de esferas. Un mapa de esfera es una representación 2D de la vista completa de 360 grados de la escena que rodea a un objeto, como si se hubiera tomado a través de un objetivo de ojos pesqueros, como se muestra en la siguiente ilustración.

![Ilustración de un mapa de esfera del interior de un edificio](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Coordenadas de textura para mapas de entorno esféricos

Las coordenadas de textura que se especifican para cada vértice que recibe una asignación de entorno deben abordar la textura como una función de la distorsión reflectante creada por la curvatura de la superficie. Las aplicaciones deben calcular estas coordenadas de textura para cada vértice para lograr el efecto deseado. Una manera sencilla y eficaz de generar coordenadas de textura usa el vértice normal como entrada. Aunque existen varios métodos, la siguiente ecuación es común entre las aplicaciones que realizan la asignación de entorno con mapas de esferas.

![ecuación de las coordenadas de textura de cálculo para un mapa de esfera](images/spheremap-formula.png)

En estas fórmulas, usted y v son las coordenadas de textura que se están calculando y N<sub>X</sub> y n<sub>y</sub> son los componentes X e y del vértice del espacio de la cámara normal. La fórmula es sencilla pero eficaz. Si el normal tiene un componente x positivo, el normal apunta a la derecha y la coordenada u se ajusta para abordar la textura correctamente. Del mismo modo que la coordenada v: y positivo indica que el punto normal es. Lo contrario se aplica a los valores negativos en cada componente.

Si el punto normal apunta directamente a la cámara, las coordenadas resultantes no recibirán ninguna distorsión. La diferencia entre + 0,5 y ambas coordenadas coloca el punto de la distorsión cero en el centro del mapa de esfera y el de un vértice normal de (0,0) se dirige a este punto. Esta fórmula no tiene en cuenta el componente z de la normal, pero las aplicaciones que usan la fórmula pueden optimizar los cálculos omitiendo los vértices con un normal que tiene un elemento z positivo. Esto funciona para los objetos con sombra plana porque, en el espacio de la cámara, si el punto normal se aleja de la cámara (positivo z), el vértice se selecciona cuando se representa el objeto. En el caso de los objetos con sombreado Gouraud, una normal puede apuntar a la cámara (x positivo) y el triángulo que contiene el vértice puede seguir siendo visible. Si no calcula usted y v para este vértice, la esfera podría seguir utilizándose, lo que produce un comportamiento inesperado.

## <a name="applying-spherical-environment-maps"></a>Aplicación de mapas de entorno esféricos

Para aplicar un mapa de entorno a objetos de la misma manera que para cualquier otra textura, establezca la textura en la fase de textura adecuada con el método [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) . Establezca el primer parámetro en el índice de la fase de textura deseada y establezca el segundo parámetro en la dirección de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se devuelve al crear la textura para el mapa de entorno. Puede establecer las operaciones y los argumentos de combinación de colores y alfa según sea necesario para lograr los efectos de combinación de texturas deseados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de entorno](environment-mapping.md)
</dt> </dl>

 

 
