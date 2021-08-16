---
description: Comandos de DVD
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: Comandos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02f9c0b6a50b6d7eb67832286ee980b0faf69460621a46caf98089efc24b19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820589"
---
# <a name="dvd-commands"></a>Comandos de DVD

Los comandos de navegación y reproducción de DVD se definen en una sección de la especificación de DVD denominada Anexo J, por lo que la documentación de DirectShow a menudo hace referencia a "Comandos J anexos". Sin embargo, los nombres que se dan en el anexo J no siempre son muy intuitivos, por lo DirectShow usa nombres que pueden ser más fáciles de entender.

En la tabla siguiente se enumeran los comandos del anexo J y sus DirectShow equivalentes.



| Comando J del anexo                                                                           | Descripción                                                                  | Método IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Reproducción \_ de título                                                                               | Reproducir un título.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT \_ Play                                                                                 | Reproducir un capítulo de un título.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| Time \_ Play                                                                                | Reproducir un título a partir de una hora especificada.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Stop                                                                                      | Detenga la reproducción.                                                               | [**Stop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| Goup                                                                                      | Vuelva de un submenú al menú primario.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Búsqueda de \_ tiempo                                                                              | Reproducir a la hora especificada dentro del título actual.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| PTT \_ Search                                                                               | Reproducir un capítulo dentro del título actual.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| PrevPG \_ Search                                                                            | Vaya al inicio del capítulo anterior y reanude la reproducción.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| TopPG \_ Search                                                                             | Vaya al inicio del capítulo actual y reanude la reproducción.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| NextPG \_ Search                                                                            | Vaya al inicio del capítulo siguiente y reanude la reproducción.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Análisis \_ hacia delante                                                                             | Reproducir hacia delante a una velocidad de reproducción especificada. La velocidad de reproducción predeterminada es 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Examen \_ hacia atrás                                                                            | Reproducir hacia atrás a una velocidad de reproducción especificada.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Llamada de \_ menú                                                                                | Mostrar un menú.                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Reanudar                                                                                    | Vuelva desde un menú y reanude la reproducción.                                      | [**Reanudar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| Upper \_ Button \_ Select, Lower \_ Button \_ Select, Left \_ Button \_ Select, Right \_ Button \_ Select | Seleccione un botón cuya posición sea relativa al botón seleccionado actualmente. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Activar \_ botón                                                                          | Active el botón seleccionado.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Botón \_ Seleccionar \_ y \_ activar                                                             | Seleccione y active un botón.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Still \_ Off                                                                                | Reanude la reproducción al mostrar una imagen fija.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Pausar \_ en                                                                                 | Pausar la reproducción.                                                              | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Pausar \_ desactivado                                                                                | Reanude la reproducción desde el estado en pausa.                                       | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Selección del \_ idioma del \_ menú                                                                    | Seleccione el idioma de los menús.                                               | [**SeleccioneDefaultMenuLanguage.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| Cambio \_ de secuencia de \_ audio                                                                     | Establezca la secuencia de audio.                                                        | [**SeleccioneAudioStream.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Cambio de secuencia \_ de sub \_ picture                                                               | Establezca la secuencia de subimagen; habilitar o deshabilitar la presentación de subimagen.             | [**SeleccioneSubpictureStream.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| Cambio de \_ ángulo                                                                             | Establezca el ángulo de la cámara.                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| Selección \_ de nivel \_ parental                                                                   | Establezca el nivel parental.                                                      | [**SeleccioneParentalLevel.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Selección \_ del país \_ parental                                                                 | Establezca el país o región para la administración parental.                              | [**SeleccioneParentalCountry.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| Cambio \_ del modo de presentación audio de Audio de \_ \_ \_ Audio                                                | Establezca el modo de mezcla de audio para la mezcla de audio.                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| Cambio \_ del modo de presentación de \_ \_ vídeo                                                         | Establezca el modo de relación de aspecto en widescreen, letterbox o pan scan.             | [**SeleccioneVideoModePreference.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



