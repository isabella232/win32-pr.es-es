---
title: Introducción a las texturas en Direct3D 11
description: Un recurso de textura es una colección estructurada de datos diseñada para almacenar textura.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fcafdfb9caf53a27e60956c8182ae3ef95008e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903613"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Introducción a las texturas en Direct3D 11

Un recurso de textura es una colección estructurada de datos diseñada para almacenar textura. Un textura representa la unidad más pequeña de una textura que se puede leer o escribir en la canalización. A diferencia de los búferes, las texturas se pueden filtrar por muestras de texturas, ya que las unidades de sombreador las leen. El tipo de textura afecta al modo en que se filtra la textura. Cada textura contiene de 1 a 4 componentes, organizados en uno de los formatos de DXGI definidos por la \_ enumeración de formato de dxgi.

Las texturas se crean como un recurso estructurado con un tamaño conocido. Sin embargo, cada textura puede ser de tipo o sin tipo cuando se crea el recurso, siempre que el tipo se especifique por completo utilizando una vista cuando la textura esté enlazada a la canalización.

## <a name="texture-types"></a>Tipos de textura

Hay varios tipos de texturas: 1D, 2D y 3D, cada una de las cuales se puede crear con o sin mapas MIP. Direct3D 11 también admite matrices de texturas y texturas multimuestreadas.

-   [Texturas 1D](#1d-textures)
-   [Matrices de texturas 1D](#1d-texture-arrays)
-   [Texturas 2D y matrices de textura 2D](#2d-textures-and-2d-texture-arrays)
-   [Texturas 3D](#3d-textures)

### <a name="1d-textures"></a>Texturas 1D

Una textura 1D en su forma más simple contiene datos de textura que se pueden direccionar con una sola coordenada de textura. se puede visualizar como una matriz de textura, tal como se muestra en la siguiente ilustración. las texturas 1D se representan mediante la interfaz [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) .

![Ilustración de una textura 1D](images/d3d10-1d-texture.png)

Cada textura contiene una serie de componentes de color dependiendo del formato de los datos almacenados. Agregar más complejidad, puede crear una textura 1D con niveles de mipmap, tal como se muestra en la siguiente ilustración.

![Ilustración de una textura 1D con niveles de mipmap](images/d3d10-resource-texture1d.png)

Un nivel de mipmap es una textura que es una potencia de dos menor que el nivel superior. El nivel más alto contiene la mayoría de los detalles, cada nivel posterior es más pequeño. En el caso de un mipmap 1D, el nivel más pequeño contiene un textura. Además, los niveles de MIP siempre reducen hasta 1:1. Cuando se generan los mapas MIP para una textura de tamaño impar, el siguiente nivel inferior siempre es igual de tamaño (excepto cuando el nivel más bajo llega a 1). Por ejemplo, el diagrama muestra una textura 5x1 cuyo siguiente nivel más bajo es una textura 2x1, cuyo nivel de MIP siguiente (y último) es una textura de tamaño 1x1. Los niveles se identifican mediante un índice denominado LOD (nivel de detalle) que se usa para tener acceso a la textura más pequeña al representar geometría que no es tan cercana a la cámara.

### <a name="1d-texture-arrays"></a>Matrices de texturas 1D

Direct3D 11 también admite matrices de texturas. La interfaz [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) también representa una matriz de textura 1D. Una matriz de texturas 1D es conceptualmente similar a la siguiente ilustración.

![Ilustración de una matriz de texturas 1D](images/d3d10-resource-texture1darray.png)

Esta matriz de texturas contiene tres texturas. Cada una de las tres texturas tiene un ancho de textura de 5 (que es el número de elementos de la primera capa). Cada textura también contiene un mipmap de 3 niveles.

Todas las matrices de texturas en Direct3D son una matriz de texturas homogénea; Esto significa que todas las texturas de una matriz de textura deben tener el mismo formato de datos y el mismo tamaño (incluido el ancho de la textura y el número de niveles de mipmap). Puede crear matrices de texturas de diferentes tamaños, siempre que todas las texturas de cada matriz coincidan en tamaño.

### <a name="2d-textures-and-2d-texture-arrays"></a>Texturas 2D y matrices de textura 2D

Un recurso Texture2D contiene una cuadrícula 2D de textura. Cada textura es direccionable por un vector u, v. Dado que se trata de un recurso de textura, puede contener niveles de mipmap y Subrecursos. las texturas 2D se representan mediante la interfaz [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) . Un recurso de textura 2D totalmente rellenado tiene un aspecto similar al de la siguiente ilustración.

![Ilustración de un recurso de textura 2D](images/d3d10-resource-texture2d.png)

Este recurso de textura contiene una sola textura 3x5 con tres niveles de mipmap.

Un recurso de matriz de textura 2D es una matriz homogénea de texturas 2D; es decir, cada textura tiene el mismo formato de datos y dimensiones (incluidos los niveles de mipmap). La interfaz [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) también representa una matriz de textura 2D. Tiene un diseño similar al de la matriz de texturas 1D, salvo que las texturas contienen ahora datos 2D, como se muestra en la siguiente ilustración.

![Ilustración de una matriz de texturas 2D](images/d3d10-resource-texture2darray.png)

Esta matriz de texturas contiene tres texturas; cada textura se 3x5 con dos niveles de mipmap.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Usar una matriz de textura 2D como un cubo de textura

Un cubo de textura es una matriz de textura 2D que contiene 6 texturas, una para cada una de las caras del cubo. Un cubo de textura totalmente rellenado tiene un aspecto similar al de la siguiente ilustración.

![Ilustración de una matriz de texturas 2D que representan un cubo de textura](images/d3d10-resource-texturecube.png)

Una matriz de textura 2D que contiene 6 texturas se puede leer desde los sombreadores con las funciones intrínsecas de mapa de cubo, una vez enlazadas a la canalización con una vista de textura de cubo. Los cubos de textura se dirigen desde el sombreador con un vector 3D que señala hacia fuera del centro del cubo de textura.

> [!Note]  
> Los dispositivos que se crean [**con \_ un nivel de características de 10 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) y versiones posteriores pueden admitir matrices de cubos de textura en las que el número de texturas es igual al número de cubos de textura en una matriz multiplicado por seis. Los dispositivos que se crean con un [**\_ nivel de características de 10 0**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) solo admiten un único cubo de textura de seis caras. Además, Direct3D 11 no es compatible con cubemaps parciales.

 

### <a name="3d-textures"></a>Texturas 3D

Un recurso de textura 3D (también conocido como textura de volumen) contiene un volumen 3D de textura. Dado que se trata de un recurso de textura, puede contener niveles de mipmap. las texturas 3D se representan mediante la interfaz [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) . Una textura 3D totalmente rellenada es similar a la siguiente ilustración.

![Ilustración de un recurso de textura 3D](images/d3d10-resource-texture3d.png)

Cuando un segmento MIP de textura 3D se enlaza como salida de destino de representación (con una vista de destino de representación), la textura 3D se comporta de forma idéntica a una matriz de textura 2D con n segmentos. El segmento de representación determinado se elige en la fase de sombreador de geometría, declarando un componente escalar de los datos de salida como el \_ valor del sistema VP RenderTargetArrayIndex.

No hay ningún concepto de una matriz de textura 3D; por lo tanto, un subrecurso de textura 3D es un solo nivel de mipmap.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




