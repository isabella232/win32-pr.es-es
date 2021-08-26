---
title: Introducción a las texturas en Direct3D 11
description: Un recurso de textura es una colección estructurada de datos diseñada para almacenar elementos de textura.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3bfd19f018ff3f3d9fc8eb1608212a93b4364de2cc24b6213763dfcda4ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027905"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Introducción a las texturas en Direct3D 11

Un recurso de textura es una colección estructurada de datos diseñada para almacenar elementos de textura. Un texel representa la unidad más pequeña de una textura que se puede leer o escribir en la canalización. A diferencia de los búferes, las texturas se pueden filtrar por muestreadores de textura a medida que las unidades de sombreador las leen. El tipo de textura afecta a cómo se filtra la textura. Cada texel contiene de 1 a 4 componentes, organizados en uno de los formatos DXGI definidos por la enumeración DXGI \_ FORMAT.

Las texturas se crean como un recurso estructurado con un tamaño conocido. Sin embargo, cada textura se puede escribir o sin tipo cuando se crea el recurso, siempre y cuando el tipo se especifique completamente mediante una vista cuando la textura está enlazada a la canalización.

## <a name="texture-types"></a>Tipos de textura

Hay varios tipos de texturas: 1D, 2D, 3D, cada una de las cuales se puede crear con o sin mapas mip. Direct3D 11 también admite matrices de texturas y texturas multimuestreo.

-   [Texturas 1D](#1d-textures)
-   [Matrices de textura 1D](#1d-texture-arrays)
-   [Texturas 2D y matrices de texturas 2D](#2d-textures-and-2d-texture-arrays)
-   [Texturas 3D](#3d-textures)

### <a name="1d-textures"></a>Texturas 1D

Una textura 1D en su forma más sencilla contiene datos de textura que se pueden abordar con una sola coordenada de textura; se puede visualizar como una matriz de elementos de textura, como se muestra en la ilustración siguiente. Las texturas 1D se representan mediante la [**interfaz ID3D11Texture1D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)

![ilustración de una textura 1d](images/d3d10-1d-texture.png)

Cada texel contiene una serie de componentes de color según el formato de los datos almacenados. Si agrega más complejidad, puede crear una textura 1D con niveles de mapa mip, como se muestra en la ilustración siguiente.

![ilustración de una textura 1d con niveles de mapa mip](images/d3d10-resource-texture1d.png)

Un nivel de mapa mip es una textura que es una potencia de dos más pequeña que el nivel por encima de él. El nivel superior contiene la mayor cantidad de detalles; cada nivel posterior es menor. Para un mapa mipmap 1D, el nivel más pequeño contiene un texel. Además, los niveles de MIP siempre se reducen a 1:1. Cuando se generan mapas MIP para una textura de tamaño impar, el siguiente nivel inferior siempre es de tamaño par (excepto cuando el nivel más bajo alcanza 1). Por ejemplo, el diagrama muestra una textura de 5x1 cuyo siguiente nivel más bajo es una textura 2x1, cuyo siguiente (y último) nivel de mip es una textura de tamaño 1x1. Los niveles se identifican mediante un índice denominado LOD (nivel de detalle) que se usa para acceder a la textura más pequeña al representar geometría que no está tan cerca de la cámara.

### <a name="1d-texture-arrays"></a>Matrices de textura 1D

Direct3D 11 también admite matrices de texturas. Una matriz de textura 1D también se representa mediante la [**interfaz ID3D11Texture1D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) Una matriz de texturas 1D se parece conceptualmente a la ilustración siguiente.

![ilustración de una matriz de texturas 1d](images/d3d10-resource-texture1darray.png)

Esta matriz de texturas contiene tres texturas. Cada una de las tres texturas tiene un ancho de textura de 5 (que es el número de elementos de la primera capa). Cada textura también contiene un mapa mipmap de 3 capas.

Todas las matrices de texturas de Direct3D son una matriz homogéneo de texturas; esto significa que todas las texturas de una matriz de texturas deben tener el mismo formato y tamaño de datos (incluido el ancho de textura y el número de niveles de mapa mip). Puede crear matrices de textura de diferentes tamaños, siempre y cuando todas las texturas de cada matriz coincidan en tamaño.

### <a name="2d-textures-and-2d-texture-arrays"></a>Texturas 2D y matrices de texturas 2D

Un recurso Texture2D contiene una cuadrícula 2D de elementos de textura. Cada texel es direccionable mediante un vector u, v. Puesto que es un recurso de textura, puede contener niveles de mapa mip y subrecursos. Las texturas 2D se representan mediante la [**interfaz ID3D11Texture2D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) Un recurso de textura 2D totalmente rellenado es similar al de la ilustración siguiente.

![ilustración de un recurso de textura 2d](images/d3d10-resource-texture2d.png)

Este recurso de textura contiene una sola textura de 3x5 con tres niveles de mapa mip.

Un recurso de matriz de textura 2D es una matriz homogéneo de texturas 2D; es decir, cada textura tiene el mismo formato de datos y dimensiones (incluidos los niveles de mapa mip). Una matriz de texturas 2D también se representa mediante la [**interfaz ID3D11Texture2D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) Tiene un diseño similar al de la matriz de texturas 1D, salvo que las texturas ahora contienen datos 2D, como se muestra en la ilustración siguiente.

![ilustración de una matriz de texturas 2d](images/d3d10-resource-texture2darray.png)

Esta matriz de texturas contiene tres texturas; cada textura es 3x5 con dos niveles de mapa mip.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Usar una matriz de texturas 2D como un cubo de textura

Un cubo de textura es una matriz de textura 2D que contiene 6 texturas, una para cada cara del cubo. Un cubo de textura totalmente rellenado se parece a la ilustración siguiente.

![ilustración de una matriz de texturas 2d que representan un cubo de textura](images/d3d10-resource-texturecube.png)

Una matriz de texturas 2D que contiene 6 texturas se puede leer desde los sombreadores con las funciones intrínsecas del mapa de cubo, después de enlazarse a la canalización con una vista de textura de cubo. Los cubos de textura se abordan desde el sombreador con un vector 3D que señala desde el centro del cubo de textura.

> [!Note]  
> Los dispositivos que cree con [**\_ 10 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) nivel de característica y superiores pueden admitir matrices de cubos de textura en los que el número de texturas es igual al número de cubos de textura de una matriz por seis. Los dispositivos que cree con [**el nivel de característica \_ 10 0**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) solo admiten un único cubo de textura de seis caras. Además, Direct3D 11 no admite mapas de cubo parciales.

 

### <a name="3d-textures"></a>Texturas 3D

Un recurso de textura 3D (también conocido como textura de volumen) contiene un volumen 3D de texturas. Dado que es un recurso de textura, puede contener niveles de mapa mip. Las texturas 3D se representan mediante la [**interfaz ID3D11Texture3D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) Una textura 3D totalmente rellenada es similar a la siguiente ilustración.

![ilustración de un recurso de textura 3D](images/d3d10-resource-texture3d.png)

Cuando un segmento mipmap de textura 3D se enlaza como una salida de destino de representación (con una vista render-target), la textura 3D se comporta de forma idéntica a una matriz de textura 2D con n segmentos. El segmento de representación determinado se elige en la fase del sombreador de geometría, declarando un componente escalar de los datos de salida como el valor del sistema \_ SV RenderTargetArrayIndex.

No hay ningún concepto de una matriz de texturas 3D; por lo tanto, un subcurso de textura 3D es un único nivel de mapa mip.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




