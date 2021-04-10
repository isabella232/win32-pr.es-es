---
description: Los mapas de textura son imágenes digitalizadas dibujadas en formas tridimensionales para agregar detalles visuales.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Recursos de textura comprimidos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b7ef048c0e1780f92246a407863a4fa48a94a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275062"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Recursos de textura comprimidos (Direct3D 9)

Los mapas de textura son imágenes digitalizadas dibujadas en formas tridimensionales para agregar detalles visuales. Se asignan a estas formas durante la rasterización y el proceso puede consumir grandes cantidades de memoria y bus del sistema. Para reducir la cantidad de memoria consumida por las texturas, Direct3D admite la compresión de las superficies de textura. Algunos dispositivos Direct3D admiten superficies de textura comprimidas de forma nativa. En estos dispositivos, cuando se crea una superficie comprimida y se cargan los datos en ella, la superficie se puede usar en Direct3D como cualquier otra superficie de textura. Direct3D controla la descompresión cuando la textura se asigna a un objeto 3D.

## <a name="storage-efficiency-and-texture-compression"></a>Eficiencia del almacenamiento y compresión de textura

Todos los formatos de compresión de textura son potencias de dos. Aunque esto no significa que una textura sea necesariamente cuadrada, significa que x e y son potencias de dos. Por ejemplo, si una textura es originalmente 512 por 128 bytes, el siguiente mipmapping sería 256 por 64 y así sucesivamente, con cada nivel disminuido por una potencia de dos. En los niveles inferiores, donde la textura se filtra a 16 por 2 y 8 en 1, habrá bits desperdiciados porque el bloque de compresión siempre es un bloque de 4 por 4 de textura. Las partes no utilizadas del bloque se rellenan. Aunque hay bits desperdiciados en los niveles más bajos, la ganancia general sigue siendo significativa. El peor de los casos es, en teoría, una de 2 a 1 textura (2 ⁰ de potencia). Aquí, solo una fila de píxeles se codifica por bloque, mientras que el resto del bloque no se usa.

## <a name="mixing-formats-within-a-single-texture"></a>Combinación de formatos en una sola textura

Es importante tener en cuenta que cualquier textura única debe especificar que sus datos se almacenan como 64 o 128 bits por grupo de 16 textura. Si los bloques de 64 bits, es decir, el formato DXT1, se usan para la textura, es posible mezclar los formatos alfa opacos y de 1 bit en cada bloque dentro de la misma textura. En otras palabras, la comparación de la magnitud de entero sin signo de color \_ 0 y el color \_ 1 se realiza de forma única para cada bloque de 16 textura.

Una vez que se usan los bloques de 128 bits, el canal alfa debe especificarse en modo EXPLICIT (Format DXT2 y DXT3) o Interpolated (Format DXT4 y DXT5) para toda la textura. Al igual que con el color, cuando se selecciona el modo interpolado (formato DXT4 y DXT5), se pueden usar ocho alfa interpolados o seis modos alfa interpolados bloque a bloque. De nuevo, la comparación de la magnitud de alfa \_ 0 y alfa \_ 1 se realiza de forma exclusiva en bloque por bloque.

Direct3D proporciona servicios para comprimir superficies que se usan para aplicar texturas a modelos 3D. En esta sección se proporciona información sobre cómo crear y manipular los datos en una superficie de textura comprimida.

En los temas siguientes se incluye información.

-   [Texturas alfa opacas y de 1 bit (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturas con canales alfa (Direct3D 9)](textures-with-alpha-channels.md)
-   [Formatos de textura comprimidos (Direct3D 9)](compressed-texture-formats.md)
-   [Usar texturas comprimidas (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



