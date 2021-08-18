---
description: El método IDirect3DDevice9::SetStreamSource enlaza un búfer de vértices a un flujo de datos de dispositivo, lo que crea una asociación entre los datos del vértice y uno de los varios puertos de flujo de datos que alimentan las funciones de procesamiento primitivo.
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Establecer el origen de la secuencia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91bd760b23204de2c6ccd313b164ac7536c7db2d3e2da26d7e40b7d98daa60a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044243"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Establecer el origen de la secuencia (Direct3D 9)

El [**método IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) enlaza un búfer de vértices a un flujo de datos de dispositivo, lo que crea una asociación entre los datos del vértice y uno de los varios puertos de flujo de datos que alimentan las funciones de procesamiento primitivo. Las referencias reales a los datos de flujo no se producen hasta que se llama a un método de dibujo, como [**IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)

Una secuencia se define como una matriz uniforme de datos de componentes, donde cada componente consta de uno o varios elementos que representan una sola entidad, como la posición, la normal, el color, etc. El parámetro Stride especifica el tamaño del componente, en bytes.

En el código siguiente se muestra cómo establecer el origen de la secuencia y dibujar su contenido. La variable \_ g pVB es un LPDIRECT3DVERTEXBUFFER9 que contiene datos de vértices.


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



Para obtener más información sobre este código, vea el siguiente tutorial: [Tutorial 3: Uso de matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de primitivas](rendering-primitives.md)
</dt> </dl>

 

 
