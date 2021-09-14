---
description: Las aplicaciones de C++ pueden controlar cómo afecta el color de los objetos de una escena cambiando la forma en que Microsoft Direct3D calcula los efectos de efecto a lo largo de la distancia.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Fórmulas de fórmulas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888561"
---
# <a name="fog-formulas-direct3d-9"></a>Fórmulas de fórmulas (Direct3D 9)

Las aplicaciones de C++ pueden controlar cómo afecta el color de los objetos de una escena cambiando la forma en que Microsoft Direct3D calcula los efectos de efecto a lo largo de la distancia. El [**tipo enumerado D3DFOGMODE**](./d3dfogmode.md) contiene miembros que identifican las tres fórmulas de matriz. Todas las fórmulas calculan un factor de matriz como una función de distancia, dados los parámetros que establece la aplicación.

## <a name="linear-fog"></a>Linear Linear (Lineal)

Esto se establece con la siguiente ecuación LINEAL D3DFOG. \_

![ecuación de la línea lineal direct3d](images/fogliner.png)

, donde

-   start es la distancia a la que comienzan los efectos de sonido.
-   end es la distancia a la que ya no aumentan los efectos de efecto de sonido.
-   d representa la profundidad o la distancia desde el punto de vista. En el caso de los intervalos basados en intervalos, el valor de d es la distancia entre la posición de la cámara y un vértice. En el caso de los intervalos no basados en intervalos, el valor de d es el valor absoluto de la coordenada Z en el espacio de la cámara.

## <a name="exponential-fog"></a>Exponencialmente exponencial

Las fórmulas lineales y exponenciales se admiten tanto para el vértice de píxeles como para el vértice.

Esto se establece con la siguiente ecuación exp de D3DFOG. \_

![ecuación de la expansión exponencial de direct3d](images/fogexp.png)

, donde

-   e es la base de logaritmos naturales (aproximadamente 2,71828).
-   density es una densidad de densidad arbitraria que puede oscilar entre 0,0 y 1,0.
-   d representa la profundidad o la distancia desde el punto de vista, como se indicó anteriormente.

Esto se establece con la siguiente ecuación D3DFOG \_ EXP2.

![ecuación de direct3d exponential 2 menos](images/fogexp2.png)

, donde

-   e es la base de los logaritmos naturales como se indicó anteriormente.
-   density es una densidad de densidad arbitraria que puede oscilar entre 0,0 y 1,0, como se indicó anteriormente.
-   d representa la profundidad o la distancia desde el punto de vista, como se indicó anteriormente.

> [!Note]  
> El sistema almacena el factor de color en el componente alfa del color especular de un vértice. Si la aplicación realiza su propia transformación e iluminación, puede insertar manualmente valores de factor de efusión que el sistema aplicará durante la representación.

 

En el gráfico siguiente se muestran estas fórmulas, usando valores comunes como en los parámetros de fórmula.

![gráfico de las fórmulas de niebla a lo largo de la distancia y la cantidad de color](images/foggraph.png)

D3DFOG \_ LINEAR es 1.0 al principio y 0.0 al final. No se mide con respecto a los planos cercanos o lejanos.

Cuando Direct3D calcula los efectos de la fusión, usa el factor de fusión de una de las ecuaciones anteriores en la siguiente ecuación de combinación.

![ecuación de efectos de efecto para direct3d](images/fogcalc.png)

Esta fórmula escala de forma eficaz el color del polígono actual C por el factor f y agrega el producto al color de color de color C, escalado por el inverso bit a bit del factor de paleta. El valor de color resultante es una combinación del color de color de color y el color original, como un factor de distancia. La fórmula se aplica a todos los dispositivos compatibles con Microsoft DirectX 7.0 y versiones posteriores. En el caso del dispositivo de rampa heredado, el factor de rampa escala los componentes de color difuso y especular, con fijación en el intervalo de 0,0 y 1,0, ambos incluidos. El factor de vuelo normalmente comienza en 1,0 para el plano cercano y disminuye a 0,0 en el plano lejano.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de vaselina](fog-types.md)
</dt> </dl>

 

 
