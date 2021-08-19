---
description: La representación de datos de vértices desde un búfer de vértices requiere unos pocos pasos. En primer lugar, debe establecer el origen de la secuencia llamando al método IDirect3DDevice9::SetStreamSource, como se muestra en el ejemplo siguiente.
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Representación desde un búfer de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ee3d477fc812d2dabed765e28bb14452a6badf746a331a13283108ef46b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520076"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Representación desde un búfer de vértices (Direct3D 9)

La representación de datos de vértices desde un búfer de vértices requiere unos pocos pasos. En primer lugar, debe establecer el origen de la secuencia llamando al método [**IDirect3DDevice9::SetStreamSource,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) como se muestra en el ejemplo siguiente.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



El primer parámetro de [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indica a Direct3D el origen del flujo de datos del dispositivo. El segundo parámetro es el búfer de vértices que se va a enlazar al flujo de datos. El tercer parámetro es el desplazamiento desde el principio de la secuencia hasta el principio de los datos del vértice, en bytes. El cuarto parámetro es el paso del componente, en bytes. En el código de ejemplo anterior, se usa el tamaño de customvertex para el paso del componente.

El siguiente paso consiste en informar a Direct3D qué sombreador de vértices usar llamando al [**método IDirect3DDevice9::SetVertexShader.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) El código de ejemplo siguiente establece un código FVF para el sombreador de vértices. Esto informa a Direct3D de los tipos de vértices con los que está trabajando.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Después de establecer el origen de la secuencia y el sombreador de vértices, los métodos de dibujo usarán el búfer de vértices. En el ejemplo de código siguiente se muestra cómo representar vértices desde un búfer de vértices con el [**método IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



El segundo parámetro que [**acepta IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) es el índice del primer vector del búfer de vértices que se va a cargar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> <dt>

[Representación a partir de búferes de vértices e índices (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
