---
description: Una lista de triángulos es una lista de triángulos aislados. Es posible que se acerquen entre sí. Una lista de triángulos debe tener al menos tres vértices y el número total de vértices debe ser divisible entre tres.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Listas de triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0f9df4d9a0a6d883abd2ccf6b4f3e86c03bb54bcc404901b3c3fa6d10ede03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797447"
---
# <a name="triangle-lists"></a>Listas de triángulos

Una lista de triángulos es una lista de triángulos aislados. Es posible que se acerquen entre sí. Una lista de triángulos debe tener al menos tres vértices y el número total de vértices debe ser divisible entre tres.

Use listas de triángulos para crear un objeto que se compone de partes desconexas. Por ejemplo, una manera de crear una pared de campo de fuerza en un juego 3D es especificar una lista grande de triángulos pequeños y no conectados. A continuación, aplique un material y una textura que parezca emitir luz a la lista de triángulos. Parece que cada triángulo de la pared se desluce. La escena detrás de la pared se vuelve parcialmente visible a través de los huecos entre los triángulos, como podría esperar un jugador al mirar un campo de fuerza.

Las listas de triángulos también son útiles para crear primitivas que tienen bordes nítidos y se sombrean con sombreado de Gouraud. Vea [Vectores normales de caras y vértices (Direct3D 9).](face-and-vertex-normal-vectors.md)

En la ilustración siguiente se muestra una lista de triángulos representados.

![ilustración de una lista de triángulos representados](images/trilist.png)

El código siguiente muestra cómo crear vértices para esta lista de triángulos.


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



En el ejemplo de código siguiente se muestra cómo representar esta lista de triángulos en Direct3D 9 mediante [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



También puede usar franjas de triángulos para representar triángulos que no están conectados entre sí. Para ello, especifique un triángulo degenerado (es decir, un triángulo con tamaño cero) en la lista; esto creará una línea entre los dos triángulos que no aparecerán durante la representación. Por ejemplo, para representar solo el primer y el último triángulo del ejemplo anterior, inicialice el búfer de vértices con los siguientes vértices:


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

 

 
