---
title: Ejemplo de textura de volumen DDS
description: En el caso de una textura de volumen, utilice DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, DDSD \_ Depth, flags y set y dwDepth. Una textura de volumen es una extensión de una textura estándar para Direct3D 9; una textura de volumen se puede definir con o sin mapas MIP.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714183"
---
# <a name="dds-volume-texture-example"></a>Ejemplo de textura de volumen DDS

En el caso de una textura de volumen, utilice DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, DDSD \_ Depth, flags y set y dwDepth. Una textura de volumen es una extensión de una textura estándar para Direct3D 9; una textura de volumen se puede definir con o sin mapas MIP.

En el caso de los volúmenes sin mipmaps, cada segmento de profundidad se escribe en el archivo en orden. Si se incluyen los mapas MIP, todos los segmentos de profundidad de un nivel de mipmap determinado se escriben juntos, con cada nivel que contiene la mitad de los segmentos que el nivel anterior con un mínimo de 1.

Por ejemplo, un mapa de volumen 64 por 64 por 4 con un formato de píxel de R8G8B8 (3 bytes por píxel) con todos los niveles de mipmap contendrá lo siguiente:



| Componentes DDS                      | \# Bytes    |
|-------------------------------------|-------------|
| header                              | 128 bytes   |
| 64-por-64 segmento 1 de 4 imagen principal.   | 12288 bytes |
| 64-por-64 segmento 2 de 4 imagen principal.   | 12288 bytes |
| 64-por-64 segmento 3 de 4 imagen principal.   | 12288 bytes |
| 64-por-64 segmento 4 de 4 imagen principal.   | 12288 bytes |
| 32-por-32 segmento 1 de 2 imagen de mipmap. | 3072 bytes  |
| 32-por-32 segmento 2 de 2 imágenes de mipmap. | 3072 bytes  |
| segmento 1 de 16 por 16 de 1 imagen de mipmap. | 768 bytes   |
| 8 por 8 segmento 1 de 1 imagen de mipmap.   | 192 bytes   |
| 4 por 4 segmento 1 de 1 imagen de mipmap.   | 48 bytes    |
| 2-por 2 segmento 1 de 1 imagen de mipmap.   | 12 bytes    |
| 1 por 1 segmento 1 de 1 imagen de mipmap.   | 3 bytes     |



 

Tenga en cuenta que el nivel de mipmap más pequeño es solo 3 bytes porque el valor de bitCount es 24 y no hay ninguna compresión agregada en este nivel.

Se ha agregado compatibilidad con las texturas de volumen en DirectX 8.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




