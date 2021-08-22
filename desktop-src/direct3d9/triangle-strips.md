---
description: Una franja de triángulos es una serie de triángulos conectados.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Franjas de triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf229883fa156afc93ca2889a0a97f4f2c3eabbb344fb7551476c98f33905f8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044116"
---
# <a name="triangle-strips"></a>Franjas de triángulos

Una franja de triángulos es una serie de triángulos conectados. Dado que los triángulos están conectados, la aplicación no necesita especificar repetidamente los tres vértices para cada triángulo. Por ejemplo, solo necesita siete vértices para definir la siguiente franja de triángulo.

![ilustración de una franja de triángulo con siete vértices](images/tristrip.png)

El sistema usa vértices v1, v2 y v3 para dibujar el primer triángulo; v2, v4 y v3 para dibujar el segundo triángulo; v3, v4 y v5 para dibujar el tercero; v4, v6 y v5 para dibujar el cuarto; y así sucesivamente. Observe que los vértices del segundo y cuarto triángulo no están en orden; esto es necesario para asegurarse de que todos los triángulos se dibujan en una orientación en el sentido de las agujas del reloj.

La mayoría de los objetos de las escenas 3D se componen de franjas de triángulos. Esto se debe a que las franjas de triángulos se pueden usar para especificar objetos complejos de una manera que haga un uso eficaz de la memoria y el tiempo de procesamiento.

En la ilustración siguiente se muestra una franja de triángulo representada.

![ilustración de una franja de triángulo representado](images/tstrip2.png)

El código siguiente muestra cómo crear vértices para esta franja de triángulo.


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



En el ejemplo de código siguiente se muestra cómo representar esta franja de triángulo en Direct3D 9 mediante [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Use una franja de triángulos para representar triángulos que no están conectados entre sí. Para ello, especifique un triángulo degenerado (es decir, un triángulo cuyo área es cero) en la lista de triángulos. Esto crea una línea entre los dos triángulos que no se representarán. Para representar solo el primer y el último triángulo del ejemplo anterior, modifique el búfer de vértices como se muestra aquí:


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

 

 
