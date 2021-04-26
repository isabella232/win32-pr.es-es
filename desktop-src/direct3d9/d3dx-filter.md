---
description: Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6e1ab3ab51a73277da685b7ac562e84d1b94a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997332"
---
# <a name="d3dx_filter"></a>FILTRO \_ D3DX

Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar.



| \#Definir                | Descripción                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ FILTER \_ NONE      | No se realizará ningún escalado ni filtrado. Se supone que los píxeles fuera de los límites de la imagen de origen son de color negro transparente.                                                                                 |
| PUNTO DE FILTRO \_ \_ D3DX     | Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.                                                                                                                     |
| D3DX \_ FILTER \_ LINEAR    | Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen. Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.                                          |
| TRIÁNGULO DE FILTRO D3DX \_ \_  | Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino. Este es el más lento de los filtros.                                                                                           |
| CUADRO DE FILTRO \_ \_ D3DX       | Cada píxel se calcula calculando el promedio de un cuadro de 2 x 2(x2) de píxeles a partir de la imagen de origen. Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como es el caso de los mapas mip. |
| REFLEJO DEL FILTRO D3DX \_ \_ \_ U | Los píxeles del borde de la textura en el eje U deben reflejarse, no ajustarse.                                                                                                                           |
| D3DX \_ FILTER \_ MIRROR \_ V | Los píxeles del borde de la textura en el eje v deben reflejarse, no ajustarse.                                                                                                                           |
| REFLEJO DEL FILTRO D3DX \_ \_ \_ W | Los píxeles del borde de la textura en el eje w deben reflejarse, no ajustarse.                                                                                                                           |
| REFLEJO DEL FILTRO D3DX \_ \_    | Especificar esta marca es igual que especificar las marcas D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR V y \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.                                                                     |
| D3DX \_ FILTER \_ DITHER    | La imagen resultante debe estar entrelazada mediante un algoritmo de dither ordenado de 4x4.                                                                                                                                  |
| FILTRO D3DX \_ \_ SRGB \_ EN  | Los datos de entrada están en un espacio de colores sRGB (gamma 2.2).                                                                                                                                                              |
| FILTRO D3DX \_ \_ SRGB \_ OUT | Los datos de salida están en el espacio de color sRGB (gamma 2.2).                                                                                                                                                         |
| FILTRO D3DX \_ \_ SRGB      | Igual que especificar D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.                                                                                                                                       |



 

Cada filtro válido debe contener exactamente una de las marcas siguientes: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX FILTER TRIANGLE o \_ \_ D3DX \_ FILTER \_ BOX. Además, puede usar el operador OR para especificar cero o más de las siguientes marcas opcionales con un filtro válido: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER MIRROR \_ W, D3DX \_ FILTER MIRROR, D3DX FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX FILTER SRGB OUT o \_ \_ \_ D3DX \_ FILTER \_ SRGB.

Especificar D3DX DEFAULT para este parámetro suele ser el equivalente a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER. Sin embargo, D3DX \_ DEFAULT puede tener significados diferentes, dependiendo del método que use el filtro. Por ejemplo:

-   Al usar [**D3DXCreateTextureFromFileEx,**](d3dxcreatetexturefromfileex.md)D3DX DEFAULT se asigna a \_ D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.
-   Cuando se [**usa D3DXFilterTexture,**](d3dxfiltertexture.md)D3DX DEFAULT se asigna a D3DX FILTER BOX si el tamaño de textura es una potencia de \_ dos y \_ \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER \_ en caso contrario.

Haga referencia a cada método para buscar información sobre cómo se asigna el \_ filtro D3DX DEFAULT.

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3dx9tex.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



