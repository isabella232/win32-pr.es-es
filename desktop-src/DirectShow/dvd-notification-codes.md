---
description: Códigos de notificación de eventos de DVD
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: Códigos de notificación de eventos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717c260c84a1038860ee04f46db6224025b7709c3ad039e7625a48ae6359cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686455"
---
# <a name="dvd-event-notification-codes"></a>Códigos de notificación de eventos de DVD

En esta sección se enumeran los códigos de notificación de eventos para la reproducción y navegación de DVD en DirectShow.

Para obtener información sobre cómo recibir eventos en DirectShow, vea [Notificación de eventos en DirectShow](event-notification-in-directshow.md).

Para otros códigos de evento que no son DVD, vea [Códigos de notificación de eventos](event-notification-codes.md).



| Código de notificación de eventos                                                        | Descripción                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAMBIO \_ DE ÁNGULO DE DVD DE \_ \_ EC**](ec-dvd-angle-change.md)                          | Indica que ha cambiado el número de ángulos disponibles o que ha cambiado el número de ángulo actual.                                                                      |
| [**ÁNGULOS \_ DE DVD DE EC \_ \_ DISPONIBLES**](ec-dvd-angles-available.md)                  | Indica si se reproduce un bloque angular y se pueden realizar cambios de ángulo.                                                                                      |
| [**CAMBIO \_ DE SECUENCIA DE AUDIO DE DVD DE \_ \_ \_ EC**](ec-dvd-audio-stream-change.md)           | Indica que el número de secuencia de audio actual ha cambiado para el título principal.                                                                                                  |
| [**DVD \_ de EC \_ BeginNavigationCommands**](ec-dvd-beginnavigationcommands.md)     | Se envía cuando se inicia un conjunto de comandos de navegación de DVD.                                                                                                                  |
| [**BOTÓN \_ DE DVD DE EC ACTIVADO \_ \_ \_ AUTOMÁTICAMENTE**](ec-dvd-button-auto-activated.md)       | Indica que un botón de menú se ha activado automáticamente según las instrucciones del disco.                                                                                 |
| [**CAMBIO \_ DEL BOTÓN DE DVD DE \_ \_ EC**](ec-dvd-button-change.md)                        | Indica que ha cambiado el número de botones disponibles o que ha cambiado el número de botón seleccionado actualmente.                                                         |
| [**EC \_ DVD \_ CHAPTER \_ AUTOSTOP**](ec-dvd-chapter-autostop.md)                  | Indica que la reproducción se detuvo como resultado de una llamada al método [**IDvdControl2::P layChaptersAutoStop.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop)                    |
| [**INICIO DEL \_ CAPÍTULO DE DVD DE \_ \_ EC**](ec-dvd-chapter-start.md)                        | Indica que el navegador de DVD inició la reproducción de un nuevo capítulo en el título actual.                                                                                    |
| [**EC \_ DVD \_ CMD \_ START**](ec-dvd-cmd-start.md)                                | Indica que ha comenzado un comando determinado.                                                                                                                              |
| [**EC \_ DVD \_ CMD \_ END**](ec-dvd-cmd-end.md)                                    | Indica que se ha completado un comando determinado.                                                                                                                          |
| [**EC \_ DVD \_ CURRENT \_ HMSF \_ TIME**](ec-dvd-current-hmsf-time.md)               | Señala la hora actual en formato [**\_ DVD HMSF \_ TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) al principio de cada unidad de objeto de vídeo (VOBU).                                   |
| [**HORA \_ ACTUAL DEL DVD DE \_ \_ EC**](ec-dvd-current-time.md)                          | Señala el principio de cada VOBU.                                                                                                                                      |
| [**DISCO \_ DE DVD EC \_ \_ EXPULSADA**](ec-dvd-disc-ejected.md)                          | Indica que se ha expulsado un disco de la unidad.                                                                                                                      |
| [**DISCO \_ DE DVD DE EC \_ \_ INSERTADO**](ec-dvd-disc-inserted.md)                        | Indica que se ha insertado un disco en la unidad.                                                                                                                     |
| [**CAMBIO \_ DE DOMINIO DE DVD DE \_ \_ EC**](ec-dvd-domain-change.md)                        | Indica el nuevo dominio del navegador de DVD.                                                                                                                                 |
| [**ERROR \_ DE DVD DE \_ EC**](ec-dvd-error.md)                                         | Señala una condición de error de DVD.                                                                                                                                            |
| [**Cambio \_ de GPRM de DVD \_ de \_ EC**](ec-dvd-gprm-change.md)                            | Se envía cuando cambia el valor de un registro de parámetros general (GPRM).                                                                                                       |
| [**MODO \_ DVD \_ DVD \_ EC**](ec-dvd-karaoke-mode.md)                          | Indica que el navegador ha empezado a reproducir o ha terminado de reproducir datos de la máquina.                                                                                   |
| [**EC \_ DVD \_ NavigationCommand**](ec-dvd-navigationcommand.md)                 | Se envía cuando [el navegador de DVD](dvd-navigator-filter.md) procesa un comando de navegación de DVD.                                                                               |
| [**EC \_ DVD \_ NO \_ FP \_ PGC**](ec-dvd-no-fp-pgc.md)                               | Indica que el disco de DVD no tiene una FP \_ PGC (Cadena de programa de primera reproducción).                                                                                           |
| [**CAMBIO \_ DE NIVEL PARENTAL DE DVD DE \_ \_ \_ EC**](ec-dvd-parental-level-change.md)       | Indica que el nivel parental del contenido escrito está a punto de cambiar.                                                                                               |
| [**CAMBIO DE \_ VELOCIDAD DE REPRODUCCIÓN DE DVD DE \_ \_ \_ EC**](ec-dvd-playback-rate-change.md)         | Indica que se ha iniciado un cambio de velocidad de reproducción y que la nueva velocidad está en el parámetro .                                                                            |
| [**REPRODUCCIÓN \_ DE DVD DE EC \_ \_ DETENIDA**](ec-dvd-playback-stopped.md)                  | Indica que se ha detenido la reproducción. El navegador de DVD ha completado la reproducción del título y no encontró ninguna otra instrucción de bifurcación para la reproducción posterior. |
| [**EC \_ DVD \_ PLAYPERIOD \_ AUTOSTOP**](ec-dvd-playperiod-autostop.md)            | Indica que el navegador ha terminado de reproducir el segmento especificado en una llamada a PlayPeriodInTitleAutoStop.                                                           |
| [**CAMBIO \_ DE CELDA DEL PROGRAMA DVD DE \_ \_ \_ EC**](ec-dvd-program-cell-change.md)           | Se envía cuando cambia el número de programa de DVD o el número de celda.                                                                                                                  |
| [**CAMBIO EN \_ LA CADENA DEL PROGRAMA DVD DE \_ \_ \_ EC**](ec-dvd-program-chain-change.md)         | Se envía cuando cambia la cadena de programas actual (PGC).                                                                                                                            |
| [**Cambio \_ de \_ SPRM de DVD de \_ EC**](ec-dvd-sprm-change.md)                            | Se envía cuando cambia el valor de un registro de parámetros del sistema (SPRM).                                                                                                        |
| [**DVD \_ DE EC TODAVÍA \_ \_ DESACTIVADO**](ec-dvd-still-off.md)                                | Señala el final de cualquier todavía.                                                                                                                                             |
| [**DVD \_ DE EC TODAVÍA EN \_ \_ ON**](ec-dvd-still-on.md)                                  | Señala el principio de cualquier todavía.                                                                                                                                       |
| [**EC DVD SUBPICTURE STREAM CHANGE (CAMBIO DE SECUENCIA \_ \_ DE \_ SUBASPECCIÓN DE DVD DE \_ EC)**](ec-dvd-subpicture-stream-change.md) | Indica que el número de secuencia de subpicture actual cambió para el título principal.                                                                                             |
| [**CAMBIO \_ DE CONJUNTO DE TÍTULO DE DVD DE \_ \_ \_ EC**](ec-dvd-title-set-change.md)                 | Se envía cuando cambia el conjunto de títulos de vídeo (VTS) actual.                                                                                                                          |
| [**CAMBIO \_ DE TÍTULO DEL DVD DE \_ \_ EC**](ec-dvd-title-change.md)                          | Indica cuándo cambia el número de título actual.                                                                                                                          |
| [**CAMBIO \_ DE \_ \_ UOPS VÁLIDO DE DVD DE \_ EC**](ec-dvd-valid-uops-change.md)               | Indica que el conjunto disponible de métodos de interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) ha cambiado.                                                                     |
| [**Desplazamiento \_ \_ VOBU de DVD de \_ EC**](ec-dvd-vobu-offset.md)                            | Se envía cuando [el navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.                                                                                              |
| [**Marca de \_ tiempo DE VOBU de DVD \_ de EC \_**](ec-dvd-vobu-timestamp.md)                      | Se envía cuando [el navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.                                                                                              |
| [**ADVERTENCIA \_ DE DVD DE \_ EC**](ec-dvd-warning.md)                                     | Señala una condición de advertencia de DVD.                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> </dl>

 

 



