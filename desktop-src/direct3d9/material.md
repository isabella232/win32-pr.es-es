---
description: Define un color de material básico que se puede aplicar a una malla completa o a las caras individuales de una malla. La potencia es el exponente especular del material.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d4dcb1cef7597ff7c02d16f1db311287511166c9259c89a0ea60a0c49fb7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798972"
---
# <a name="material"></a>Material

Define un color de material básico que se puede aplicar a una malla completa o a las caras individuales de una malla. La potencia es el exponente especular del material.

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

Donde:

-   faceColor: color de cara. Una plantilla ColorRGBA. Vea [**ColorRGBA**](colorrgba.md).
-   power: exponente de color especular de material.
-   specularColor: color especular del material. Una plantilla ColorRGB. Consulte [**ColorRGB**](colorrgb.md).
-   emissiveColor: color de material emissive. Una plantilla ColorRGB. Consulte [**ColorRGB**](colorrgb.md).

> [!Note]  
> El color ambiente requiere un componente alfa.

 

[**TextureFilename es**](texturefilename.md) un objeto de datos opcional. Si este objeto no está presente, la cara no tiene texto.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



