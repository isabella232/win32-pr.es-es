---
title: Objetos del modelo de sombreador 5,1
description: Se han agregado los siguientes objetos al modelo de sombreador 5,1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616afd8e4036988b6f91cb09cddf0db26c1dd480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359120"
---
# <a name="shader-model-51-objects"></a>Objetos del modelo de sombreador 5,1

Se han agregado los siguientes objetos al modelo de sombreador 5,1.

En el caso de las [vistas de orden de rasterizador](/windows/desktop/direct3d11/rasterizer-order-views) (disponibles en D3D 11.3 y D3D12), los objetos siguientes son nuevos y solo se permiten en el sombreador de píxeles. Tenga en cuenta que los métodos que admiten son idénticos a los objetos UAV correspondientes.



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| Objeto de rasterizador                  | Objeto UAV                                                    |
| RasterizerOrderedBuffer            | [**RWBuffer**](sm5-object-rwbuffer.md)                       |
| RasterizerOrderedByteAddressBuffer | [**RWByteAddressBuffer**](sm5-object-rwbyteaddressbuffer.md) |
| RasterizerOrderedStructuredBuffer  | [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md)   |
| RasterizerOrderedTexture1D         | [**RWTexture1D**](sm5-object-rwtexture1d.md)                 |
| RasterizerOrderedTexture1DArray    | [**RWTexture1DArray**](sm5-object-rwtexture1darray.md)       |
| RasterizerOrderedTexture2D         | [**RWTexture2D**](sm5-object-rwtexture2d.md)                 |
| RasterizerOrderedTexture2DArray    | [**RWTexture2DArray**](sm5-object-rwtexture2darray.md)       |
| RasterizerOrderedTexture3D         | [**RWTexture3D**](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5,1](shader-model-5-1.md)
</dt> <dt>

[Características del modelo de sombreador de HLSL 5,1 para Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 