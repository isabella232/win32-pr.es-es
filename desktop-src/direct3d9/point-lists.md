---
description: Una lista de puntos es una colección de vértices que se representan como puntos aislados. La aplicación puede utilizarlos en escenas 3D para los campos de estrella o líneas de puntos en la superficie de un polígono.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Listas de puntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806235"
---
# <a name="point-lists"></a>Listas de puntos

Una lista de puntos es una colección de vértices que se representan como puntos aislados. La aplicación puede utilizarlos en escenas 3D para los campos de estrella o líneas de puntos en la superficie de un polígono.

En la ilustración siguiente se muestra una lista de puntos representados.

![Ilustración de una lista de puntos](images/pointlst.png)

La aplicación puede aplicar materiales y texturas a una lista de puntos. Los colores del material o la textura solo aparecen en los puntos dibujados y no en cualquier punto entre los puntos.

En el código siguiente se muestra cómo crear vértices para esta lista de puntos.


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



En el ejemplo de código siguiente se muestra cómo representar esta lista de puntos en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos primitivos](primitives.md)
</dt> </dl>

 

 
