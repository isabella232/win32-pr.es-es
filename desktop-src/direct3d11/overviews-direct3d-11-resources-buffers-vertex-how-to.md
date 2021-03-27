---
title: Cómo crear un búfer de vértices
description: En este tema se muestra cómo inicializar un búfer de vértices estático, es decir, un búfer de vértice que no cambia.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- búfer de vértices, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357301"
---
# <a name="how-to-create-a-vertex-buffer"></a><span data-ttu-id="a6cef-104">Cómo: crear un búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="a6cef-104">How to: Create a Vertex Buffer</span></span>

<span data-ttu-id="a6cef-105">Los [búferes de vértices](overviews-direct3d-11-resources-buffers-intro.md) contienen datos por vértice.</span><span class="sxs-lookup"><span data-stu-id="a6cef-105">[Vertex buffers](overviews-direct3d-11-resources-buffers-intro.md) contain per vertex data.</span></span> <span data-ttu-id="a6cef-106">En este tema se muestra cómo inicializar un [búfer de vértices](overviews-direct3d-11-resources-buffers-intro.md)estático, es decir, un búfer de vértice que no cambia.</span><span class="sxs-lookup"><span data-stu-id="a6cef-106">This topic shows how to initialize a static [vertex buffer](overviews-direct3d-11-resources-buffers-intro.md), that is, a vertex buffer that does not change.</span></span> <span data-ttu-id="a6cef-107">Para obtener ayuda para inicializar un búfer no estático, consulte la sección [comentarios](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="a6cef-107">For help initializing a non-static buffer, see the [remarks](#remarks) section.</span></span>

<span data-ttu-id="a6cef-108">**Para inicializar un búfer de vértices estáticos**</span><span class="sxs-lookup"><span data-stu-id="a6cef-108">**To initialize a static vertex buffer**</span></span>

1.  <span data-ttu-id="a6cef-109">Defina una estructura que describa un vértice.</span><span class="sxs-lookup"><span data-stu-id="a6cef-109">Define a structure that describes a vertex.</span></span> <span data-ttu-id="a6cef-110">Por ejemplo, si los datos de vértice contienen datos de posición y datos de color, la estructura tendría un vector que describa la posición y otro que describa el color.</span><span class="sxs-lookup"><span data-stu-id="a6cef-110">For example, if your vertex data contains position data and color data, your structure would have one vector that describes the position and another that describes the color.</span></span>
2.  <span data-ttu-id="a6cef-111">Asigne memoria (mediante malloc o New) para la estructura que definió en el paso uno.</span><span class="sxs-lookup"><span data-stu-id="a6cef-111">Allocate memory (using malloc or new) for the structure that you defined in step one.</span></span> <span data-ttu-id="a6cef-112">Rellene este búfer con los datos de vértice reales que describen su geometría.</span><span class="sxs-lookup"><span data-stu-id="a6cef-112">Fill this buffer with the actual vertex data that describes your geometry.</span></span>
3.  <span data-ttu-id="a6cef-113">Cree una descripción de búfer rellenando una estructura [**\_ \_ DESC de búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="a6cef-113">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="a6cef-114">Pase la \_ marca de búfer de vértices BIND de D3D11 \_ \_ al miembro **BindFlags** y pase el tamaño de la estructura del paso uno al miembro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="a6cef-114">Pass the D3D11\_BIND\_VERTEX\_BUFFER flag to the **BindFlags** member and pass the size of the structure from step one to the **ByteWidth** member.</span></span>
4.  <span data-ttu-id="a6cef-115">Cree una descripción de los datos de subrecurso rellenando una estructura de [**\_ \_ datos de subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="a6cef-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="a6cef-116">El miembro **pSysMem** de la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) debe apuntar directamente a los datos de recursos creados en el paso dos.</span><span class="sxs-lookup"><span data-stu-id="a6cef-116">The **pSysMem** member of the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure should point directly to the resource data created in step two.</span></span>
5.  <span data-ttu-id="a6cef-117">Llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mientras pasa la estructura de [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la interfaz [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="a6cef-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="a6cef-118">En el ejemplo de código siguiente se muestra cómo crear un búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="a6cef-118">The following code example demonstrates how to create a vertex buffer.</span></span> <span data-ttu-id="a6cef-119">En este ejemplo se da por supuesto que **g \_ pd3dDevice** es un objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido.</span><span class="sxs-lookup"><span data-stu-id="a6cef-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object.</span></span>


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a><span data-ttu-id="a6cef-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6cef-120">Remarks</span></span>

<span data-ttu-id="a6cef-121">A continuación se indican algunas maneras de inicializar un búfer de vértice que cambia con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="a6cef-121">Here are some ways to initialize a vertex buffer that changes over time.</span></span>

1.  <span data-ttu-id="a6cef-122">Cree un segundo búfer con [**el \_ \_ almacenamiento provisional del uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); rellene el segundo búfer con [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)desasignar; use [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) para copiar desde el búfer de almacenamiento provisional al búfer predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6cef-122">Create a 2nd buffer with [**D3D11\_USAGE\_STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); fill the second buffer using [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) to copy from the staging buffer to the default buffer.</span></span>
2.  <span data-ttu-id="a6cef-123">Use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para copiar datos de la memoria.</span><span class="sxs-lookup"><span data-stu-id="a6cef-123">Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to copy data from memory.</span></span>
3.  <span data-ttu-id="a6cef-124">Cree un búfer con el uso de D3D11 dinámico y rellénelo con [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) desasignar (mediante las marcas discard y NoOverwrite de [**\_ \_ forma**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)adecuada).</span><span class="sxs-lookup"><span data-stu-id="a6cef-124">Create a buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), and fill it with [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (using the Discard and NoOverwrite flags appropriately).</span></span>

<span data-ttu-id="a6cef-125">\#1 y \# 2 son útiles para el contenido que cambia menos de una vez por fotograma.</span><span class="sxs-lookup"><span data-stu-id="a6cef-125">\#1 and \#2 are useful for content that changes less than once per frame.</span></span> <span data-ttu-id="a6cef-126">En general, las lecturas de GPU serán rápidas y las actualizaciones de CPU serán más lentas.</span><span class="sxs-lookup"><span data-stu-id="a6cef-126">In general, GPU reads will be fast and CPU updates will be slower.</span></span>

<span data-ttu-id="a6cef-127">\#3 es útil para el contenido que cambia más de una vez por fotograma.</span><span class="sxs-lookup"><span data-stu-id="a6cef-127">\#3 is useful for content that changes more than once per frame.</span></span> <span data-ttu-id="a6cef-128">En general, las lecturas de GPU serán más lentas, pero las actualizaciones de la CPU serán más rápidas.</span><span class="sxs-lookup"><span data-stu-id="a6cef-128">In general, GPU reads will be slower, but CPU updates will be faster.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6cef-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6cef-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6cef-130">Búferes</span><span class="sxs-lookup"><span data-stu-id="a6cef-130">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="a6cef-131">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a6cef-131">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




