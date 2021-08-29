---
title: Tipo de textura
description: Use la sintaxis siguiente para declarar una variable de textura.
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
ms.openlocfilehash: 78e508c72faf61a1a1167fda4fbfba621f4c5255021b6196b8b30a6b86c13fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846005"
---
# <a name="texture-type"></a>Tipo de textura

Use la sintaxis siguiente para declarar una variable de textura.

|                |
|----------------|
| **Nombre de tipo;** |

## <a name="parameters"></a>Parámetros
| Elemento                                                                                     | Descripción                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**<br/> | Uno de los siguientes tipos: textura (sin tipo, por compatibilidad con versiones anteriores), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube. El tamaño del elemento debe caber en 4 cantidades de 32 bits.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/> | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                                                                                                                                                   |
## <a name="remarks"></a>Comentarios

Hay tres partes para usar una textura.

1.  Declarar una variable de textura. Esto se hace con la sintaxis mostrada anteriormente. Por ejemplo, se trata de declaraciones válidas.

    ```
    texture g_MeshTexture;
    ```

    \- O bien

    ```
    Texture2D g_MeshTexture;
    ```

2.  Declarar e inicializar un objeto sampler. Esto se hace con una sintaxis ligeramente diferente en Direct3D 9 y Direct3D 10. Para obtener más información sobre la sintaxis del objeto [sampler, vea Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).
3.  Invocar una función de textura en un sombreador.

Diferencias entre Direct3D 9 y Direct3D 10:

Direct3D 9 usa funciones [de textura intrínsecas](dx-graphics-hlsl-intrinsic-functions.md) para realizar operaciones de textura. Este ejemplo es del [ejemplo BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) y usa [texas2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) para realizar el muestreo de textura.

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

Direct3D 10 usa objetos [de textura con plantilla](dx-graphics-hlsl-to-type.md) en su lugar. Este es un ejemplo de la operación de textura equivalente.

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>Vea también

[Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
