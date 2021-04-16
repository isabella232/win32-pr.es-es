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
# <a name="setting-the-stream-source-direct3d-9"></a><span data-ttu-id="e10cc-103">Establecer el origen de la secuencia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e10cc-103">Setting the Stream Source (Direct3D 9)</span></span>

<span data-ttu-id="e10cc-104">El método [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) enlaza un búfer de vértice a un flujo de datos de dispositivo, creando una asociación entre los datos de vértice y uno de varios puertos de flujo de datos que alimentan las funciones de procesamiento primitiva.</span><span class="sxs-lookup"><span data-stu-id="e10cc-104">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="e10cc-105">Las referencias reales a los datos de la secuencia no se producen hasta que se llama a un método de dibujo, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="e10cc-105">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="e10cc-106">Un flujo se define como una matriz uniforme de datos de componentes, donde cada componente consta de uno o varios elementos que representan una sola entidad, como posición, normal, color, etc.</span><span class="sxs-lookup"><span data-stu-id="e10cc-106">A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="e10cc-107">El parámetro STRIDE especifica el tamaño del componente, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e10cc-107">The Stride parameter specifies the size of the component, in bytes.</span></span>

<span data-ttu-id="e10cc-108">El código siguiente muestra cómo establecer el origen de la secuencia y dibujar su contenido.</span><span class="sxs-lookup"><span data-stu-id="e10cc-108">The following code demonstrates setting the stream source and drawing its contents.</span></span> <span data-ttu-id="e10cc-109">La \_ variable g pVB es un LPDIRECT3DVERTEXBUFFER9 que contiene datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="e10cc-109">The g\_pVB variable is a LPDIRECT3DVERTEXBUFFER9 that contains vertex data.</span></span>


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



<span data-ttu-id="e10cc-110">Para obtener más información sobre este código, vea el tutorial siguiente: [tutorial 3: usar matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e10cc-110">For more information about this code see the following tutorial: [Tutorial 3: Using Matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e10cc-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e10cc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e10cc-112">Representación de primitivas</span><span class="sxs-lookup"><span data-stu-id="e10cc-112">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
