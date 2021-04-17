---
description: Una lista de triángulo es una lista de triángulos aislados. Pueden estar o no cercanos entre sí. Una lista de triángulos debe tener al menos tres vértices y el número total de vértices debe ser divisible por tres.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Listas de triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705252"
---
# <a name="triangle-lists"></a>Listas de triángulos

Una lista de triángulo es una lista de triángulos aislados. Pueden estar o no cercanos entre sí. Una lista de triángulos debe tener al menos tres vértices y el número total de vértices debe ser divisible por tres.

Use listas de triángulos para crear un objeto compuesto por piezas disjuntos. Por ejemplo, una forma de crear un muro de campo forzada en un juego 3D es especificar una lista grande de triángulos pequeños y no conectados. A continuación, aplique un material y una textura que parezcan emitir luz a la lista de triángulos. Cada triángulo de la pared aparece iluminado. La escena detrás de la pared se hace visible parcialmente a través de los huecos entre los triángulos, ya que un reproductor podría esperar al mirar un campo de fuerza.

Las listas de triángulos también son útiles para crear primitivas que tienen bordes nítidos y se sombrean con sombreado Gouraud. Consulte [vectores normales de cara y vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).

En la ilustración siguiente se muestra una lista de triángulos representada.

![Ilustración de una lista de triángulos representada](images/trilist.png)

En el código siguiente se muestra cómo crear vértices para esta lista de triángulos.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}

};
```



En el ejemplo de código siguiente se muestra cómo representar esta lista de triángulos en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



También puede usar bandas triangulares para representar triángulos que no están conectados entre sí. Para ello, especifique un triángulo degenerado (es decir, un triángulo con tamaño cero) en la lista; Esto creará una línea entre los dos triángulos que no aparecerá durante la representación. Por ejemplo, para representar solo el primer y último triángulo del ejemplo anterior, inicialice el búfer de vértices con los siguientes vértices:


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos primitivos](primitives.md)
</dt> </dl>

 

 
