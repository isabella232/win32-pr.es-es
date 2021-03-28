---
title: Cómo crear un búfer de índice
description: En este tema se muestra cómo inicializar un búfer de índice como preparación para la representación.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- búfer de índice, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269093"
---
# <a name="how-to-create-an-index-buffer"></a><span data-ttu-id="c0531-104">Cómo: crear un búfer de índice</span><span class="sxs-lookup"><span data-stu-id="c0531-104">How to: Create an Index Buffer</span></span>

<span data-ttu-id="c0531-105">Los [búferes de índice](overviews-direct3d-11-resources-buffers-intro.md) contienen datos de índice.</span><span class="sxs-lookup"><span data-stu-id="c0531-105">[Index buffers](overviews-direct3d-11-resources-buffers-intro.md) contain index data.</span></span> <span data-ttu-id="c0531-106">En este tema se muestra cómo inicializar un [búfer de índice](overviews-direct3d-11-resources-buffers-intro.md) como preparación para la representación.</span><span class="sxs-lookup"><span data-stu-id="c0531-106">This topic shows how to initialize an [index buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="c0531-107">**Para inicializar un búfer de índice**</span><span class="sxs-lookup"><span data-stu-id="c0531-107">**To initialize an index buffer**</span></span>

1.  <span data-ttu-id="c0531-108">Cree un búfer que contenga la información del índice.</span><span class="sxs-lookup"><span data-stu-id="c0531-108">Create a buffer that contains your index information.</span></span>
2.  <span data-ttu-id="c0531-109">Cree una descripción de búfer rellenando una estructura [**\_ \_ DESC de búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="c0531-109">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="c0531-110">Pase la marca de búfer de D3D11 \_ BIND \_ index \_ al miembro **BindFlags** y pase el tamaño del búfer en bytes al miembro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="c0531-110">Pass the D3D11\_BIND\_INDEX\_BUFFER flag to the **BindFlags** member and pass the size of the buffer in bytes to the **ByteWidth** member.</span></span>
3.  <span data-ttu-id="c0531-111">Cree una descripción de los datos de subrecurso rellenando una estructura de [**\_ \_ datos de subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="c0531-111">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="c0531-112">El miembro **pSysMem** debe apuntar directamente a los datos de índice creados en el paso uno.</span><span class="sxs-lookup"><span data-stu-id="c0531-112">The **pSysMem** member should point directly to the index data created in step one.</span></span>
4.  <span data-ttu-id="c0531-113">Llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mientras pasa la estructura de [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la interfaz [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="c0531-113">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="c0531-114">En el ejemplo de código siguiente se muestra cómo crear un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="c0531-114">The following code example demonstrates how to create an index buffer.</span></span> <span data-ttu-id="c0531-115">En este ejemplo se da por supuesto que</span><span class="sxs-lookup"><span data-stu-id="c0531-115">This example assumes that</span></span>


```
g_pd3dDevice
```



<span data-ttu-id="c0531-116">es un objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido y que</span><span class="sxs-lookup"><span data-stu-id="c0531-116">is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that</span></span>


```
g_pd3dContext
```



<span data-ttu-id="c0531-117">es un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.</span><span class="sxs-lookup"><span data-stu-id="c0531-117">is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a><span data-ttu-id="c0531-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0531-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0531-119">Búferes</span><span class="sxs-lookup"><span data-stu-id="c0531-119">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="c0531-120">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c0531-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




