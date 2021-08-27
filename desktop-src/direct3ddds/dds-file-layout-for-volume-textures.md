---
title: Ejemplo de textura de volumen de DDS
description: Para una textura de volumen, use DDSCAPS \_ COMPLEX, DDSCAPS2 \_ VOLUME, DDSD \_ DEPTH, flags and set y dwDepth. Una textura de volumen es una extensión de una textura estándar para Direct3D 9; una textura de volumen se puede definir con o sin mapas mip.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79501ea3ffa6f4a660f4ab3b248fedbdc7df17bf8af94520cad5808c3c611fd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025745"
---
# <a name="dds-volume-texture-example"></a>Ejemplo de textura de volumen de DDS

Para una textura de volumen, use DDSCAPS \_ COMPLEX, DDSCAPS2 \_ VOLUME, DDSD \_ DEPTH, flags and set y dwDepth. Una textura de volumen es una extensión de una textura estándar para Direct3D 9; una textura de volumen se puede definir con o sin mapas mip.

Para los volúmenes sin mapas mip, cada segmento de profundidad se escribe en el archivo en orden. Si se incluyen mapas mip, todos los segmentos de profundidad para un nivel de mapa mip determinado se escriben juntos, con cada nivel que contiene la mitad de los segmentos que el nivel anterior con un mínimo de 1.

Por ejemplo, un mapa de volumen de 64 por 64 por 4 con un formato de píxel de R8G8B8 (3 bytes por píxel) con todos los niveles de mapa mipmap contendrá lo siguiente:



| Componentes de DDS                      | \# Bytes    |
|-------------------------------------|-------------|
| encabezado                              | 128 bytes   |
| 64 por 64 segmento 1 de 4 imagen principal.   | 12288 bytes |
| 64 por 64 segmento 2 de 4 imagen principal.   | 12288 bytes |
| 64 por 64 segmento 3 de 4 imagen principal.   | 12288 bytes |
| 64 por 64 segmento 4 de 4 imagen principal.   | 12288 bytes |
| Imagen de 32 por 32 segmento 1 de 2 mipmap. | 3072 bytes  |
| Imagen de 32 por 32 segmento 2 de 2 mipmap. | 3072 bytes  |
| 16 por 16 segmento 1 de una imagen de asignación mip. | 768 bytes   |
| 8 por 8 segmento 1 de una imagen de mapa mip.   | 192 bytes   |
| 4 por 4 segmento 1 de una imagen de mapa mip.   | 48 bytes    |
| 2 por 2 segmento 1 de una imagen de mapa mip.   | 12 bytes    |
| 1 por 1 segmento 1 de una imagen de mapa mip.   | 3 bytes     |



 

Tenga en cuenta que el nivel de mapa mip más pequeño es de solo 3 bytes porque el número de bits es 24 y no hay ninguna compresión agregada en este nivel.

Se agregó compatibilidad con texturas de volumen en DirectX 8.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




