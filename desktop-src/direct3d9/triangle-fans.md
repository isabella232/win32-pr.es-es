---
description: Un ventilador de triángulo es similar a una franja de triángulo, excepto en que todos los triángulos comparten un vértice, tal como se muestra en la siguiente ilustración.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventiladores de triángulo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553776"
---
# <a name="triangle-fans-direct3d-9"></a>Ventiladores de triángulo (Direct3D 9)

Un ventilador de triángulo es similar a una franja de triángulo, excepto en que todos los triángulos comparten un vértice, tal como se muestra en la siguiente ilustración.

![Ilustración de un ventilador de triángulo](images/trifan.gif)

El sistema utiliza los vértices V2, V3 y V1 para dibujar el primer triángulo; V3, V4 y V1 para dibujar el segundo triángulo; V4, V5 y V1 para dibujar el tercer triángulo; etc. Cuando está habilitado el sombreado plano, el sistema sombrea el triángulo con el color del primer vértice.

En la ilustración siguiente se muestra un ventilador de triángulo representado.

![Ilustración de un ventilador de triángulo representado](images/tfan2.gif)

En el código siguiente se muestra cómo crear vértices para este ventilador de triángulo.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



En el ejemplo de código siguiente se muestra cómo representar este ventilador de triángulo en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



Los ventiladores de triángulo no se admiten en Direct3D 10 o versiones posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos primitivos](primitives.md)
</dt> </dl>

 

 
