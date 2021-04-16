---
title: Ejemplo de textura DDS
description: En el caso de una textura sin comprimir, use las marcas DDSD de \_ tono y DDPF \_ RGB; para una textura comprimida, use las \_ marcas DDSD LINEARSIZE y DDPF \_ FourCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714184"
---
# <a name="dds-texture-example"></a>Ejemplo de textura DDS

En el caso de una textura sin comprimir, use las marcas DDSD de \_ tono y DDPF \_ RGB; para una textura comprimida, use las \_ marcas DDSD LINEARSIZE y DDPF \_ FourCC. En el caso de una textura mipmapped, use las \_ marcas complejas DDSD MIPMAPCOUNT, DDSCAPS \_ y DDSCAPS también, así como \_ el miembro de número de MIPMAP. Si se generan los mapas MIP, normalmente se escriben todos los niveles por debajo de 1 por 1.

En el caso de una textura comprimida, el tamaño de cada imagen de nivel de mipmap es normalmente un cuarto del tamaño de la anterior, con un mínimo de 8 (DXT1) o 16 (DXT2-5) bytes (para las texturas cuadradas). Use la fórmula siguiente para calcular el tamaño de cada nivel para una textura no cuadrada:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



En esta tabla se muestra la cantidad de espacio que ocupa cada capa para una textura R8G8B8 de 256 por 256, sin usar la compresión.



| Componentes DDS          | \# Bytes |
|-------------------------|----------|
| header                  | 128      |
| imagen principal de 256-por-256   | 196608   |
| imagen de mipmap 128 por 128 | 49152    |
| imagen de mipmap 64 por 64   | 12288    |
| imagen de mipmap 32 por 32   | 3072     |
| imagen de mipmap de 16 por 16   | 768      |
| imagen de mipmap de 8 por 8     | 192      |
| imagen de mipmap de 4 por 4     | 48       |
| imagen de mipmap 2 por 2     | 12       |
| imagen de mipmap 1 por 1     | 3        |



 

En esta tabla se muestra la cantidad de espacio que ocupa cada capa de la misma textura mediante compresión (DXT1).



| Componentes DDS         | \# Bytes |
|------------------------|----------|
| header                 | 128      |
| imagen principal de 256-por-64   | 8192     |
| imagen de mipmap 128 por 32 | 2048     |
| imagen de mipmap 64 por 16  | 512      |
| imagen de mipmap 32 por 8   | 128      |
| imagen de mipmap de 16 por 4   | 32       |
| imagen de mipmap de 8 por 2    | 16       |
| imagen de mipmap de 4 por 1    | 8        |
| imagen de mipmap 2 por 1    | 8        |
| imagen de mipmap 1 por 1    | 8        |



 

En esta tabla se muestra la cantidad de espacio que ocupa cada capa de la misma textura con un formato de compresión de DXGI (en este caso BC3 \_ UNORM) que, por lo tanto, requiere el encabezado extendido:



| Componentes DDS                                                | \# Bytes |
|---------------------------------------------------------------|----------|
| header (FourCC establecido en "contenido DX10")                                 | 128      |
| encabezado extendido (formato de DXGI establecido en \_ formato de dxgi \_ BC3 \_ UNORM) | 20       |
| imagen principal de 256-por-64                                          | 16384    |
| imagen de mipmap 128 por 32                                        | 4096     |
| imagen de mipmap 64 por 16                                         | 1024     |
| imagen de mipmap 32 por 8                                          | 256      |
| imagen de mipmap de 16 por 4                                          | 64       |
| imagen de mipmap de 8 por 2                                           | 32       |
| imagen de mipmap de 4 por 1                                           | 16       |
| imagen de mipmap 2 por 1                                           | 16       |
| imagen de mipmap 1 por 1                                           | 16       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




