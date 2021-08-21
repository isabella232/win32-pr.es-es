---
description: Un ventilador de triángulo es similar a una franja de triángulo, salvo que todos los triángulos comparten un vértice, como se muestra en la ilustración siguiente.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Triángulos de ventiladores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806dc57545f4cb8341eee2b586aa062ba93d98568e6269e209dbf616fbb081d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044186"
---
# <a name="triangle-fans-direct3d-9"></a>Triángulos de ventiladores (Direct3D 9)

Un ventilador de triángulo es similar a una franja de triángulo, salvo que todos los triángulos comparten un vértice, como se muestra en la ilustración siguiente.

![ilustración de un ventilador de triángulo](images/trifan.gif)

El sistema usa los vértices v2, v3 y v1 para dibujar el primer triángulo; v3, v4 y v1 para dibujar el segundo triángulo; v4, v5 y v1 para dibujar el tercer triángulo; y así sucesivamente. Cuando el sombreado plano está habilitado, el sistema sombrea el triángulo con el color de su primer vértice.

En la ilustración siguiente se muestra un ventilador de triángulo representado.

![ilustración de un ventilador de triángulo representado](images/tfan2.gif)

El código siguiente muestra cómo crear vértices para este ventilador de triángulo.


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



En el ejemplo de código siguiente se muestra cómo representar este ventilador de triángulo en Direct3D 9 mediante [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


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

 

 
