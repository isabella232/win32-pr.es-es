---
title: Parámetros de accesibilidad
description: El sistema mantiene un conjunto de parámetros de accesibilidad que indican si el usuario tiene necesidades o preferencias especiales que requieren que las aplicaciones cambien su comportamiento predeterminado.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f089b28d36ffa982ca6568996126a812263af9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705001"
---
# <a name="accessibility-parameters"></a>Parámetros de accesibilidad

El sistema mantiene un conjunto de parámetros de accesibilidad que indican si el usuario tiene necesidades o preferencias especiales que requieren que las aplicaciones cambien su comportamiento predeterminado. El usuario controla el estado de estos parámetros, normalmente mediante el centro de accesibilidad en el panel de control. Las aplicaciones del panel de control u otros programas que permiten al usuario personalizar el entorno pueden utilizar la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para establecer los parámetros de accesibilidad.

Si un usuario cambia estos parámetros, el panel de control envía el mensaje de [**\_ SETTINGCHANGE de WM**](/windows/desktop/winmsg/wm-settingchange) . Las aplicaciones deben responder a este mensaje y usar [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para determinar el estado de los parámetros de accesibilidad. Cuando un parámetro de accesibilidad está habilitado, la aplicación debe modificar su interfaz de usuario, si es necesario, para acomodar las preferencias del usuario.

Windows admite los siguientes parámetros de accesibilidad.



| Parámetro                                                                    | Descripción                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [High contrast](high-contrast-parameter.md)                                 | Indica que las aplicaciones deben proporcionar un contraste alto entre los objetos visuales de primer plano y de fondo.                                                                            |
| [Preferencias de teclado](keyboard-preference-parameter.md)                     | Indica que las aplicaciones deben mostrar interfaces de teclado que, de lo contrario, se ocultarían.                                                                                 |
| [Lector de pantalla](screen-reader-parameter.md)                                 | Indica que las aplicaciones deben proporcionar información de texto en situaciones en las que, de lo contrario, presentaría la información de forma gráfica.                                     |
| [Mostrar sonidos (y marca de descripción de audio)](showsounds-parameter.md) | Indica que las aplicaciones también deben proporcionar una alerta visual o una indicación al usar un sonido para transmitir información importante, o proporcionar una descripción de audio para los elementos visuales. |
| [Animación del área de cliente](client-area-animation.md)                           | Indica que las aplicaciones deben respetar las preferencias del usuario para mostrar la animación en el área cliente.                                                                       |
| [Duración del mensaje](message-duration.md)                                     | Indica que las aplicaciones que proporcionan notificaciones emergentes deben supervisar marcas sobre la duración del mensaje y ajustar su longitud de notificación.                                  |



 

Los siguientes parámetros del sistema son útiles para las aplicaciones de accesibilidad. Para obtener más información, vea [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) (función).



| Grupo de parámetros      | Parámetro                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parámetros de escritorio   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Parámetros de entrada     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, SPI \_ GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ GETMOUSE, SPI \_ GETMOUSEHOVERHEIGHT, SPI \_ GETMOUSEHOVERTIME, SPI \_ GETMOUSEHOVERWIDTH, SPI \_ GETMOUSESPEED, SPI \_ GETMOUSETRAILS, SPI \_ GETSNAPTODEFBUTTON, SPI \_ GETWHEELSCROLLLINES, SPI \_ SETDOUBLECLICKTIME, SPI SETDOUBLECLKHEIGHT, \_ SPI \_ SETDOUBLECLKWIDTH, SPI \_ SETKEYBOARDCUES, SPI \_ SETKEYBOARDDELAY, SPI SETKEYBOARDPREF \_ , SPI \_ SETKEYBOARDSPEED, SPI \_ SETMOUSE, SPI \_ SETMOUSEHOVERHEIGHT, SPI SETMOUSEHOVERTIME, \_ SPI \_ SETMOUSEHOVERWIDTH, SPI SETMOUSESPEED, SPI SETMOUSETRAILS, SPI \_ \_ \_ SETSNAPTODEFBUTTON, SPI \_ SETWHEELSCROLLLINES |
| Parámetros de efectos de la interfaz de usuario | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Parámetros de ventana    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRAGHEIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT, SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las características de accesibilidad de Windows](about-windows-accessibility-features.md)
</dt> </dl>

 

 