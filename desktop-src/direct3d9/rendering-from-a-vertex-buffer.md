---
description: 'La representación de datos de vértices desde un búfer de vértice requiere algunos pasos. En primer lugar, debe establecer el origen de la secuencia llamando al método IDirect3DDevice9:: SetStreamSource, como se muestra en el ejemplo siguiente.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Representar desde un búfer de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151972"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Representar desde un búfer de vértice (Direct3D 9)

La representación de datos de vértices desde un búfer de vértice requiere algunos pasos. En primer lugar, debe establecer el origen de la secuencia llamando al método [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , como se muestra en el ejemplo siguiente.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



El primer parámetro de [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indica a Direct3D el origen del flujo de datos del dispositivo. El segundo parámetro es el búfer de vértices que se va a enlazar al flujo de datos. El tercer parámetro es el desplazamiento desde el principio del flujo hasta el principio de los datos del vértice, en bytes. El cuarto parámetro es el paso del componente, en bytes. En el código de ejemplo anterior, se usa el tamaño de un CUSTOMVERTEX para el paso del componente.

El siguiente paso es informar a Direct3D del sombreador de vértices que se va a usar mediante una llamada al método [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) . En el código de ejemplo siguiente se establece un código de FVF para el sombreador de vértices. Esto informa a Direct3D de los tipos de vértices con los que se está tratando.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Después de establecer el origen de flujo y el sombreador de vértices, cualquier método draw usará el búfer de vértices. En el ejemplo de código siguiente se muestra cómo representar los vértices de un búfer de vértice con el método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



El segundo parámetro que [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) acepta es el índice del primer vector del búfer de vértice que se va a cargar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> <dt>

[Representación de búferes de vértices y de índices (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
