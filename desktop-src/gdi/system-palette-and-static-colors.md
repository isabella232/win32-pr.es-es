---
description: Normalmente, no se pueden cambiar las entradas de la paleta del sistema que el sistema reserva para los colores estáticos.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: Paleta del sistema y colores estáticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffc555331ea7ad14675b4155a76d14cc61f3bef3fa7e92b331ad89449b97884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613385"
---
# <a name="system-palette-and-static-colors"></a>Paleta del sistema y colores estáticos

Normalmente, no se pueden cambiar las entradas de la paleta del sistema que el sistema reserva para los colores estáticos. Una aplicación puede invalidar este comportamiento predeterminado mediante la función [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) para reducir el número de entradas de color estático y, por tanto, aumentar el número de entradas de la paleta del sistema no utilizadas. Sin embargo, dado que cambiar los colores estáticos puede tener un efecto inmediato y drástico en todas las ventanas de la pantalla, una aplicación no debe llamar a **SetSystemPaletteUse**, a menos que tenga una ventana maximizada y el foco de entrada.

Cuando una aplicación llama a [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con el valor SYSPAL NOSTATIC, el sistema libera todas las entradas reservadas, menos dos, lo que permite que esas entradas reciban nuevos valores de color cuando la aplicación se dé cuenta posteriormente de su paleta \_ lógica. Las dos entradas de color estático restantes permanecen reservadas y se establecen en blanco y negro. Una aplicación puede restaurar las entradas reservadas llamando a **SetSystemPaletteUse** con el valor \_ STATIC de SYSPAL. Puede detectar el uso actual de la paleta del sistema mediante la [**función GetSystemPaletteUse.**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse)

Además, después de establecer el uso de la paleta del sistema en SYSPAL NOSTATIC, la aplicación debe darse cuenta inmediatamente de su paleta lógica, llamar a la función GetSysColor para guardar la configuración de color del sistema actual, llamar a la función \_ [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) para establecer los colores del sistema en valores razonables mediante blanco y negro y, por último, enviar el mensaje [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) a otras ventanas de nivel superior para permitirles volver a dibujarlos con los nuevos colores del sistema. [](/windows/win32/api/winuser/nf-winuser-getsyscolor) Al establecer los colores del sistema con blanco y negro, la aplicación debe asegurarse de que los elementos adyacentes o superpuestos, como los marcos de ventana y los bordes, están establecidos en blanco y negro, respectivamente.

Antes de que la aplicación pierda el foco de entrada, cierre su ventana o finalice, debe llamar inmediatamente a [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con el valor STATIC de SYSPAL, realizar su paleta lógica, restaurar los colores del sistema a sus valores anteriores y enviar el mensaje \_ [**\_ SYSCOLORCHANGE de WM.**](wm-syscolorchange.md) El sistema envía un [**mensaje WM \_ PAINT**](wm-paint.md) a cualquier ventana afectada por un cambio de color del sistema. Las aplicaciones que tienen pinceles que usan los colores del sistema existentes deben eliminar esos pinceles y volver a crearlos con los nuevos colores del sistema.

 

 
