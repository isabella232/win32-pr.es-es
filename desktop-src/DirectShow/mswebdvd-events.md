---
description: Eventos MSWebDVD
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: Eventos MSWebDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f363f15c35cbfe61a3ab1ff3703a31307785481
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254360"
---
# <a name="mswebdvd-events"></a>Eventos MSWebDVD

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

> [!Note]  
> Esta API está en desuso. Para obtener información sobre la reproducción de DVD y la navegación en DirectShow, vea [Aplicaciones de DVD](dvd-applications.md).

 

El control MSWebDVD Microsoft® ActiveX® notifica a la aplicación cuándo se producen varios tipos de eventos internos o cuando se encuentra cierta información en el disco.

La mayoría de los eventos están relacionados con los controles de operación de usuario (UOP). Los autores de DVD pueden codificar el disco para que cualquier comando de DVD (como **PlayForwards**, **Pause**, **ShowMenu,** entre otros) se pueda deshabilitar en cualquier momento. Por ejemplo, la mayoría de los discos no permitirán a los usuarios avanzar o mostrar un menú mientras se reproduce la advertencia de FAVOR. Una vez que se ha terminado la advertencia, el disco permite estas operaciones. Al controlar los eventos UOP, la aplicación puede actualizar su interfaz de usuario para mostrar al usuario qué comandos permite actualmente el disco. La manera más común de hacerlo es deshabilitar un botón. Por ejemplo, si la aplicación recibió un evento PlayForwards con **bEnabled** establecido en **FALSE,** podría deshabilitar el botón Reproducir. Cuando recibió ese evento con **bEnabled** establecido en **TRUE,** podría volver a habilitar el botón.

Hay tres eventos que no están relacionados con los controles UOP. El **evento DVDNotify** notifica a la aplicación muchos tipos diferentes de eventos relacionados con DVD, que se identifican en el *parámetro EventCode.* Algunos eventos tienen información adicional en los *parámetros Param1* *y Param2.* El **evento ReadyStateChange** notifica a la aplicación los cambios en la propiedad MSWebDVD ReadyState, que es una propiedad común a todos los ActiveX controles. El **evento UpdateOverlay** se envía a las aplicaciones solo si hospedan MSWebDVD en modo sin ventanas. Las aplicaciones solo deben responder a este evento si muestran botones flotantes sobre el rectángulo de vídeo en modo de pantalla completa.



| Evento                                                                  | Descripción                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | Se envía cuando el disco habilita o deshabilita el cambio del ángulo.                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | Se envía cuando el disco habilita o deshabilita el cambio de la secuencia de audio.                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | Se envía cuando **el comando ChangeCurrentSubpictureStream** se ha habilitado o deshabilitado. |
| [**DVDNotify**](dvdnotify.md)                                         | Notifica a una aplicación muchos eventos de DVD e instrucciones de disco diferentes.           |
| [**PauseOn**](pauseon.md)                                             | Se envía cuando **el comando Pausa** se ha habilitado o deshabilitado.                         |
| [**PlayAtTime**](playattime.md)                                       | Se envía cuando **el comando PlayAtTime** se ha habilitado o deshabilitado.                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | Se envía cuando **el comando PlayAtTimeInTitle** se ha habilitado o deshabilitado.             |
| [**PlayBackwards**](playbackwards.md)                                 | Se envía cuando **el comando PlayBackwards** se ha habilitado o deshabilitado.                 |
| [**PlayChapter**](playchapter.md)                                     | Se envía cuando **el comando PlayChapter** se ha habilitado o deshabilitado.                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | Se envía cuando **el comando PlayChapterInTitle** se ha habilitado o deshabilitado.            |
| [**PlayForwards**](playforwards.md)                                   | Se envía cuando **el comando PlayForwards** se ha habilitado o deshabilitado.                  |
| [**PlayNextChapter**](playnextchapter.md)                             | Se envía cuando **el comando PlayNextChapter** se ha habilitado o deshabilitado.               |
| [**PlayPrevChapter**](playprevchapter.md)                             | Se envía cuando **el comando PlayPrevChapter** se ha habilitado o deshabilitado.               |
| [**PlayTitle**](playtitle.md)                                         | Se envía cuando el **comando PlayTitle** se ha habilitado o deshabilitado.                     |
| [**ReadyStateChange**](readystatechange.md)                           | Se envía cuando **la propiedad ReadyState** del control MSWebDVD ha cambiado.            |
| [**ReplayChapter**](replaychapter.md)                                 | Se envía cuando **el comando ReplayChapter** se ha habilitado o deshabilitado.                 |
| [**Reanudar**](resume.md)                                               | Se envía cuando **el comando Reanudar** se ha habilitado o deshabilitado.                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | Se envía cuando **el comando ReturnFromSubmenu** se ha habilitado o deshabilitado.             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | Se envía cuando el disco habilita o deshabilita la selección o activación de botones de menú.   |
| [**ShowMenu**](showmenu.md)                                           | Se envía cuando el disco habilita o deshabilita la presentación de un menú.                         |
| [**StillOff**](stilloff.md)                                           | Se envía cuando el **comando StillOff** se ha habilitado o deshabilitado.                      |
| [**Stop**](stop.md)                                                   | Se envía cuando **el comando Stop** se ha habilitado o deshabilitado.                          |
| [**UpdateOverlay**](updateoverlay.md)                                 | Se envía cuando se ha movido o cambiado el tamaño de la superficie de superposición o se ha cambiado su clave de color. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



