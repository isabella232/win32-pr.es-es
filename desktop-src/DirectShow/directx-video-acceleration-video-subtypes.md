---
description: Los descodificadores que utilizan la aceleración de vídeo de DirectX (DXVA) usan los siguientes subtipos.
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Subtipos de vídeo de aceleración de vídeo de DirectX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680269"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Subtipos de vídeo de aceleración de vídeo de DirectX

Los descodificadores que utilizan la aceleración de vídeo de DirectX (DXVA) usan los siguientes subtipos. AI44 y IA44 son superficies con un valor de bits por píxel de 8. Hay 4 bits de I y 4 bits de *un*. *I* representa un índice en una paleta YUV de 16 entradas. *Representa 4* bits de información de transparencia (también conocido como alfa por píxel). Por lo tanto, las superficies AI44 y IA44 permiten 16 colores diferentes con 16 valores de transparencia distintos, o 256 representaciones de píxeles diferentes. Con AI44, el alfa se almacena en el HI-Nibble, en IA44, el alfa se almacena en el medio de recorte. Ambos formatos son muy útiles para imágenes de subimagen de DVD e imágenes de Line21 e teletexto. Microsoft prefiere la versión de AI44 porque es algo más fácil generar texto con este formato.

| Subtype            | Descripción                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | Para subimágenes y superposiciones de texto. Vea la descripción anterior. |
| MEDIASUBTYPE \_ IA44 | Para subimágenes y superposiciones de texto. Vea la descripción anterior. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> </dl>

 

 




