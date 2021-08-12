---
title: Ejemplo de textura de DDS
description: Para una textura sin comprimir, use las marcas RGB DDSD PITCH y DDPF; para una textura comprimida, use las marcas \_ \_ DDSD LINEARSIZE y \_ DDPF \_ FOURCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47fe1d7da71727c2c84bb3745772a10520367ac1cf6e9c4033932548d86c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289802"
---
# <a name="dds-texture-example"></a>Ejemplo de textura de DDS

Para una textura sin comprimir, use las marcas RGB DDSD PITCH y DDPF; para una textura comprimida, use las marcas \_ \_ DDSD LINEARSIZE y \_ DDPF \_ FOURCC. Para una textura mipmapped, use las marcas \_ MIPMAPCOUNT, DDSCAPS MIPMAP y DDSCAPS COMPLEX de DDSCAPS, así como el miembro \_ \_ mipmap count. Si se generan mapas MIP, normalmente se escriben todos los niveles hasta 1 por 1.

Para una textura comprimida, el tamaño de cada imagen de nivel de mapa mip suele ser una cuarta parte del tamaño del anterior, con un mínimo de 8 (DXT1) o 16 (DXT2-5) bytes (para texturas cuadradas). Use la fórmula siguiente para calcular el tamaño de cada nivel para una textura no cuadrada:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



En esta tabla se muestra la cantidad de espacio que toma cada capa para una textura R8G8B8 de 256 por 256, sin usar compresión.



| Componentes de DDS          | \# Bytes |
|-------------------------|----------|
| encabezado                  | 128      |
| Imagen principal de 256 por 256   | 196608   |
| Imagen mipmap de 128 por 128 | 49152    |
| Imagen de mapa mipmap de 64 por 64   | 12288    |
| Imagen de mapa mipmap de 32 por 32   | 3072     |
| Imagen de mapa mipmap de 16 por 16   | 768      |
| Imagen de mapa mipmap de 8 por 8     | 192      |
| Imagen de mapa mipmap de 4 por 4     | 48       |
| Imagen de mapa mipmap de 2 por 2     | 12       |
| Imagen de mapa mipmap de 1 por 1     | 3        |



 

En esta tabla se muestra la cantidad de espacio ocupado por cada capa para la misma textura mediante compresión (DXT1).



| Componentes de DDS         | \# Bytes |
|------------------------|----------|
| encabezado                 | 128      |
| Imagen principal 256 por 64   | 8192     |
| Imagen de mapa mipmap de 128 por 32 | 2048     |
| Imagen mipmap de 64 por 16  | 512      |
| Imagen de mapa mipmap de 32 por 8   | 128      |
| Imagen de mapa mipmap de 16 por 4   | 32       |
| Imagen de mapa mipmap de 8 por 2    | 16       |
| Imagen de mapa mipmap de 4 por 1    | 8        |
| Imagen de mapa mipmap de 2 por 1    | 8        |
| Imagen de mapa mipmap de 1 por 1    | 8        |



 

En esta tabla se muestra la cantidad de espacio ocupado por cada capa para la misma textura mediante un formato de compresión DXGI (en este caso BC3 UNORM) que, por tanto, requiere el \_ encabezado extendido:



| Componentes de DDS                                                | \# Bytes |
|---------------------------------------------------------------|----------|
| header (FourCC establecido en "DX10")                                 | 128      |
| encabezado extendido (formato DXGI establecido en DXGI \_ FORMAT \_ BC3 \_ UNORM) | 20       |
| Imagen principal 256 por 64                                          | 16384    |
| Imagen de mapa mipmap de 128 por 32                                        | 4096     |
| Imagen mipmap de 64 por 16                                         | 1024     |
| Imagen de mapa mipmap de 32 por 8                                          | 256      |
| Imagen de mapa mipmap de 16 por 4                                          | 64       |
| Imagen de mapa mipmap de 8 por 2                                           | 32       |
| Imagen de mapa mipmap de 4 por 1                                           | 16       |
| Imagen de mapa mipmap de 2 por 1                                           | 16       |
| Imagen de mapa mipmap de 1 por 1                                           | 16       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




