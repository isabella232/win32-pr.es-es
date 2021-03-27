---
title: Tipo de textura
description: Use la siguiente sintaxis para declarar una variable de textura.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Tipo de textura HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "103789135"
---
# <a name="texture-type"></a>Tipo de textura

Use la siguiente sintaxis para declarar una variable de textura.

|                |
|----------------|
| **Nombre del tipo;** |

## <a name="parameters"></a>Parámetros
| Elemento                                                                                     | Descripción                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Automáticamente**<br/> | Uno de los siguientes tipos: Texture (sin tipo, para compatibilidad con versiones anteriores), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube. El tamaño del elemento debe ajustarse a las cantidades de 4 32 bits.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/> | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                                                                                                                                                   |
## <a name="remarks"></a>Observaciones

El uso de una textura consta de tres partes.

1.  Declarar una variable de textura. Esto se hace con la sintaxis mostrada anteriormente. Por ejemplo, se trata de declaraciones válidas.

    ```
    texture g_MeshTexture;
    ```

    \- o -

    ```
    Texture2D g_MeshTexture;
    ```

2.  Declarar e inicializar un objeto de muestra. Esto se hace con una sintaxis ligeramente diferente en Direct3D 9 y Direct3D 10. Para obtener más información sobre la sintaxis de objetos de muestra, vea [tipo de muestra (DirectX HLSL)](dx-graphics-hlsl-sampler.md).
3.  Invocar una función de textura en un sombreador.

Diferencias entre Direct3D 9 y Direct3D 10:

Direct3D 9 usa [funciones de textura intrínsecas](dx-graphics-hlsl-intrinsic-functions.md) para realizar operaciones de textura. Este ejemplo está en el [ejemplo BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) y usa [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) para realizar el muestreo de textura.

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

En su lugar, Direct3D 10 usa [objetos de textura con plantilla](dx-graphics-hlsl-to-type.md) . Este es un ejemplo de la operación de textura equivalente.

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>Vea también

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
