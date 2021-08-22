---
description: Una lista de líneas es una lista de segmentos aislados y de línea recta.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Listas de líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f06ca68e3fefab1217e77bbf41bc30aa42dac9631b70480fe4bf0a98d38d913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606805"
---
# <a name="line-lists"></a>Listas de líneas

Una lista de líneas es una lista de segmentos aislados y de línea recta. Las listas de líneas son útiles para tareas como agregar aguanieve o lluvia intensa a una escena 3D. Las aplicaciones crean una lista de líneas rellenando una matriz de vértices. Tenga en cuenta que el número de vértices de una lista de líneas debe ser un número par mayor o igual que dos.

En la ilustración siguiente se muestra una lista de líneas representado.

![ilustración de una lista de líneas](images/linelst.png)

Puede aplicar materiales y texturas a una lista de líneas. Los colores del material o textura solo aparecen a lo largo de las líneas dibujadas, no en ningún punto entre las líneas.

El código siguiente muestra cómo crear vértices para esta lista de líneas.


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



En el ejemplo de código siguiente se muestra cómo representar una lista de líneas en Direct3D 9 mediante [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos primitivos](primitives.md)
</dt> </dl>

 

 
