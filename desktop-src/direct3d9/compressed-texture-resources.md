---
description: Los mapas de textura son imágenes digitalizados dibujadas en formas tridimensionales para agregar detalles visuales.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Recursos de textura comprimida (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd4e21dfd0e042f8d8d97fd8415529a2b4a5a952334df3e7f39ef8ae20a890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989285"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Recursos de textura comprimida (Direct3D 9)

Los mapas de textura son imágenes digitalizados dibujadas en formas tridimensionales para agregar detalles visuales. Se asignan a estas formas durante la rasterización y el proceso puede consumir grandes cantidades de memoria y bus del sistema. Para reducir la cantidad de memoria que consumen las texturas, Direct3D admite la compresión de superficies de textura. Algunos dispositivos Direct3D admiten superficies de textura comprimidas de forma nativa. En estos dispositivos, cuando haya creado una superficie comprimida y cargado los datos en ella, la superficie se puede usar en Direct3D como cualquier otra superficie de textura. Direct3D controla la descompresión cuando la textura se asigna a un objeto 3D.

## <a name="storage-efficiency-and-texture-compression"></a>Storage Eficiencia y compresión de textura

Todos los formatos de compresión de textura son potencias de dos. Aunque esto no significa que una textura sea necesariamente cuadrada, significa que x e y son potencias de dos. Por ejemplo, si una textura es originalmente 512 por 128 bytes, la siguiente aplicación mipm sería 256 por 64, y así sucesivamente, con cada nivel disminuyendo en una potencia de dos. En niveles inferiores, donde la textura se filtra a 16 por 2 y 8 por 1, habrá bits desperdiciados porque el bloque de compresión siempre es un bloque de 4 por 4 de elementos de textura. Se agregan partes no usadas del bloque. Aunque hay bits desperdiciados en los niveles más bajos, la ganancia general sigue siendo significativa. El peor caso es, en teoría, una textura de 2K por 1 (2 ó 1 potencia). En este caso, solo se codifica una sola fila de píxeles por bloque, mientras que el resto del bloque no se usa.

## <a name="mixing-formats-within-a-single-texture"></a>Mezclar formatos dentro de una sola textura

Es importante tener en cuenta que cualquier textura única debe especificar que sus datos se almacenan como 64 o 128 bits por grupo de 16 texturas. Si se usan bloques de 64 bits (es decir, el formato DXT1) para la textura, es posible mezclar los formatos alfa opacos y de 1 bit por bloque dentro de la misma textura. En otras palabras, la comparación de la magnitud de entero sin signo del color 0 y el color 1 se realiza de forma única para cada bloque de \_ \_ 16 elementos de textura.

Una vez que se usan los bloques de 128 bits, el canal alfa debe especificarse en modo explícito (formato DXT2 y DXT3) o interpolado (formato DXT4 y DXT5) para toda la textura. Al igual que con el color, cuando se selecciona el modo interpolado (formato DXT4 y DXT5), se pueden usar ocho alfas interpolados o seis alfas interpolados en bloque. Una vez más, la comparación de magnitud de alfa 0 y alfa 1 se realiza de forma única en bloque \_ \_ por bloque.

Direct3D proporciona servicios para comprimir superficies que se usan para texturizar modelos 3D. En esta sección se proporciona información sobre cómo crear y manipular los datos en una superficie de textura comprimida.

La información se incluye en los temas siguientes.

-   [Texturas opacas y alfa de 1 bit (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturas con canales alfa (Direct3D 9)](textures-with-alpha-channels.md)
-   [Formatos de textura comprimidos (Direct3D 9)](compressed-texture-formats.md)
-   [Usar texturas comprimidas (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



