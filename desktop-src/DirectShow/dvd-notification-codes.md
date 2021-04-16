---
description: Códigos de notificación de eventos de DVD
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: Códigos de notificación de eventos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15172e8eba3da048e7c7704a90d7992fa21714a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677132"
---
# <a name="dvd-event-notification-codes"></a>Códigos de notificación de eventos de DVD

En esta sección se enumeran los códigos de notificación de eventos para la reproducción de DVD y la navegación en DirectShow.

Para obtener información acerca de cómo recibir eventos en DirectShow, vea [notificación de eventos en DirectShow](event-notification-in-directshow.md).

Para otros códigos de eventos que no son de DVD, consulte [códigos de notificación de eventos](event-notification-codes.md).



| Código de notificación de eventos                                                        | Descripción                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_cambio de \_ ángulo de DVD de EC \_**](ec-dvd-angle-change.md)                          | Indica que se ha cambiado el número de ángulos disponibles o que ha cambiado el número de ángulo actual.                                                                      |
| [**ángulos de DVD de EC \_ \_ \_ disponibles**](ec-dvd-angles-available.md)                  | Indica si se está reproduciendo un bloque de ángulo y se pueden realizar cambios en el ángulo.                                                                                      |
| [**\_cambio de \_ flujo de audio de DVD de EC \_ \_**](ec-dvd-audio-stream-change.md)           | Indica que el número de secuencia de audio actual ha cambiado para el título principal.                                                                                                  |
| [**\_BeginNavigationCommands de DVD de EC \_**](ec-dvd-beginnavigationcommands.md)     | Se envía cuando se inicia un conjunto de comandos de navegación de DVD.                                                                                                                  |
| [**botón de DVD de EC \_ \_ \_ \_ activado automáticamente**](ec-dvd-button-auto-activated.md)       | Indica que se ha activado automáticamente un botón de menú por cada instrucción del disco.                                                                                 |
| [**\_cambio de \_ botón de DVD de EC \_**](ec-dvd-button-change.md)                        | Indica que ha cambiado el número de botones disponibles o que ha cambiado el número de botón seleccionado actualmente.                                                         |
| [**reparo de capítulos de DVD de EC \_ \_ \_**](ec-dvd-chapter-autostop.md)                  | Indica que la reproducción se detuvo como resultado de una llamada al método [**IDvdControl2::P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) .                    |
| [**\_Inicio de \_ capítulo de DVD de EC \_**](ec-dvd-chapter-start.md)                        | Indica que el navegador de DVD inició la reproducción de un nuevo capítulo en el título actual.                                                                                    |
| [**\_Inicio de \_ cmd de DVD de EC \_**](ec-dvd-cmd-start.md)                                | Indica que ha empezado un comando determinado.                                                                                                                              |
| [**\_fin de \_ cmd de DVD de EC \_**](ec-dvd-cmd-end.md)                                    | Indica que se ha completado un comando determinado.                                                                                                                          |
| [**\_hora de \_ \_ HMSF actual del DVD \_ de EC**](ec-dvd-current-hmsf-time.md)               | Indica la hora actual en el formato de [**\_ código de \_ tiempo HMSF de DVD**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) al principio de cada unidad de objeto de vídeo (VOBU).                                   |
| [**\_ \_ hora actual del DVD de EC \_**](ec-dvd-current-time.md)                          | Indica el principio de cada VOBU.                                                                                                                                      |
| [**\_disco DVD de EC \_ \_ expulsado**](ec-dvd-disc-ejected.md)                          | Indica que se ha expulsado un disco de la unidad.                                                                                                                      |
| [**\_disco DVD de EC \_ \_ insertado**](ec-dvd-disc-inserted.md)                        | Indica que se ha insertado un disco en la unidad.                                                                                                                     |
| [**\_cambio de \_ dominio de DVD de EC \_**](ec-dvd-domain-change.md)                        | Indica el nuevo dominio del explorador de DVD.                                                                                                                                 |
| [**\_error de DVD de EC \_**](ec-dvd-error.md)                                         | Indica una condición de error de DVD.                                                                                                                                            |
| [**\_Cambio de \_ GPRM de DVD de EC \_**](ec-dvd-gprm-change.md)                            | Se envía cuando cambia el valor de un registro de parámetros general (GPRM).                                                                                                       |
| [**\_modo de \_ Karaoke de DVD de EC \_**](ec-dvd-karaoke-mode.md)                          | Indica que el navegador ha empezado a reproducir o ha terminado de reproducir los datos de karaoke.                                                                                   |
| [**\_NavigationCommand de DVD de EC \_**](ec-dvd-navigationcommand.md)                 | Se envía cuando el [navegador de DVD](dvd-navigator-filter.md) procesa un comando de navegación por DVD.                                                                               |
| [**DVD de EC \_ \_ sin \_ FP \_**](ec-dvd-no-fp-pgc.md)                               | Indica que el disco DVD no tiene una cadena de \_ programa de reproducción de FP (primera).                                                                                           |
| [**\_cambio de \_ nivel parental de DVD de \_ EC \_**](ec-dvd-parental-level-change.md)       | Indica que el nivel parental del contenido creado está a punto de cambiar.                                                                                               |
| [**\_cambio de \_ velocidad de reproducción de DVD de EC \_ \_**](ec-dvd-playback-rate-change.md)         | Indica que se ha iniciado un cambio de velocidad de reproducción y que la nueva velocidad está en el parámetro.                                                                            |
| [**reproducción de DVD de EC \_ \_ \_ detenida**](ec-dvd-playback-stopped.md)                  | Indica que se ha detenido la reproducción. El navegador de DVD ha completado la reproducción del título y no ha encontrado ninguna otra instrucción de bifurcación para la posterior reproducción. |
| [**\_detención de \_ PLAYPERIOD de DVD de EC \_**](ec-dvd-playperiod-autostop.md)            | Indica que el navegador ha terminado de reproducirse el segmento especificado en una llamada a PlayPeriodInTitleAutoStop.                                                           |
| [**\_cambio de \_ celda del programa de DVD de EC \_ \_**](ec-dvd-program-cell-change.md)           | Se envía cuando cambia el número de programa o el número de celda del DVD.                                                                                                                  |
| [**\_cambio de \_ cadena de programa de DVD EC \_ \_**](ec-dvd-program-chain-change.md)         | Se envía cuando cambia la cadena de programas actual (PGC).                                                                                                                            |
| [**\_Cambio de \_ SPRM de DVD de EC \_**](ec-dvd-sprm-change.md)                            | Se envía cuando cambia el valor de un registro de parámetros del sistema (SPRM).                                                                                                        |
| [**DVD de EC \_ \_ sin \_ conexión**](ec-dvd-still-off.md)                                | Señala el final de cualquier todavía.                                                                                                                                             |
| [**\_DVD \_ de EC todavía \_ encendido**](ec-dvd-still-on.md)                                  | Indica el principio de cualquier todavía.                                                                                                                                       |
| [**\_cambio de \_ secuencia de subimagen de DVD de \_ EC \_**](ec-dvd-subpicture-stream-change.md) | Indica que el número de secuencia de la subimagen actual ha cambiado para el título principal.                                                                                             |
| [**\_cambio de \_ conjunto de títulos de DVD de EC \_ \_**](ec-dvd-title-set-change.md)                 | Se envía cuando cambia el conjunto de títulos de vídeo actual (VTS).                                                                                                                          |
| [**\_cambio de \_ título de DVD de EC \_**](ec-dvd-title-change.md)                          | Indica cuándo cambia el número de título actual.                                                                                                                          |
| [**\_cambio de \_ \_ UOPS válido de DVD \_ de EC**](ec-dvd-valid-uops-change.md)               | Indica que el conjunto disponible de métodos de interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) ha cambiado.                                                                     |
| [**\_Desplazamiento de \_ VOBU de DVD de EC \_**](ec-dvd-vobu-offset.md)                            | Se envía cuando el [navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.                                                                                              |
| [**Marca de tiempo VOBU de DVD de EC \_ \_ \_**](ec-dvd-vobu-timestamp.md)                      | Se envía cuando el [navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.                                                                                              |
| [**\_Advertencia de DVD de EC \_**](ec-dvd-warning.md)                                     | Indica una condición de advertencia de DVD.                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> </dl>

 

 



