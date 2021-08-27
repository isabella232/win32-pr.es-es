---
title: Cómo crear un búfer de índice
description: En este tema se muestra cómo inicializar un búfer de índice como preparación para la representación.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- búfer de índice, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d474114e5908a42a112dddd550e24c13e5e1d3bf2cec523d47dfe1d617ac0bf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119505"
---
# <a name="how-to-create-an-index-buffer"></a>Cómo: Crear un búfer de índice

[Los búferes de índice](overviews-direct3d-11-resources-buffers-intro.md) contienen datos de índice. En este tema se muestra cómo inicializar un búfer [de índice](overviews-direct3d-11-resources-buffers-intro.md) como preparación para la representación.

**Para inicializar un búfer de índice**

1.  Cree un búfer que contenga la información del índice.
2.  Cree una descripción del búfer rellenando una [**estructura \_ \_ DESC de BÚFER D3D11.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Pase la marca BIND INDEX BUFFER de D3D11 al miembro BindFlags y pase el tamaño del búfer en bytes al \_ \_ miembro \_ **ByteWidth.** 
3.  Cree una descripción de datos de subrecursos rellenando una estructura [**\_ SUBRESOURCE \_ DATA de D3D11.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) El **miembro pSysMem** debe apuntar directamente a los datos de índice creados en el paso uno.
4.  Llame a [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) al pasar la estructura [**D3D11 \_ BUFFER \_ DESC,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) la estructura [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la [**interfaz ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se inicializará.

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

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




