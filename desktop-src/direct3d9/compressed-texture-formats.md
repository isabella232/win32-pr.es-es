---
description: Esta sección contiene información sobre la organización interna de formatos de textura comprimidos.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formatos de textura comprimidos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807748"
---
# <a name="compressed-texture-formats-direct3d-9"></a>Formatos de textura comprimidos (Direct3D 9)

Esta sección contiene información sobre la organización interna de formatos de textura comprimidos. No necesita estos detalles para usar texturas comprimidas, ya que puede usar las funciones de D3DX para la conversión a y desde formatos comprimidos. Sin embargo, esta información resulta útil si desea trabajar directamente con datos de superficie comprimidos.

Direct3D usa un formato de compresión que divide los mapas de textura en bloques textura 4x4. Si la textura no contiene transparencia (es opaca) o si la transparencia se especifica mediante un alfa de 1 bit, un bloque de 8 bytes representa el bloque de mapa de textura. Si el mapa de textura contiene textura transparentes, mediante un canal alfa, un bloque de 16 bytes lo representa.

-   [Texturas alfa opacas y de 1 bit (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturas con canales alfa (Direct3D 9)](textures-with-alpha-channels.md)

Cualquier textura única debe especificar que sus datos se almacenan como 64 o 128 bits por grupo de 16 textura. Si los bloques de 64 bits, es decir, el formato DXT1, se usan para la textura, es posible mezclar los formatos alfa opacos y de 1 bit en cada bloque dentro de la misma textura. En otras palabras, la comparación de la magnitud de entero sin signo de color \_ 0 y el color \_ 1 se realiza de forma única para cada bloque de 16 textura.

Cuando se usan bloques de 128 bits, el canal alfa debe especificarse en modo EXPLICIT (Format DXT2 o DXT3) o Interpolated (Format DXT4 o DXT5) para toda la textura. Al igual que con el color, cuando se selecciona el modo interpolado, se pueden usar ocho alfa interpolados o el modo alfa interpolado bloque a bloque. De nuevo, la comparación de la magnitud de alfa \_ 0 y alfa \_ 1 se realiza de forma exclusiva en bloque por bloque.

El paso de los formatos DXTn es diferente de lo que se devolvió en DirectX 7,0. El paso se mide ahora en bytes (no en bloques). Por ejemplo, si tiene un ancho de 16, tendrá un paso de cuatro bloques (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de textura comprimidos](compressed-texture-resources.md)
</dt> </dl>

 

 



