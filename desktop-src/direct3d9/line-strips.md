---
description: Una franja de líneas es un primitivo compuesto por segmentos de línea conectados.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Bandas de líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537617"
---
# <a name="line-strips"></a>Bandas de líneas

Una franja de líneas es un primitivo compuesto por segmentos de línea conectados. La aplicación puede usar bandas de líneas para crear polígonos que no están cerrados. Un polígono cerrado es un polígono cuyo último vértice está conectado al primer vértice por un segmento de línea. Si la aplicación crea polígonos basados en franjas de líneas, no se garantiza que los vértices sean coplanares.

En la ilustración siguiente se muestra una franja de líneas representada.

![Ilustración de una franja de líneas](images/linstrip.gif)

En el código siguiente se muestra cómo crear vértices para esta franja de líneas.


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



En el ejemplo de código siguiente se muestra cómo representar una franja de líneas en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


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

 

 
