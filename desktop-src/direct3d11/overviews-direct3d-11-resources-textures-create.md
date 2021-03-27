---
title: Cómo crear una textura
description: En este tema se muestra cómo crear una textura.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d3c4715bb4c790ea772dcbba4834051946747e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777593"
---
# <a name="how-to-create-a-texture"></a>Cómo: crear una textura

La manera más sencilla de crear una textura es describir sus propiedades y llamar a la API de creación de texturas. En este tema se muestra cómo crear una textura.

**Para crear una textura**

1.  Rellene una [**estructura \_ \_ DESC de D3D11 TEXTURE2D**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) con una descripción de los parámetros de la textura.
2.  Cree la textura mediante una llamada a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) con la descripción de la textura.

En este ejemplo se crea una textura 256 x 256, con [**uso dinámico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), para su uso como un [**recurso de sombreador**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) con [**acceso de escritura de CPU**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




