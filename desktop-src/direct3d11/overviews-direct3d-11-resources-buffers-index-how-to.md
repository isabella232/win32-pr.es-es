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
# <a name="how-to-create-an-index-buffer"></a>Cómo: crear un búfer de índice

Los [búferes de índice](overviews-direct3d-11-resources-buffers-intro.md) contienen datos de índice. En este tema se muestra cómo inicializar un [búfer de índice](overviews-direct3d-11-resources-buffers-intro.md) como preparación para la representación.

**Para inicializar un búfer de índice**

1.  Cree un búfer que contenga la información del índice.
2.  Cree una descripción de búfer rellenando una estructura [**\_ \_ DESC de búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Pase la marca de búfer de D3D11 \_ BIND \_ index \_ al miembro **BindFlags** y pase el tamaño del búfer en bytes al miembro **ByteWidth** .
3.  Cree una descripción de los datos de subrecurso rellenando una estructura de [**\_ \_ datos de subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . El miembro **pSysMem** debe apuntar directamente a los datos de índice creados en el paso uno.
4.  Llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mientras pasa la estructura de [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la interfaz [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se va a inicializar.

En el ejemplo de código siguiente se muestra cómo crear un búfer de índice. En este ejemplo se da por supuesto que


```
g_pd3dDevice
```



es un objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido y que


```
g_pd3dContext
```



es un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




