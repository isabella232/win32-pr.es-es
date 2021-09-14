---
description: Los mapas de entorno esféricos, o mapas de esfera, son texturas especiales que contienen una imagen de la escena que rodea un objeto o los efectos de iluminación alrededor del objeto.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Asignación de entorno esférica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b0e7aaa123478ecc7cc327dca0b13a8aae3d0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160432"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Asignación de entorno esférica (Direct3D 9)

Los mapas de entorno esféricos, o mapas de esfera, son texturas especiales que contienen una imagen de la escena que rodea un objeto o los efectos de iluminación alrededor del objeto. A diferencia de los mapas de entorno cúbica, los mapas de esfera no representan directamente el entorno de un objeto. La imagen de té en el tema [Asignación de entorno (Direct3D 9)](environment-mapping.md) muestra los efectos de reflexión que puede lograr con la asignación de esferas. Un mapa de esfera es una representación en 2D de la vista completa de 360 grados de la escena que rodea a un objeto, como si se tomara a través de una lente de ojo de ojos, como se muestra en la ilustración siguiente.

![ilustración de un mapa de esfera del interior de un edificio](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Coordenadas de textura para el entorno esférico Mapas

Las coordenadas de textura que especifique para cada vértice que recibe una asignación de entorno deben abordar la textura como una función de la distorsión reflectante creada por la curvación de la superficie. Las aplicaciones deben calcular estas coordenadas de textura para cada vértice a fin de lograr el efecto deseado. Una manera sencilla y eficaz de generar coordenadas de textura usa el vértice normal como entrada. Aunque existen varios métodos, la siguiente ecuación es común entre las aplicaciones que realizan la asignación de entorno con mapas de esfera.

![ecuación de calcular coordenadas de textura para un mapa de esfera](images/spheremap-formula.png)

En estas fórmulas, usted y v son las coordenadas de textura que se calculan, y N<sub>X</sub> e N<sub>Y</sub> son los componentes x e y del vértice del espacio de cámara normal. La fórmula es sencilla pero eficaz. Si la normal tiene un componente x positivo, el normal apunta a la derecha y la coordenada u se ajusta para abordar la textura correctamente. Del mismo modo para la coordenada v: positivo y indica que el normal apunta hacia arriba. Lo contrario se aplica a los valores negativos de cada componente.

Si los puntos normales directamente en la cámara, las coordenadas resultantes no deben recibir distorsión. El sesgo de +0,5 en ambas coordenadas coloca el punto de distorsión cero en el centro del mapa de esfera y un vértice normal de (0, 0, z) direcciona este punto. Esta fórmula no tiene en cuenta el componente z de lo normal, pero las aplicaciones que usan la fórmula pueden optimizar los cálculos omitiendo los vértices con un normal que tiene un elemento z positivo. Esto funciona con objetos sombreados planos porque, en el espacio de la cámara, si el normal se aleja de la cámara (z positivo), el vértice se hace cuando se representa el objeto. En el caso de los objetos sombreados por Gouraud, un normal puede apuntar fuera de la cámara (x positivo) y el triángulo que contiene el vértice puede seguir siendo visible. Si no calcula usted y v para este vértice, es posible que todavía se utilice la cara, lo que da lugar a un comportamiento inesperado.

## <a name="applying-spherical-environment-maps"></a>Aplicación del entorno esférico Mapas

Para aplicar un mapa de entorno a objetos de la misma manera que para cualquier otra textura, establezca la textura en la fase de textura adecuada con el método [**IDirect3DDevice9::SetTexture.**](/windows/desktop/api) Establezca el primer parámetro en el índice de la fase de textura deseada y establezca el segundo parámetro en la dirección de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) devuelta al crear la textura para el mapa de entorno. Puede establecer las operaciones y los argumentos de combinación de color y alfa según sea necesario para lograr los efectos de mezcla de textura deseados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de entorno](environment-mapping.md)
</dt> </dl>

 

 
