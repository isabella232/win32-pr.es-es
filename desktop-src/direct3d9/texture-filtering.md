---
description: Cuando Direct3D representa una primitiva, asigna la primitiva 3D en una pantalla 2D.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Filtrado de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faeeb83e1a3bc7fc03534771b15b6076aeb48f8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495281"
---
# <a name="texture-filtering-direct3d-9"></a>Filtrado de texturas (Direct3D 9)

Cuando Direct3D representa una primitiva, asigna la primitiva 3D en una pantalla 2D. Si el primitivo tiene una textura, Direct3D debe usar esa textura para generar un color para cada píxel de la imagen representada en 2D de la primitiva. Para cada píxel de la imagen en pantalla del primitivo, debe obtener un valor de color de la textura. Este proceso se denomina filtrado de textura.

Cuando se realiza una operación de filtro de textura, la textura utilizada normalmente también se amplía o reducida. En otras palabras, se asigna a una imagen primitiva que es mayor o menor que sí misma. La ampliación de una textura puede dar lugar a que se asignen muchos píxeles a un textura. El resultado puede ser una apariencia fragmentada. La minificación de una textura suele significar que se asigna un solo píxel a muchos textura. La imagen resultante puede ser borrosa o tiene un alias. Para resolver estos problemas, se debe realizar alguna combinación de los colores de textura para llegar a un color para el píxel.

Direct3D simplifica el proceso complejo de filtrado de texturas. Proporciona tres tipos de filtros de texturas: filtrado lineal, filtrado anisotrópico y filtrado de mipmap. Si selecciona ningún filtro de textura, Direct3D utiliza una técnica denominada muestreo de punto más cercano.

Cada tipo de filtrado de texturas tiene ventajas y desventajas. Por ejemplo, el filtrado de texturas lineal puede producir bordes escalonados o una apariencia fragmentada en la imagen final. Sin embargo, se trata de un método de filtrado de texturas de bajo costo computacional. El filtrado con los mapas de MIP normalmente produce los mejores resultados, especialmente cuando se combina con el filtrado anisotrópico. Sin embargo, requiere la mayor parte de la memoria de las técnicas que admite Direct3D.

Las aplicaciones que usan punteros de interfaz de textura deben establecer el método de filtrado de textura actual llamando al método [**IDirect3DDevice9:: SetSamplerState**](/windows/desktop/api) . Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que está seleccionando un método de filtrado de textura. Pase D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER para el segundo parámetro con el fin de establecer el filtro de ampliación, minificación o mipmapping. Pase un miembro del tipo enumerado [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) como valor del tercer parámetro.

En esta sección se presentan los métodos de filtrado de textura que admite Direct3D. Se organiza en los temas siguientes.

-   [Muestreo de punto más cercano (Direct3D 9)](nearest-point-sampling.md)
-   [Filtrado de textura lineal (Direct3D 9)](linear-texture-filtering.md)
-   [Filtrado de textura bilineal (Direct3D 9)](bilinear-texture-filtering.md)
-   [Filtrado de texturas anisotrópico (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Filtrado de textura con mapas MIP (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Aunque los Estados de representación del filtrado de textura presentes en el tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) se sustituyen por los Estados de fase de textura, [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate), en lugar de la versión IDirect3DDevice2, no produce un error si intenta utilizarlos. En su lugar, el sistema asigna los efectos de estos Estados de representación a la primera fase en cascada de múltiples texturas, fase 0. Las aplicaciones no deben mezclar los Estados de representación heredados con sus Estados de fase de textura correspondientes, ya que se pueden producir resultados imprevisibles.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
