---
description: Comandos de DVD
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: Comandos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bf06127ab3829ed6cdcbbb70c3b2c1d1b41cf0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806506"
---
# <a name="dvd-commands"></a>Comandos de DVD

Los comandos de navegación y reproducción de DVD se definen en una sección de la especificación de DVD denominada Annex J, que es el motivo por el que la documentación de DirectShow a menudo hace referencia a "comandos J del anexo". Sin embargo, los nombres proporcionados en el Anexo J no siempre son muy intuitivos, por lo que DirectShow usa nombres que pueden ser más fáciles de entender.

En la tabla siguiente se enumeran los comandos del Anexo J y sus equivalentes de DirectShow.



| Anexo J (comando)                                                                           | Descripción                                                                  | Método IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| \_Reproducir título                                                                               | Reproducir un título.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| \_Juego PTT                                                                                 | Reproducir un capítulo en un título.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| Tiempo de \_ reproducción                                                                                | Reproducir un título a partir de una hora especificada.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Stop                                                                                      | Detenga la reproducción.                                                               | [**Stop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| De                                                                                      | Volver de un submenú al menú primario.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Búsqueda de hora \_                                                                              | Reproducir a una hora especificada dentro del título actual.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| Búsqueda de PTT \_                                                                               | Reproducir un capítulo dentro del título actual.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| Búsqueda de PrevPG \_                                                                            | Vaya al inicio del capítulo anterior y reanude la reproducción.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| Búsqueda de TopPG \_                                                                             | Vaya al inicio del capítulo actual y reanude la reproducción.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| Búsqueda de NextPG \_                                                                            | Vaya al inicio del capítulo siguiente y reanude la reproducción.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Examen hacia delante \_                                                                             | Avanzar a una velocidad de reproducción especificada. La velocidad de reproducción predeterminada es 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Examen hacia atrás \_                                                                            | Se reproduce hacia atrás con una velocidad de reproducción especificada.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Llamada de menú \_                                                                                | Mostrar un menú.                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Reanudar                                                                                    | Volver de un menú y reanudar la reproducción.                                      | [**Reanudar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| \_ \_ Selección de botón superior, \_ botón inferior \_ seleccionar, \_ botón izquierdo \_ seleccionar, \_ botón derecho \_ seleccionar | Seleccione un botón cuya posición sea relativa al botón seleccionado actualmente. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| \_Activar botón                                                                          | Activar el botón seleccionado.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| \_Selección \_ y \_ activación del botón                                                             | Seleccione y active un botón.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Todavía \_ desactivado                                                                                | Reanuda la reproducción al mostrar una imagen fija.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Pausar \_ en                                                                                 | Pausar reproducción.                                                              | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Pausar \_                                                                                | Reanuda la reproducción del estado de pausa.                                       | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| \_Selección de idioma de menú \_                                                                    | Seleccione el idioma de los menús.                                               | [**SelectDefaultMenuLanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| \_Cambio de secuencia de audio \_                                                                     | Establezca la secuencia de audio.                                                        | [**SelectAudioStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Cambio de secuencia de subimagen \_ \_                                                               | Establecer el flujo de la subimagen; habilitar o deshabilitar la visualización de la imagen.             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| Cambio de ángulo \_                                                                             | Establezca el ángulo de la cámara.                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| \_Selección de nivel parental \_                                                                   | Establezca el nivel parental.                                                      | [**SelectParentalLevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| \_Selección del país parental \_                                                                 | Establezca el país o región para la administración parental.                              | [**SelectParentalCountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| \_Cambio de \_ modo de presentación de audio de karaoke \_ \_                                                | Establezca el modo de combinación de audio para karaoke.                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| Cambio en el modo de presentación de vídeo \_ \_ \_                                                         | Establezca el modo de relación de aspecto en panorámico, panorámica o examen panorámico.             | [**SelectVideoModePreference**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



