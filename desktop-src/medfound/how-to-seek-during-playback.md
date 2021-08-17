---
description: En este tema se describe cómo buscar durante la reproducción mediante MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Cómo buscar durante la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47e035ff8cc3764a9080698e8596660ce61907319bda70ac019b4cba1f8c27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974424"
---
# <a name="how-to-seek-during-playback"></a>Cómo buscar durante la reproducción

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo buscar durante la reproducción mediante MFPlay.

**Para buscar durante la reproducción**

1.  Inicialice **propVARIANT para** contener el tiempo de búsqueda en unidades de 100 nanosegundos, como un tipo **LARGE \_ INTEGER** **(VT \_ I8).**
2.  Llame [**a IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition). Especifique **MFP \_ POSITIONTYPE \_ 100NS** para el primer parámetro y pase **PROPVARIANT** para el segundo parámetro.

## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



