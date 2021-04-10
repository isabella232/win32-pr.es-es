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
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="a9df7-104">Representar desde un búfer de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9df7-104">Rendering from a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="a9df7-105">La representación de datos de vértices desde un búfer de vértice requiere algunos pasos.</span><span class="sxs-lookup"><span data-stu-id="a9df7-105">Rendering vertex data from a vertex buffer requires a few steps.</span></span> <span data-ttu-id="a9df7-106">En primer lugar, debe establecer el origen de la secuencia llamando al método [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a9df7-106">First, you need to set the stream source by calling the [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) method, as shown in the following example.</span></span>


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



<span data-ttu-id="a9df7-107">El primer parámetro de [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indica a Direct3D el origen del flujo de datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9df7-107">The first parameter of [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) tells Direct3D the source of the device data stream.</span></span> <span data-ttu-id="a9df7-108">El segundo parámetro es el búfer de vértices que se va a enlazar al flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="a9df7-108">The second parameter is the vertex buffer to bind to the data stream.</span></span> <span data-ttu-id="a9df7-109">El tercer parámetro es el desplazamiento desde el principio del flujo hasta el principio de los datos del vértice, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a9df7-109">The third parameter is the offset from the beginning of the stream to the beginning of the vertex data, in bytes.</span></span> <span data-ttu-id="a9df7-110">El cuarto parámetro es el paso del componente, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a9df7-110">The fourth parameter is the stride of the component, in bytes.</span></span> <span data-ttu-id="a9df7-111">En el código de ejemplo anterior, se usa el tamaño de un CUSTOMVERTEX para el paso del componente.</span><span class="sxs-lookup"><span data-stu-id="a9df7-111">In the sample code above, the size of a CUSTOMVERTEX is used for the stride of the component.</span></span>

<span data-ttu-id="a9df7-112">El siguiente paso es informar a Direct3D del sombreador de vértices que se va a usar mediante una llamada al método [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="a9df7-112">The next step is to inform Direct3D which vertex shader to use by calling the [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) method.</span></span> <span data-ttu-id="a9df7-113">En el código de ejemplo siguiente se establece un código de FVF para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="a9df7-113">The following sample code sets an FVF code for the vertex shader.</span></span> <span data-ttu-id="a9df7-114">Esto informa a Direct3D de los tipos de vértices con los que se está tratando.</span><span class="sxs-lookup"><span data-stu-id="a9df7-114">This informs Direct3D of the types of vertices it is dealing with.</span></span>


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



<span data-ttu-id="a9df7-115">Después de establecer el origen de flujo y el sombreador de vértices, cualquier método draw usará el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="a9df7-115">After setting the stream source and vertex shader, any draw methods will use the vertex buffer.</span></span> <span data-ttu-id="a9df7-116">En el ejemplo de código siguiente se muestra cómo representar los vértices de un búfer de vértice con el método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="a9df7-116">The code example below shows how to render vertices from a vertex buffer with the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method.</span></span>


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



<span data-ttu-id="a9df7-117">El segundo parámetro que [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) acepta es el índice del primer vector del búfer de vértice que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="a9df7-117">The second parameter that [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepts is the index of the first vector in the vertex buffer to load.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9df7-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9df7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9df7-119">Búferes de vértices</span><span class="sxs-lookup"><span data-stu-id="a9df7-119">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> <dt>

[<span data-ttu-id="a9df7-120">Representación de búferes de vértices y de índices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9df7-120">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
