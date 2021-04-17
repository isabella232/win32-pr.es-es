---
description: En este tema se describe cómo buscar durante la reproducción mediante MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Cómo buscar durante la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687120"
---
# <a name="how-to-seek-during-playback"></a>Cómo buscar durante la reproducción

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo buscar durante la reproducción mediante MFPlay.

**Para buscar durante la reproducción**

1.  Inicialice un **PROPVARIANT** para que contenga el tiempo de búsqueda en unidades de 100-nanosegundos, como un tipo **\_ entero grande** (**VT \_ i8**).
2.  Llame a [**IMFPMediaPlayer:: SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition). Especifique **MFP \_ POSITIONTYPE de \_ 100 NS** para el primer parámetro y pase el **PROPVARIANT** para el segundo parámetro.

## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



