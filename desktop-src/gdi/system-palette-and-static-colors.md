---
description: Normalmente, las entradas de la paleta del sistema que el sistema reserva para los colores estáticos no se pueden cambiar.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: Paleta del sistema y colores estáticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537bdc87fecdd055334b83a56b0a53f9999be94c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985371"
---
# <a name="system-palette-and-static-colors"></a>Paleta del sistema y colores estáticos

Normalmente, las entradas de la paleta del sistema que el sistema reserva para los colores estáticos no se pueden cambiar. Una aplicación puede invalidar este comportamiento predeterminado mediante el uso de la función [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) para reducir el número de entradas de color estáticas y, por lo tanto, aumentar el número de entradas de la paleta del sistema no utilizadas. Sin embargo, dado que cambiar los colores estáticos puede tener un efecto inmediato y drástico en todas las ventanas de la pantalla, una aplicación no debe llamar a **SetSystemPaletteUse**, a menos que tenga una ventana maximizada y el foco de entrada.

Cuando una aplicación llama a [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con el \_ valor nostatic de SYSPAL, el sistema libera todas las entradas reservadas excepto las dos, lo que permite que dichas entradas reciban nuevos valores de color cuando la aplicación se dé de la paleta lógica. Las dos entradas de color estáticas restantes permanecen reservadas y se establecen en blanco y negro. Una aplicación puede restaurar las entradas reservadas llamando a **SetSystemPaletteUse** con el \_ valor estático SYSPAL. Puede detectar el uso actual de la paleta del sistema mediante la función [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse) .

Además, después de establecer el uso de la paleta del sistema en SYSPAL \_ nostatic, la aplicación debe darse de inmediato a su paleta lógica, llamar a la función [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) para guardar la configuración actual del color del sistema, llamar a la función [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) para establecer los colores del sistema en valores razonables usando blanco y negro y, por último, enviar el mensaje de [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) a otras ventanas de nivel superior para permitir Al establecer los colores del sistema mediante blanco y negro, la aplicación debe asegurarse de que los elementos adyacentes o superpuestos, como los bordes y los marcos de ventana, se establecen en blanco y negro, respectivamente.

Antes de que la aplicación pierda el foco de entrada, cierre su ventana o finalice, debe llamar inmediatamente a [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con el \_ valor estático SYSPAL, obtener la paleta lógica, restaurar los colores del sistema a sus valores anteriores y enviar el mensaje de [**\_ SYSCOLORCHANGE de WM**](wm-syscolorchange.md) . El sistema envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) a cualquier ventana afectada por un cambio de color del sistema. Las aplicaciones que tienen pinceles que usan los colores del sistema existentes deben eliminar esos pinceles y volver a crearlos con los nuevos colores del sistema.

 

 
