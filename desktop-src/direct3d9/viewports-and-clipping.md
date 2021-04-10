---
description: Conceptualmente, una ventanilla es un rectángulo bidimensional (2D) en el que se proyecta una escena 3D.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Ventanillas y recorte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57f64d17f7abf4e370406f984fa50037be6d44e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151943"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Ventanillas y recorte (Direct3D 9)

Conceptualmente, una ventanilla es un rectángulo bidimensional (2D) en el que se proyecta una escena 3D. En Direct3D, el rectángulo existe como coordenadas dentro de una superficie de Direct3D que el sistema usa como destino de representación. La transformación proyección convierte los vértices en el sistema de coordenadas que se usa para la ventanilla. Una ventanilla también se usa para especificar el intervalo de valores de profundidad en una superficie de representación-destino en la que se representará una escena (normalmente de 0,0 a 1,0).

## <a name="the-viewing-frustum"></a>El frustum de visualización

Un frustum de visualización es un volumen 3D en una escena colocada en relación con la cámara de la ventanilla. La forma del volumen afecta a cómo se proyectan los modelos desde el espacio de la cámara en la pantalla. El tipo más común de proyección, una proyección en perspectiva, es responsable de que los objetos cercanos a la cámara aparezcan más grandes que los objetos de la distancia. Para ver la perspectiva, el frustum de visualización se puede visualizar como una pirámide, con la cámara colocada en la punta, tal como se muestra en la siguiente ilustración. Esta pirámide está intersectada por un plano de recorte delantero y trasero. El número que se encuentra dentro de la pirámide entre los planos de recorte delantero y trasero es el frustum de visualización. Los objetos solo son visibles cuando están en este volumen.

![Ilustración de un frustrum de visualización con un plan de recorte delantero y posterior](images/frustum.png)

Si Imagine que está de pie en una habitación oscura y examina una ventana cuadrada, está visualizando un frustum de visualización. En esta analogía, el plano de recorte cercano es la ventana y el plano de recorte hacia atrás es lo que finalmente interrumpa la vista: el rascacielo en la calle, las montañas de la distancia o nada en absoluto. Puede ver todo lo que se encuentra dentro de la pirámide truncada que comienza en la ventana y termina con cualquier interrupción de la vista, y puede ver nada más.

El frustum de visualización está definido por un campo de código (campo de vista) y por las distancias de los planos de recorte delantero y posterior, que se especifican en coordenadas z, tal como se muestra en el diagrama siguiente.

![diagrama del frustum de visualización](images/fovdiag.png)

En este diagrama, la variable D es la distancia desde la cámara hasta el origen del espacio que se definió en la última parte de la canalización de geometría: la transformación de visualización. Este es el espacio alrededor del cual se organizan los límites del frustum de visualización. Para obtener información sobre cómo se usa esta variable D para compilar la matriz de proyección, vea la [transformación de proyección (Direct3D 9)](projection-transform.md)

## <a name="viewport-rectangle"></a>Rectángulo de ventanilla

El rectángulo de ventanilla se define en C++ mediante la estructura [**D3DVIEWPORT9**](d3dviewport9.md) . La estructura D3DVIEWPORT9 se utiliza con los siguientes métodos de manipulación de la ventanilla expuestos por la interfaz IDirect3DDevice9.

-   [**IDirect3DDevice9::GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

La estructura D3DVIEWPORT9 contiene cuatro miembros: X, Y, ancho y alto, que definen el área de la superficie de representación-destino en la que se representará una escena. Estos valores se corresponden con el rectángulo de destino, o con el rectángulo de la ventanilla, tal y como se muestra en el diagrama siguiente.

![diagrama del rectángulo de la ventanilla](images/destrect.png)

Los valores que se especifican para los miembros X, Y, ancho y alto son coordenadas de pantalla relativas a la esquina superior izquierda de la superficie de representación-destino. La estructura define dos miembros adicionales (MinZ y MaxZ) que indican los intervalos de profundidad en los que se representará la escena.

Direct3D supone que el volumen de recorte de la ventanilla oscila entre-1,0 y 1,0 en X y de 1,0 a-1,0 en Y. Se trata de la configuración usada con más frecuencia por aplicaciones en el pasado. Puede ajustar la relación de aspecto de la ventanilla antes del recorte mediante la [transformación de proyección](projection-transform.md).

> [!Note]  
> MinZ y MaxZ indican los intervalos de profundidad en los que se representará la escena y no se usarán para el recorte. La mayoría de las aplicaciones establecerá estos miembros en 0,0 y 1,0 para permitir que el sistema se represente en todo el intervalo de valores de profundidad en el búfer de profundidad. En algunos casos, puede lograr efectos especiales mediante el uso de otros intervalos de profundidad. Por ejemplo, para representar una pantalla emergente en un juego, puede establecer ambos valores en 0,0 para obligar al sistema a representar objetos en una escena en primer plano, o puede establecer ambos en 1,0 para representar un objeto que siempre debe estar en segundo plano.

 

Las dimensiones usadas en los miembros X, Y, ancho y alto de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) de una ventanilla definen la ubicación y las dimensiones de la ventanilla en la superficie de representación-destino. Estos valores se encuentran en coordenadas de pantalla, con respecto a la esquina superior izquierda de la superficie.

Direct3D usa la ubicación y las dimensiones de la ventanilla para escalar los vértices para que se ajusten a una escena representada en la ubicación adecuada en la superficie de destino. De forma interna, Direct3D inserta estos valores en la matriz siguiente que se aplica a cada vértice.

![ecuación de la matriz que se aplica a cada vértice](images/vpscale.png)

Esta matriz escala los vértices según las dimensiones de la ventanilla y el intervalo de profundidad deseado y los convierte en la ubicación adecuada en la superficie de representación-destino. La matriz también voltea la coordenada y para reflejar el origen de una pantalla en la esquina superior izquierda con y aumentando hacia abajo. Después de aplicar esta matriz, los vértices siguen siendo homogéneos, es decir, siguen existiendo como \[ x, y, z, \] e vértices, y deben convertirse en coordenadas no homogéneas antes de enviarse al rasterizador.

> [!Note]  
> La matriz de escala de ventanilla incorpora los miembros MinZ y MaxZ de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) a los vértices de escala para ajustarse al intervalo de profundidad \[ MinZ, MaxZ \] . Esto representa una semántica diferente de las versiones anteriores de DirectX, en la que estos miembros se usaban para el recorte.

 

> [!Note]  
> Las aplicaciones normalmente establecen MinZ y MaxZ en 0,0 y 1,0, respectivamente, para que el sistema se represente en todo el intervalo de profundidad. Sin embargo, puede usar otros valores para lograr determinados efectos. Por ejemplo, puede establecer ambos valores en 0,0 para forzar todos los objetos en primer plano o establecer ambos en 1,0 para representar todos los objetos en segundo plano.

 

## <a name="clearing-a-viewport"></a>Borrar una ventanilla

Al borrar la ventanilla, se restablece el contenido del rectángulo de la ventanilla en la superficie de representación y destino. También puede borrar el rectángulo en las superficies de búfer de profundidad y de estarcido.

Use [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) para borrar la ventanilla. El método acepta uno o más rectángulos que definen las áreas de la superficie que se va a borrar. Al establecer el parámetro Count en 1, y el parámetro pRects en la dirección de un solo rectángulo que cubre el área de la ventanilla completa, se borrará toda la ventanilla. Otra manera de borrar toda la ventanilla es establecer el parámetro pRects en **null** y el parámetro Count en 0.

Se puede usar [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) para borrar los bits de una galería de símbolos en un búfer de profundidad. Solo tiene que establecer el parámetro flags para determinar cómo **IDirect3DDevice9:: Clear** funciona con el destino de representación y cualquier búfer de estarcido o profundidad asociados. La marca de destino de D3DCLEAR \_ borrará la ventanilla mediante un color RGBA arbitrario que proporcione en el argumento de color (este no es el color del material). La \_ marca D3DCLEAR ZBUFFER borrará el búfer de profundidad hasta una profundidad arbitraria que especifique en Z: 0,0 es la distancia más cercana y 1,0 es la más lejana. La \_ marca de estarcido D3DCLEAR restablecerá los bits de la galería de símbolos al valor que proporcione en el argumento de la galería de símbolos. Puede usar enteros que van de 0 a 2N-1, donde n es la profundidad de bits del búfer de estarcido.

En algunas situaciones, puede que solo se represente en pequeñas partes de las superficies de destino de representación y de búfer de profundidad. Los métodos claros también permiten borrar varias áreas de las superficies en una sola llamada. Para ello, establezca el parámetro Count en el número de rectángulos que desee borrar y especifique la dirección del primer rectángulo en una matriz de rectángulos en el parámetro pRects.

## <a name="set-up-the-viewport-for-clipping"></a>Configurar la ventanilla para el recorte

Los resultados de la matriz de proyección determinan el volumen de recorte en el espacio de proyección como:

-w<sub><=</sub> x<sub>c</sub><= w<sub>c</sub>

-w<sub><</sub> = y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c</sub><= w<sub>c</sub>

Donde: x, y, z y w representan las coordenadas de los vértices después de aplicar la transformación de proyección. Se recortan los vértices que tienen un componente x-, y-o z fuera de estos intervalos, si está habilitado el recorte (comportamiento predeterminado).

Con la excepción de los búferes de vértices, las aplicaciones habilitan o deshabilitan el recorte por medio del estado de representación de [**\_ recorte de D3DRS**](./d3drenderstatetype.md) . La información de recorte para los búferes de vértices se genera durante el procesamiento. Para obtener más información, vea [procesamiento de vértices de función fija (Direct3D 9)](fixed-function-vertex-processing.md) y [procesamiento de vértices programable (Direct3D 9)](programmable-vertex-processing.md).

Direct3D no recorta los vértices transformados de un primitivo desde un búfer de vértice a menos que proceda de [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Si va a realizar sus propias transformaciones y necesita Direct3D para realizar el recorte, no debe usar búferes de vértices. En este caso, la aplicación atraviesa los datos para transformarlos. Direct3D recorre los datos una segunda vez para recortarlo y, a continuación, el controlador representa los datos, lo que es ineficaz. Por lo tanto, si la aplicación transforma los datos, también debe recortar los datos.

Cuando el dispositivo recibe los vértices transformados y encendidos (los vértices de T&L) que deben recortarse, para realizar la operación de recorte, los vértices se transforman en el espacio de recorte mediante el uso de la información homogénea de los vértices (RHW) y la información de la ventanilla. A continuación, se realiza el recorte. No todos los dispositivos son capaces de realizar esta transformación posterior para recortar los vértices de T&.

La \_ funcionalidad del dispositivo D3DPMISCCAPS CLIPTLVERTS indica si el dispositivo es capaz de recortar los vértices de T&L. Si no se establece esta funcionalidad, la aplicación es responsable de recortar los vértices de T&L que se van a enviar al dispositivo que se va a representar. El dispositivo siempre es capaz de recortar los vértices de T&L en el modo de procesamiento de vértices de software (independientemente de si el dispositivo se crea en el modo de procesamiento de vértices de software o de cambiar al modo de procesamiento de vértices de software).

El único requisito para configurar los parámetros de la ventanilla para un dispositivo de representación es establecer el volumen de recorte de la ventanilla. Para ello, inicialice y establezca los valores de recorte para el volumen de recorte y para la superficie de representación-destino. Las ventanillas se configuran normalmente para representarse en el área completa de la superficie de representación y destino, pero esto no es un requisito.

Puede usar la siguiente configuración para los miembros de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) para lograr esto en C++.


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Después de establecer los valores en la estructura [**D3DVIEWPORT9**](d3dviewport9.md) , aplique los parámetros de ventanilla al dispositivo llamando a su método [**IDirect3DDevice9:: SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) . En el ejemplo de código siguiente se muestra el aspecto que podría tener esta llamada.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Si la llamada se realiza correctamente, se establecen los parámetros de la ventanilla y surtirán efecto la próxima vez que se llame a un método de representación. Para realizar cambios en los parámetros de la ventanilla, solo tiene que actualizar los valores de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) y llamar de nuevo a [**IDirect3DDevice9:: SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) .

> [!Note]  
> Los miembros de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) MinZ y MaxZ indican los intervalos de profundidad en los que se representará la escena y no se usarán para el recorte. La mayoría de las aplicaciones establecen estos miembros en 0,0 y 1,0 para permitir que el sistema se represente en todo el intervalo de valores de profundidad en el búfer de profundidad. En algunos casos, puede lograr efectos especiales mediante el uso de otros intervalos de profundidad. Por ejemplo, para representar una pantalla emergente en un juego, puede establecer ambos valores en 0,0 para obligar al sistema a representar objetos en una escena en primer plano, o puede establecer ambos en 1,0 para representar un objeto que siempre debe estar en segundo plano.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
