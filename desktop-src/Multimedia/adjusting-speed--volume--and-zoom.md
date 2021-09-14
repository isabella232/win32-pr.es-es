---
title: Ajustar la velocidad, el volumen y el zoom
description: Ajustar la velocidad, el volumen y el zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- Macro MCIWndSetSpeed
- Macro MCIWndGetSpeed
- Macro MCIWndSetVolume
- Macro MCIWndGetVolume
- Macro MCIWndSetZoom
- Macro MCIWndGetZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063006"
---
# <a name="adjusting-speed-volume-and-zoom"></a>Ajustar la velocidad, el volumen y el zoom

Las macros de velocidad, volumen y zoom proporcionan la  funcionalidad de los comandos **Ver,** Volumen y Velocidad en el menú MCIWnd. Las macros descritas en esta sección se usan normalmente con vídeo y otros dispositivos que muestran imágenes durante la reproducción.

Algunos dispositivos admiten varios cambios de velocidad de reproducción. Puede establecer la velocidad de reproducción de estos dispositivos mediante la macro [**MCIWndSetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) Esta macro define la velocidad de reproducción como 1000. Los valores más altos indican velocidades más rápidas. Los valores más bajos indican velocidades más lentas.

Puede recuperar la velocidad de reproducción actual mediante la macro [**MCIWndGetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) Esta macro usa los mismos valores e intervalos que los usados por **MCIWndSetSpeed.**

Algunos dispositivos admiten cambios de volumen. Puede ajustar o establecer el volumen mediante la macro [**MCIWndSetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) Esta macro define el nivel de volumen normal como 1000. Los valores más altos indican volúmenes más altos. Los valores inferiores indican volúmenes más silenciosos.

Puede recuperar el nivel de volumen actual mediante la macro [**MCIWndGetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) Esta macro usa los mismos valores numéricos e intervalo que los usados por **MCIWndSetVolume.**

En el caso de los dispositivos que usan una ventana de reproducción, MCIWnd admite una característica de zoom que establece el tamaño de la imagen de reproducción. Puede establecer el tamaño de la imagen de reproducción mediante la macro [**MCIWndSetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) La macro redefine el tamaño de la imagen de reproducción mientras se mantiene una relación de aspecto constante para la imagen. El valor de zoom se define como un porcentaje del tamaño de la imagen original. Por lo tanto, 100 representa el tamaño de la imagen original, 50 indica que la imagen mostrada es la mitad de su tamaño original y 200 indica que la imagen mostrada tiene el doble de su tamaño original.

Puede recuperar el valor de zoom actual mediante la macro [**MCIWndGetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) Esta macro usa los mismos valores e intervalo que los usados por **MCIWndSetZoom.**

> [!Note]  
> Los controladores estándar de audio y audio de forma de onda de MCI CD no admiten cambios de volumen o velocidad.

 

 

 




