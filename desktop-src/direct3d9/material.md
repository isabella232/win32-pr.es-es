---
description: Define un color de material básico que se puede aplicar a una malla completa o a las caras individuales de una malla. La potencia es el exponente especular del material.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494279"
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

-   color faceColor. Una plantilla ColorRGBA. Vea [**ColorRGBA**](colorrgba.md).
-   exponente de color especular de material de energía.
-   specularColor: color especular de material. Una plantilla ColorRGB. Vea [**ColorRGB**](colorrgb.md).
-   emissiveColor: material emisor color. Una plantilla ColorRGB. Vea [**ColorRGB**](colorrgb.md).

> [!Note]  
> El color ambiente requiere un componente alfa.

 

[**TextureFilename**](texturefilename.md) es un objeto de datos opcional. Si este objeto no está presente, la superficie no tiene textura.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



