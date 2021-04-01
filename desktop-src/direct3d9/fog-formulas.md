---
description: Las aplicaciones de C++ pueden controlar cómo afecta la niebla al color de los objetos en una escena cambiando la forma en que Microsoft Direct3D calcula los efectos de niebla a través de la distancia.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Fórmulas de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906545"
---
# <a name="fog-formulas-direct3d-9"></a>Fórmulas de niebla (Direct3D 9)

Las aplicaciones de C++ pueden controlar cómo afecta la niebla al color de los objetos en una escena cambiando la forma en que Microsoft Direct3D calcula los efectos de niebla a través de la distancia. El tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) contiene miembros que identifican las tres fórmulas de niebla. Todas las fórmulas calculan un factor de niebla como una función de distancia, dados los parámetros que establece la aplicación.

## <a name="linear-fog"></a>Niebla lineal

Se establece con la ecuación lineal de D3DFOG siguiente \_ .

![ecuación de niebla lineal de Direct3D](images/fogliner.png)

where

-   Start es la distancia a la que comienzan los efectos de niebla.
-   end es la distancia a la que los efectos de niebla ya no aumentan.
-   d representa la profundidad o la distancia desde el punto de vista. En el caso de la niebla basada en intervalo, el valor de d es la distancia entre la posición de la cámara y un vértice. En el caso de una niebla no basada en intervalos, el valor de d es el valor absoluto de la coordenada Z del espacio de la cámara.

## <a name="exponential-fog"></a>Niebla exponencial

Las fórmulas lineal y exponencial se admiten tanto para la niebla de píxeles como para la niebla de vértice.

Se establece con la siguiente ecuación D3DFOG \_ exp.

![ecuación de la niebla exponencial de Direct3D](images/fogexp.png)

where

-   e es la base de los logaritmos naturales (aproximadamente 2,71828).
-   la densidad es una densidad de niebla arbitraria que puede oscilar entre 0,0 y 1,0.
-   d representa la profundidad, o la distancia desde el punto de vista, como se indicó anteriormente.

Se establece con la siguiente ecuación de \_ EXP2 de D3DFOG.

![ecuación de la niebla de Direct3D exponencial 2](images/fogexp2.png)

where

-   e es la base de los logaritmos naturales tal y como se indicó anteriormente.
-   la densidad es una densidad de niebla arbitraria que puede oscilar entre 0,0 y 1,0, tal y como se indicó anteriormente.
-   d representa la profundidad, o la distancia desde el punto de vista, como se indicó anteriormente.

> [!Note]  
> El sistema almacena el factor de niebla en el componente alfa del color especular de un vértice. Si la aplicación realiza su propia transformación e iluminación, puede insertar valores de factor de niebla manualmente para que los aplique el sistema durante la representación.

 

En el gráfico siguiente se muestran estas fórmulas con valores comunes como en los parámetros de la fórmula.

![gráfico de las fórmulas de niebla a través de la distancia y la cantidad de color](images/foggraph.png)

D3DFOG \_ linear es 1,0 en Start y 0,0 al final. No se mide en relación con los planos near o FAR.

Cuando Direct3D calcula los efectos de niebla, utiliza el factor de niebla de una de las ecuaciones anteriores en la siguiente ecuación de fusión.

![ecuación de efectos de niebla para Direct3D](images/fogcalc.png)

Esta fórmula escala eficazmente el color del polígono actual C mediante el factor de niebla f, y agrega el producto al color de niebla C, escalado por el inverso bit a bit del factor de niebla. El valor de color resultante es una mezcla del color de niebla y el color original, como un factor de distancia. La fórmula se aplica a todos los dispositivos compatibles con Microsoft DirectX 7,0 y versiones posteriores. En el caso del dispositivo de rampa heredado, el factor de niebla escala los componentes de color difuso y especular, fijados en el intervalo de 0,0 y 1,0, ambos incluidos. Normalmente, el factor de niebla comienza en 1,0 para el plano próximo y se reduce a 0,0 en el plano lejano.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de niebla](fog-types.md)
</dt> </dl>

 

 
