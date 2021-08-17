---
title: Parámetros de accesibilidad
description: El sistema mantiene un conjunto de parámetros de accesibilidad que indican si el usuario tiene necesidades o preferencias especiales que requieren que las aplicaciones cambien su comportamiento predeterminado.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a289162366f5d69c501ffbea55108167324c11a1c865184105afd587f36bcfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327793"
---
# <a name="accessibility-parameters"></a>Parámetros de accesibilidad

El sistema mantiene un conjunto de parámetros de accesibilidad que indican si el usuario tiene necesidades o preferencias especiales que requieren que las aplicaciones cambien su comportamiento predeterminado. El usuario controla el estado de estos parámetros, normalmente mediante el Centro de accesibilidad en Panel de control. Panel de control aplicaciones u otros programas que permiten al usuario personalizar el entorno pueden usar la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para establecer los parámetros de accesibilidad.

Si un usuario cambia estos parámetros, el Panel de control envía el [**mensaje \_ WM SETTINGCHANGE.**](/windows/desktop/winmsg/wm-settingchange) Las aplicaciones deben responder a este mensaje y usar [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para determinar el estado de los parámetros de accesibilidad. Cuando se habilita un parámetro de accesibilidad, la aplicación debe modificar su interfaz de usuario, si es necesario, para adaptarse a las preferencias del usuario.

Windows admite los siguientes parámetros de accesibilidad.



| Parámetro                                                                    | Descripción                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [High contrast](high-contrast-parameter.md)                                 | Indica que las aplicaciones deben proporcionar un contraste alto entre los objetos visuales de primer plano y de fondo.                                                                            |
| [Preferencia de teclado](keyboard-preference-parameter.md)                     | Indica que las aplicaciones deben mostrar interfaces de teclado que, de lo contrario, se ocultarían.                                                                                 |
| [Lector de pantalla](screen-reader-parameter.md)                                 | Indica que las aplicaciones deben proporcionar información textual en situaciones en las que, de lo contrario, presentaría la información gráficamente.                                     |
| [Mostrar sonidos (y marca de descripción de audio)](showsounds-parameter.md) | Indica que las aplicaciones también deben proporcionar una alerta visual o una indicación cuando usa sonido para transmitir información importante, o bien proporcionar una descripción de audio para los elementos visuales. |
| [Animación de área de cliente](client-area-animation.md)                           | Indica que las aplicaciones deben respetar las preferencias del usuario para mostrar la animación en el área cliente.                                                                       |
| [Duración del mensaje](message-duration.md)                                     | Indica que las aplicaciones que proporcionan notificaciones emergentes deben supervisar las marcas sobre la duración del mensaje y ajustar su longitud de notificación.                                  |



 

Los siguientes parámetros del sistema son útiles para las aplicaciones de accesibilidad. Para obtener más información, [**vea Función SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)



| Grupo de parámetros      | Parámetro                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parámetros de escritorio   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Parámetros de entrada     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, SPI \_ GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ GETMOUSE, SPI \_ GETMOUSEHOVERHEIGHT, \_ SPI GETMOUSEHOVERTIME, SPI \_ GETMOUSEHOVERWIDTH, SPI \_ GETMOUSESPEED, SPI \_ GETMOUSETRAILS, SPI \_ GETSNAPTODEFBUTTON, SPI \_ GETWHEELSCROLLLINES, SPI \_ SETDOUBLECLICKTIME, SPI \_ SETDOUBLECLKHEIGHT, SPI \_ SETDOUBLECLREVIDTH, SPI \_ SETKEYBOARDCUES, SPI \_ SETKEYBOARDDELAY, SPI \_ SETKEYBOARDPREF, SPI \_ SETKEYBOARDSPEED, \_ SPI \_ SETMOUSE, SPI SETMOUSEHOVERHEIGHT, SPI \_ SETMOUSEHOVERTIME, SPI \_ SETMOUSEHOVERWIDTH, SPI \_ SETMOUSESPEED, SPI \_ SETMOUSETRAILS, SPI \_ SETSNAPTODEFBUTTON, SPI \_ SETWHEELSCROLLLINES |
| Parámetros de efecto de la interfaz de usuario | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Parámetros de ventana    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRAMWIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT, SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows de accesibilidad](about-windows-accessibility-features.md)
</dt> </dl>

 

 