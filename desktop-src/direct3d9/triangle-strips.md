---
description: Una franja de triángulo es una serie de triángulos conectados.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Bandas de triángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555720"
---
# <a name="triangle-strips"></a>Bandas de triángulo

Una franja de triángulo es una serie de triángulos conectados. Dado que los triángulos están conectados, no es necesario que la aplicación especifique repetidamente los tres vértices para cada triángulo. Por ejemplo, solo necesita siete vértices para definir la franja de triángulo siguiente.

![Ilustración de una franja de triángulo con siete vértices](images/tristrip.png)

El sistema utiliza los vértices v1, V2 y v3 para dibujar el primer triángulo; V2, V4 y v3 para dibujar el segundo triángulo; V3, V4 y V5 para dibujar el tercero; V4, V6 y V5 para dibujar el cuarto; etc. Observe que los vértices de los triángulos segundo y cuarto están desordenados; Esto es necesario para asegurarse de que todos los triángulos se dibujan en una orientación en el sentido de las agujas del reloj.

La mayoría de los objetos de escenas 3D se componen de bandas de triángulo. Esto se debe a que las franjas de triángulos se pueden usar para especificar objetos complejos de una manera que haga un uso eficaz de la memoria y el tiempo de procesamiento.

En la ilustración siguiente se muestra una franja de triángulo representada.

![Ilustración de una franja de triángulo representada](images/tstrip2.png)

En el código siguiente se muestra cómo crear vértices para esta franja de triángulo.


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



En el ejemplo de código siguiente se muestra cómo representar esta franja de triángulo en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Use una franja de triángulo para representar triángulos que no estén conectados entre sí. Para ello, especifique un triángulo degenerado (es decir, un triángulo cuya área sea cero) en la lista de triángulos. Esto crea una línea entre los dos triángulos que no se representarán. Para representar solo los triángulos primero y último del ejemplo anterior, modifique el búfer de vértices como se muestra aquí:


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

 

 
