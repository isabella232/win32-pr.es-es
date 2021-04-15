---
description: Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494734"
---
# <a name="d3dx_filter"></a>Filtro de D3DX \_

Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar.



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                | Descripción                                                                                                                                                                                                 |
| D3DX \_ Filter \_ ninguno      | No se llevará a cabo ningún ajuste de escala o filtro. Se supone que los píxeles que están fuera de los límites de la imagen de origen son negros transparentes.                                                                                 |
| \_Punto de filtro de D3DX \_     | Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.                                                                                                                     |
| \_Filtro \_ lineal de D3DX    | Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen. Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.                                          |
| \_Triángulo de filtro de D3DX \_  | Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino. Este es el más lento de los filtros.                                                                                           |
| \_Cuadro de filtro de D3DX \_       | Cada píxel se calcula calculando el promedio de un cuadro 2x2 (x2) de píxeles de la imagen de origen. Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como sucede con los mapas MIP. |
| Reflejo de filtro de D3DX \_ \_ \_ U | Los píxeles que están fuera del borde de la textura en el eje u deben reflejarse, no ajustarse.                                                                                                                           |
| Espejo del filtro de D3DX \_ \_ \_ V | Los píxeles que están fuera del borde de la textura en el eje v deben reflejarse, no ajustarse.                                                                                                                           |
| Reflejo del filtro de D3DX \_ \_ \_ W | Los píxeles que están fuera del borde de la textura en el eje w deben reflejarse, no ajustarse.                                                                                                                           |
| \_Reflejo del filtro de D3DX \_    | La especificación de esta marca es la misma que la especificación de las marcas de la imagen reflejada del filtro de D3DX U, de la versión reflejada del filtro de d3dx \_ \_ \_ \_ \_ \_ \_ \_ \_ .                                                                     |
| \_Interpolación de filtros de D3DX \_    | La imagen resultante debe ser interpolada mediante un algoritmo de tramado ordenado de 4x4.                                                                                                                                  |
| El \_ filtro \_ de D3DX está \_ en sRGB  | Los datos de entrada están en el espacio de colores sRGB (gamma 2,2).                                                                                                                                                              |
| Filtro de D3DX de \_ \_ \_ salida sRGB | Los datos de salida están en el espacio de colores sRGB (gamma 2,2).                                                                                                                                                         |
| Filtro de D3DX \_ \_ sRGB      | Igual que al especificar el \_ filtro de d3dx \_ sRGB \_ en el \| filtro de d3dx \_ \_ \_ .                                                                                                                                       |



 

Cada filtro válido debe contener exactamente una de las marcas siguientes: el \_ filtro \_ de d3dx no, el \_ \_ punto de filtro de d3dx, el filtro de d3dx \_ \_ lineal, el triángulo de filtro de d3dx \_ o el \_ cuadro de filtro de d3dx \_ \_ . Además, puede usar el operador OR para especificar cero o más de las siguientes marcas opcionales con un filtro válido: el filtro de D3DX de la versión u, el reflejado del filtro de d3dx, el filtro de d3dx, el filtro de d3dx y el filtro de d3dx \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ .

Especificar \_ el valor predeterminado de d3dx para este parámetro suele ser el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ . Sin embargo, \_ el valor predeterminado de D3DX puede tener distintos significados, en función del método que use el filtro. Por ejemplo:

-   Cuando se usa [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), el \_ valor predeterminado de d3dx se asigna al filtro de d3dx Triangle del filtro de d3dx \_ \_ \| \_ \_ .
-   Cuando se usa [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ el valor predeterminado de d3dx se asigna al cuadro de filtro de d3dx \_ \_ si el tamaño de la textura es una potencia de dos, y el filtro de d3dx del \_ cuadro de filtro de \_ \| d3dx \_ \_ en caso contrario.

Haga referencia a cada método para comprobar la información sobre cómo \_ se asigna el filtro predeterminado de D3DX.

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3dx9tex. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



