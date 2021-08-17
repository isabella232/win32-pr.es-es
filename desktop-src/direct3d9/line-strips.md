---
description: Una franja de líneas es una primitiva que se compone de segmentos de línea conectados.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Franjas de línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8ba98518cac542a9b8272e4f96494889ef24f269744626aa24e882c7af509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799641"
---
# <a name="line-strips"></a>Franjas de línea

Una franja de líneas es una primitiva que se compone de segmentos de línea conectados. La aplicación puede usar franjas de línea para crear polígonos que no están cerrados. Un polígono cerrado es un polígono cuyo último vértice está conectado a su primer vértice mediante un segmento de línea. Si la aplicación crea polígonos basados en franjas de línea, no se garantiza que los vértices sean coplanares.

En la ilustración siguiente se muestra una franja de líneas representado.

![ilustración de una franja de líneas](images/linstrip.gif)

El código siguiente muestra cómo crear vértices para esta franja de líneas.


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



En el ejemplo de código siguiente se muestra cómo representar una franja de líneas en Direct3D 9 mediante [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos primitivos](primitives.md)
</dt> </dl>

 

 
