---
title: Usar las paletas MCIWnd
description: Usar las paletas MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette (macro)
- MCIWndSetPalette (macro)
- MCIWndRealize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995223"
---
# <a name="using-mciwnd-palettes"></a>Usar las paletas MCIWnd

La reproducción de clips de vídeo con una profundidad de color de 8 bits (256: capacidad de color) requiere una paleta para definir los colores que se usan. A veces, la paleta incluida con un clip de vídeo no es la más adecuada para su uso durante la reproducción. En este caso, MCIWnd proporciona tres maneras de administrar las paletas para la reproducción:

-   Recupera un identificador de la paleta asociada a una ventana de MCIWnd mediante la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) . La paleta no se asocia necesariamente exclusivamente con la ventana de MCIWnd. Otras aplicaciones pueden tener acceso al identificador de la paleta e incluso invalidarlo. Por consiguiente, la aplicación debe prever el uso global de la paleta y, cuando termine con la paleta, no debe liberarla.
-   Especifique una nueva paleta para usarla con el clip de vídeo asociado a una ventana de MCIWnd mediante la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .
-   Observe la paleta asociada a una ventana de MCIWnd de la paleta del sistema mediante la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) . Esta macro llama a la función [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) con la paleta asociada a la ventana MCIWnd. Si los controladores de mensajes de la aplicación para [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) solo llaman a **RealizePalette** o **MCIWndRealize**, debe reenviar estos mensajes a MCIWnd si no los administra usted mismo.

> [!Note]  
> Cuando se carga un clip de vídeo con una profundidad de color de 8 bits en la ventana de MCIWnd, la paleta incluida con ese clip reemplaza la paleta asociada a la ventana de MCIWnd.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras en la reproducción](playback-enhancements.md)
</dt> </dl>

 

 