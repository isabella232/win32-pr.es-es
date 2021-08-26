---
description: Conceptualmente, una ventanilla es un rectángulo bidimensional (2D) en el que se proyecta una escena 3D.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Ventanillas y recorte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6ed7cd5e5a8a3116c07c5b88f3e665e7ba7de7c6dd1d3cd7bf55f936e60386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068874"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Ventanillas y recorte (Direct3D 9)

Conceptualmente, una ventanilla es un rectángulo bidimensional (2D) en el que se proyecta una escena 3D. En Direct3D, el rectángulo existe como coordenadas dentro de una superficie de Direct3D que el sistema usa como destino de representación. La transformación de proyección convierte los vértices en el sistema de coordenadas utilizado para la ventanilla. También se usa una ventanilla para especificar el intervalo de valores de profundidad en una superficie de destino de representación en la que se representará una escena (normalmente de 0,0 a 1,0).

## <a name="the-viewing-frustum"></a>El frustum de visualización

Un frustum de visualización es un volumen 3D en una escena posicionada en relación con la cámara de la ventanilla. La forma del volumen afecta a cómo se proyectan los modelos desde el espacio de la cámara a la pantalla. El tipo más común de proyección, una proyección de perspectiva, es responsable de hacer que los objetos cercanos a la cámara aparezcan más grandes que los objetos de la distancia. Para la visualización de perspectivas, el frustum de visualización se puede visualizar como una piramidal, con la cámara posicionada en la punta, como se muestra en la ilustración siguiente. Esta pirámide se interseca con un plano de recorte frontal y posterior. El volumen dentro de la pirámide entre los planos de recorte frontal y posterior es el frustum de visualización. Los objetos solo son visibles cuando están en este volumen.

![ilustración de una frusía de visualización con un plan de recorte frontal y posterior](images/frustum.png)

Si imagine que se encuentra en una sala oscura y mira a través de una ventana cuadrada, está visualizando un frustum de visualización. En esta analogía, el plano de recorte cercano es la ventana y el plano de recorte posterior es lo que finalmente interrumpe la vista: el skyscraper a través de la calle, las montañas en la distancia o nada en absoluto. Puede ver todo lo que hay dentro de la pirámide truncada que comienza en la ventana y termina con cualquier interrupción de la vista, y no puede ver nada más.

El frustum de visualización se define mediante fov (campo de vista) y por las distancias de los planos de recorte frontal y posterior, especificados en coordenadas z, como se muestra en el diagrama siguiente.

![diagrama del frustum de visualización](images/fovdiag.png)

En este diagrama, la variable D es la distancia desde la cámara hasta el origen del espacio definido en la última parte de la canalización de geometría: la transformación de visualización. Este es el espacio alrededor del cual se organizan los límites del frustum de visualización. Para obtener información sobre cómo se usa esta variable D para compilar la matriz de proyección, vea La transformación proyección [(Direct3D 9)](projection-transform.md)

## <a name="viewport-rectangle"></a>Rectángulo de ventanilla

El rectángulo de ventanilla se define en C++ mediante la [**estructura D3DVIEWPORT9.**](d3dviewport9.md) La estructura D3DVIEWPORT9 se usa con los siguientes métodos de manipulación de ventanilla expuestos por la interfaz IDirect3DDevice9.

-   [**IDirect3DDevice9::GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

La estructura D3DVIEWPORT9 contiene cuatro miembros (X, Y, Width y Height) que definen el área de la superficie de destino de representación en la que se representará una escena. Estos valores corresponden al rectángulo de destino, o rectángulo de ventanilla, como se muestra en el diagrama siguiente.

![diagrama del rectángulo de ventanilla](images/destrect.png)

Los valores que especifique para los miembros X, Y, Width y Height son coordenadas de pantalla relativas a la esquina superior izquierda de la superficie de destino de representación. La estructura define dos miembros adicionales (MinZ y MaxZ) que indican los intervalos de profundidad en los que se representará la escena.

Direct3D supone que el volumen de recorte de ventanilla oscila entre -1,0 y 1,0 en X y de 1,0 a -1,0 en Y. Estas eran las configuraciones usadas con más frecuencia por las aplicaciones en el pasado. Puede ajustar la relación de aspecto de la ventanilla antes del recorte mediante la transformación [de proyección](projection-transform.md).

> [!Note]  
> MinZ y MaxZ indican los intervalos de profundidad en los que se representará la escena y no se usan para el recorte. La mayoría de las aplicaciones establecerán estos miembros en 0.0 y 1.0 para permitir que el sistema se represente en todo el intervalo de valores de profundidad del búfer de profundidad. En algunos casos, puede lograr efectos especiales mediante otros intervalos de profundidad. Por ejemplo, para representar una presentación de cara al frente en un juego, puede establecer ambos valores en 0,0 para forzar al sistema a representar objetos en una escena en primer plano, o puede establecer ambos en 1.0 para representar un objeto que siempre debe estar en segundo plano.

 

Las dimensiones usadas en los miembros X, Y, Width y Height de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) para una ventanilla definen la ubicación y las dimensiones de la ventanilla en la superficie de destino de representación. Estos valores están en coordenadas de pantalla, en relación con la esquina superior izquierda de la superficie.

Direct3D usa la ubicación y las dimensiones de la ventanilla para escalar los vértices para ajustar una escena representado a la ubicación adecuada en la superficie de destino. Internamente, Direct3D inserta estos valores en la siguiente matriz que se aplica a cada vértice.

![ecuación de la matriz que se aplica a cada vértice](images/vpscale.png)

Esta matriz escala los vértices según las dimensiones de la ventanilla y el intervalo de profundidad deseado y los traduce a la ubicación adecuada en la superficie de destino de representación. La matriz también invierte la coordenada y para reflejar un origen de pantalla en la esquina superior izquierda con y aumentando hacia abajo. Después de aplicar esta matriz, los vértices siguen siendo homogéneos (es decir, siguen existiendo como vértices x,y,z,w) y deben convertirse en coordenadas no homogéneos antes de enviarse al \[ \] rasterizador.

> [!Note]  
> La matriz de escalado de la ventanilla incorpora los miembros MinZ y MaxZ de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) para escalar los vértices para ajustarlos al intervalo de profundidad \[ MinZ y MaxZ. \] Esto representa una semántica diferente de las versiones anteriores de DirectX, en las que estos miembros se usaban para el recorte.

 

> [!Note]  
> Las aplicaciones suelen establecer MinZ y MaxZ en 0,0 y 1,0 respectivamente para que el sistema se represente en todo el intervalo de profundidad. Sin embargo, puede usar otros valores para lograr ciertos efectos. Por ejemplo, puede establecer ambos valores en 0,0 para forzar que todos los objetos entren en primer plano o establecer ambos en 1.0 para representar todos los objetos en segundo plano.

 

## <a name="clearing-a-viewport"></a>Borrar una ventanilla

Al borrar la ventanilla, se restablece el contenido del rectángulo de la ventanilla en la superficie de destino de representación. También puede borrar el rectángulo en las superficies de búfer de profundidad y galería de símbolos.

Use [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) para borrar la ventanilla. El método acepta uno o varios rectángulos que definen las áreas de la superficie que se borran. Al establecer el parámetro Count en 1 y el parámetro pRects en la dirección de un solo rectángulo que cubre todo el área de ventanilla, se borrará toda la ventanilla. Otra manera de borrar toda la ventanilla es establecer el parámetro pRects en **NULL** y el parámetro Count en 0.

[**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) se puede usar para borrar bits de galería de símbolos dentro de un búfer de profundidad. Basta con establecer el parámetro Flags para determinar cómo **funciona IDirect3DDevice9::Clear** con el destino de representación y los búferes de profundidad o galería de símbolos asociados. La marca D3DCLEAR TARGET borrará la ventanilla con un color RGBA arbitrario que proporcione en el \_ argumento Color (no es el color del material). La marca D3DCLEAR ZBUFFER borrará el búfer de profundidad a una profundidad arbitraria que especifique en Z: 0,0 es la distancia más cercana y 1,0 es la más \_ lejana. La marca D3DCLEAR STENCIL restablecerá los bits de la galería de símbolos al valor que proporcione en el \_ argumento Stencil. Puede usar enteros que oscilan entre 0 y 2n-1, donde n es la profundidad de bits del búfer de la galería de símbolos.

En algunas situaciones, es posible que solo se represente en pequeñas partes de las superficies de destino de representación y búfer de profundidad. Los métodos clear también permiten borrar varias áreas de las superficies en una sola llamada. Para ello, establece el parámetro Count en el número de rectángulos que quieres borrar y especifica la dirección del primer rectángulo en una matriz de rectángulos en el parámetro pRects.

## <a name="set-up-the-viewport-for-clipping"></a>Configurar la ventanilla para el recorte

Los resultados de la matriz de proyección determinan el volumen de recorte en el espacio de proyección como:

-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub>

-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c<</sub> = w<sub>c</sub>

Donde: x, y, z y w representan las coordenadas de vértice después de aplicar la transformación de proyección. Los vértices que tienen un componente x, y o z fuera de estos intervalos se recortan, si está habilitado el recorte (el comportamiento predeterminado).

A excepción de los búferes de vértices, las aplicaciones habilitan o deshabilitan el recorte mediante el estado de representación CLIPPING de [**D3DRS. \_**](./d3drenderstatetype.md) La información de recorte para los búferes de vértices se genera durante el procesamiento. Para obtener más información, vea Procesamiento de vértices de función [fija (Direct3D 9)](fixed-function-vertex-processing.md) y Procesamiento de vértices [programables (Direct3D 9).](programmable-vertex-processing.md)

Direct3D no recorta los vértices transformados de una primitiva de un búfer de vértices a menos que procede de [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Si está realizando sus propias transformaciones y necesita Direct3D para realizar el recorte, no debe usar búferes de vértices. En este caso, la aplicación recorre los datos para transformarlo. Direct3D recorre los datos una segunda vez para recortarlo y, a continuación, el controlador representa los datos, lo que es ineficaz. Por lo tanto, si la aplicación transforma los datos, también debe recortar los datos.

Cuando el dispositivo recibe vértices previamente transformados y encendidos (T&L vértices) que deben recortarse, para realizar la operación de recorte, los vértices se transforman de nuevo en el espacio de recorte mediante el homogéneo w (RHW) recíproco del vértice y la información de la ventanilla. A continuación, se realiza el recorte. No todos los dispositivos son capaces de realizar esta transformación hacia atrás con el fin de recortar T&L vértices.

La funcionalidad del dispositivo D3DPMISCCAPS CLIPTLVERTS indica si el dispositivo es capaz de recortar \_ T&L vértices. Si no se establece esta funcionalidad, la aplicación es responsable de recortar los vértices de T&L que pretende enviar al dispositivo que se va a representar. El dispositivo siempre es capaz de recortar los vértices de T&L en el modo de procesamiento de vértices de software (independientemente de si el dispositivo se crea en el modo de procesamiento de vértices de software o se cambia al modo de procesamiento de vértices de software).

El único requisito para configurar los parámetros de ventanilla para un dispositivo de representación es establecer el volumen de recorte de la ventanilla. Para ello, inicialice y establezca valores de recorte para el volumen de recorte y para la superficie de destino de representación. Normalmente, las ventanillas se establecen para representarse en el área completa de la superficie de destino de representación, pero esto no es un requisito.

Puede usar la siguiente configuración para que los miembros de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) lo consigan en C++.


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Después de establecer los valores en la estructura [**D3DVIEWPORT9,**](d3dviewport9.md) aplique los parámetros de ventanilla al dispositivo mediante una llamada a su [**método IDirect3DDevice9::SetViewport.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) En el ejemplo de código siguiente se muestra el aspecto que podría tener esta llamada.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Si la llamada se realiza correctamente, se establecen los parámetros de la ventanilla y se harán efectivos la próxima vez que se llame a un método de representación. Para realizar cambios en los parámetros de la ventanilla, solo tiene que actualizar los valores de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) y llamar de nuevo a [**IDirect3DDevice9::SetViewport.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

> [!Note]  
> Los [**miembros de estructura D3DVIEWPORT9**](d3dviewport9.md) MinZ y MaxZ indican los intervalos de profundidad en los que se representará la escena y no se usan para el recorte. La mayoría de las aplicaciones establecen estos miembros en 0.0 y 1.0 para permitir que el sistema se represente en todo el intervalo de valores de profundidad del búfer de profundidad. En algunos casos, puede lograr efectos especiales mediante otros intervalos de profundidad. Por ejemplo, para representar una presentación de cara a cara en un juego, puede establecer ambos valores en 0.0 para forzar que el sistema represente objetos en una escena en primer plano, o bien puede establecer ambos en 1.0 para representar un objeto que siempre debe estar en segundo plano.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
