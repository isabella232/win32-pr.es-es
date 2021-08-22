---
title: Determinar y cambiar la posición actual
description: Determinar y cambiar la posición actual
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- Macro MCIWndGetStart
- Macro MCIWndGetEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594aa63b4b620327cd8b9ae41c263c197e1a981405c2148545ae7b8d4df86c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497345"
---
# <a name="determining-and-changing-the-current-position"></a>Determinar y cambiar la posición actual

Cuando un archivo o dispositivo está asociado a una ventana de MCIWnd, la posición de reproducción se establece inicialmente al principio del contenido, independientemente del tipo de medio. Durante la reproducción, la posición de reproducción se mueve linealmente a través del contenido y, si la reproducción no se interrumpe, llega al final del contenido. Si se produce una interrupción, la posición de reproducción actual es la ubicación en la que se detuvo o se detuvo la reproducción.

Puede recuperar las ubicaciones del principio y el final del contenido mediante las macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) y [**MCIWndGetEnd.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) Puede determinar la longitud del contenido restando el valor devuelto por **MCIWndGetStart** del valor devuelto por **MCIWndGetEnd** o mediante la macro [**MCIWndGetLength.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) Puede recuperar la posición de reproducción actual mediante la macro [**MCIWndGetPosition,**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) o puede recuperar la posición de reproducción como una cadena terminada en NULL mediante la macro [**MCIWndGetPositionString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)

Para cambiar la posición de reproducción actual, use las macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)y [**MCIWndSeek.**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) Puede mover la posición de reproducción al principio del contenido mediante **MCIWndHome** o al final del contenido mediante **MCIWndEnd**. Use **MCIWndSeek para** mover la posición de reproducción a cualquier ubicación del contenido.

También puede seguir paso a paso el contenido mediante la macro [**MCIWndStep.**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) A partir de la posición de reproducción actual, esta macro mueve la posición de reproducción hacia delante o hacia atrás en un incremento especificado.

> [!Note]  
> Las unidades usadas para especificar la posición varían entre los distintos tipos de medios y dispositivos. Por ejemplo, la posición de reproducción de los archivos AVI usados por el dispositivo MCIAVI se mide en fotogramas. la posición de reproducción de los archivos AUDIO CD, audio de forma de onda y MIDI se mide en milisegundos.

 

Los dispositivos para otros tipos de medios y dispositivos de terceros pueden usar otras unidades. Para obtener información sobre cómo determinar estas unidades, vea [Mejoras de reproducción.](playback-enhancements.md)

 

 




