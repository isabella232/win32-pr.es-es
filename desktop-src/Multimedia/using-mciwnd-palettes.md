---
title: Uso de paletas MCIWnd
description: Uso de paletas MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- Macro MCIWndGetPalette
- Macro MCIWndSetPalette
- Macro MCIWndRealize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245787"
---
# <a name="using-mciwnd-palettes"></a>Uso de paletas MCIWnd

La reproducción de clips de vídeo con una profundidad de color de 8 bits (capacidad de 256 colores) requiere una paleta para definir los colores que se usan. A veces, la paleta incluida con un clip de vídeo no es la paleta más adecuada para usar durante la reproducción. En este caso, MCIWnd proporciona tres maneras de administrar las paletas para la reproducción:

-   Recupere un identificador de la paleta asociada a una ventana de MCIWnd mediante la macro [**MCIWndGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) La paleta no está necesariamente asociada exclusivamente a la ventana MCIWnd. Otras aplicaciones pueden acceder al identificador de la paleta e incluso invalidarlo. Por lo tanto, la aplicación debe prever el uso global de la paleta y, cuando termine con la paleta, no debe liberarla.
-   Especifique una nueva paleta que se usará con el clip de vídeo asociado a una ventana de MCIWnd mediante la macro [**MCIWndSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
-   Use la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) para obtener la paleta asociada a una ventana de MCIWnd a la paleta del sistema. Esta macro llama a [**la función RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) con la paleta asociada a la ventana MCIWnd. Si los controladores de mensajes de aplicación para [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) solo llaman a **RealizePalette** o **MCIWndRealize,** debe reenviar estos mensajes a MCIWnd si no los controla usted mismo.

> [!Note]  
> Cuando se carga un clip de vídeo con profundidad de color de 8 bits en la ventana MCIWnd, la paleta incluida con ese clip reemplaza la paleta asociada a la ventana MCIWnd.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras de reproducción](playback-enhancements.md)
</dt> </dl>

 

 