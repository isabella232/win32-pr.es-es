---
description: 'El método IDirect3DDevice9:: SetStreamSource enlaza un búfer de vértice a un flujo de datos de dispositivo, creando una asociación entre los datos de vértice y uno de varios puertos de flujo de datos que alimentan las funciones de procesamiento primitiva.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Establecer el origen de la secuencia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537587"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Establecer el origen de la secuencia (Direct3D 9)

El método [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) enlaza un búfer de vértice a un flujo de datos de dispositivo, creando una asociación entre los datos de vértice y uno de varios puertos de flujo de datos que alimentan las funciones de procesamiento primitiva. Las referencias reales a los datos de la secuencia no se producen hasta que se llama a un método de dibujo, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Un flujo se define como una matriz uniforme de datos de componentes, donde cada componente consta de uno o varios elementos que representan una sola entidad, como posición, normal, color, etc. El parámetro STRIDE especifica el tamaño del componente, en bytes.

El código siguiente muestra cómo establecer el origen de la secuencia y dibujar su contenido. La \_ variable g pVB es un LPDIRECT3DVERTEXBUFFER9 que contiene datos de vértice.


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



Para obtener más información sobre este código, vea el tutorial siguiente: [tutorial 3: usar matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de primitivas](rendering-primitives.md)
</dt> </dl>

 

 
