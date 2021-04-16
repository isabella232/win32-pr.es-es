---
description: Eventos MSWebDVD
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: Eventos MSWebDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f363f15c35cbfe61a3ab1ff3703a31307785481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686280"
---
# <a name="mswebdvd-events"></a>Eventos MSWebDVD

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

> [!Note]  
> Esta API está en desuso. Para obtener información acerca de la reproducción de DVD y la navegación en DirectShow, consulte [aplicaciones de DVD](dvd-applications.md).

 

El control MSWebDVD de Microsoft® ActiveX® notifica a la aplicación cuando se producen varios tipos de eventos internos o cuando se encuentra determinada información en el disco.

La mayoría de los eventos se relacionan con los controles de operación de usuario (UOP). Los autores de DVD pueden codificar el disco para que cualquier comando de DVD (como **PlayForwards**, **PAUSE**, **showmenu**, etc.) se pueda deshabilitar en cualquier momento. Por ejemplo, la mayoría de los discos no permitirán a los usuarios avanzar rápidamente o mostrar un menú mientras se reproduce la advertencia del FBI. Una vez finalizada la advertencia, el disco permite estas operaciones. Mediante el control de los eventos de UOP, la aplicación puede actualizar su interfaz de usuario para mostrar al usuario qué comandos están permitidos actualmente en el disco. La manera más común de hacerlo es deshabilitar un botón. Por ejemplo, si la aplicación recibe un evento PlayForwards con **bEnabled** establecido en **false**, puede deshabilitar el botón reproducir. Cuando reciba ese evento con **bEnabled** establecido en **true**, podría volver a habilitar el botón.

Hay tres eventos que no se relacionan con los controles UOP. El evento **DVDNotify** notifica a la aplicación de muchos tipos diferentes de eventos relacionados con DVD, que se identifican en el parámetro *EventCode* . Algunos eventos tienen información adicional en los parámetros *parám1* y *Param2* . El evento **ReadyStateChange** notifica a la aplicación de los cambios en la propiedad MSWebDVD ReadyState, que es una propiedad común a todos los controles ActiveX. El evento **UpdateOverlay** se envía a las aplicaciones solo si hospedan MSWebDVD en modo sin ventanas. Las aplicaciones deben responder a este evento solo si muestran botones flotantes sobre el rectángulo del vídeo en el modo de pantalla completa.



| Evento                                                                  | Descripción                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | Se envía cuando el disco habilita o deshabilita el cambio de ángulo.                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | Se envía cuando el disco habilita o deshabilita el cambio de la secuencia de audio.                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | Se envía cuando se ha habilitado o deshabilitado el comando **ChangeCurrentSubpictureStream** . |
| [**DVDNotify**](dvdnotify.md)                                         | Notifica a una aplicación de muchos eventos de DVD y instrucciones de disco diferentes.           |
| [**Pausar**](pauseon.md)                                             | Se envía cuando se ha habilitado o deshabilitado el comando **pausar** .                         |
| [**PlayAtTime**](playattime.md)                                       | Se envía cuando se ha habilitado o deshabilitado el comando **PlayAtTime** .                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | Se envía cuando se ha habilitado o deshabilitado el comando **PlayAtTimeInTitle** .             |
| [**PlayBackwards**](playbackwards.md)                                 | Se envía cuando se ha habilitado o deshabilitado el comando **PlayBackwards** .                 |
| [**PlayChapter**](playchapter.md)                                     | Se envía cuando se ha habilitado o deshabilitado el comando **PlayChapter** .                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | Se envía cuando se ha habilitado o deshabilitado el comando **PlayChapterInTitle** .            |
| [**PlayForwards**](playforwards.md)                                   | Se envía cuando se ha habilitado o deshabilitado el comando **PlayForwards** .                  |
| [**PlayNextChapter**](playnextchapter.md)                             | Se envía cuando se ha habilitado o deshabilitado el comando **PlayNextChapter** .               |
| [**PlayPrevChapter**](playprevchapter.md)                             | Se envía cuando se ha habilitado o deshabilitado el comando **PlayPrevChapter** .               |
| [**PlayTitle**](playtitle.md)                                         | Se envía cuando se ha habilitado o deshabilitado el comando **PlayTitle** .                     |
| [**ReadyStateChange**](readystatechange.md)                           | Se envía cuando cambia la propiedad **ReadyState** del control MSWebDVD.            |
| [**ReplayChapter**](replaychapter.md)                                 | Se envía cuando se ha habilitado o deshabilitado el comando **ReplayChapter** .                 |
| [**Reanudar**](resume.md)                                               | Se envía cuando se ha habilitado o deshabilitado el comando de **reanudación** .                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | Se envía cuando se ha habilitado o deshabilitado el comando **ReturnFromSubmenu** .             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | Se envía cuando el disco habilita o deshabilita la selección o activación de los botones de menú.   |
| [**ShowMenu**](showmenu.md)                                           | Se envía cuando el disco habilita o deshabilita el modo en que se muestra un menú.                         |
| [**StillOff**](stilloff.md)                                           | Se envía cuando se ha habilitado o deshabilitado el comando **StillOff** .                      |
| [**Stop**](stop.md)                                                   | Se envía cuando se ha habilitado o deshabilitado el comando de **detención** .                          |
| [**UpdateOverlay**](updateoverlay.md)                                 | Se envía cuando se mueve o se cambia el tamaño de la superficie superpuesta o su clave de color ha cambiado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



