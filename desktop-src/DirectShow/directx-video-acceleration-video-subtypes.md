---
description: Los descodificadores que usan la aceleración de vídeo de DirectX (DXVA) usan los subtipos siguientes.
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Subtipos de vídeo de aceleración de vídeo de DirectX (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a2197d504929e001e07fb1ac107dbd7b13b1f443e43ec8ed90232372b08f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016153"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Subtipos de vídeo de aceleración de vídeo de DirectX

Los descodificadores que usan la aceleración de vídeo de DirectX (DXVA) usan los subtipos siguientes. AI44 e IA44 son superficies con un valor de bits por píxel de 8. Hay 4 bits de I y 4 bits de *A*. *Represento* un índice en una paleta YUV de 16 entradas. *representa* 4 bits de información de transparencia (también conocido como por píxel-alfa). Por lo tanto, las superficies AI44 e IA44 permiten 16 colores diferentes en 16 valores de transparencia diferentes o 256 representaciones de píxeles diferentes. Con AI44, el alfa se almacena en hi-nibble, en IA44, el alfa se almacena en lo-nibble. Ambos formatos son muy útiles para las imágenes de subpágenes de DVD y las imágenes de texto teletexto y Line21. Microsoft prefiere la versión AI44 porque es ligeramente más fácil generar texto con este formato.

| Subtype            | Descripción                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | Para subimagen y superposiciones de texto. Consulte la descripción anterior. |
| MEDIASUBTYPE \_ IA44 | Para subimagen y superposiciones de texto. Consulte la descripción anterior. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> </dl>

 

 




