---
title: Reproducción de audio simple
description: Reproducción de audio simple
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimedia, de onda
- audio, de onda
- audio de forma de onda, reproducción simple
- MessageBeep función)
- sndPlaySound función)
- Función PlaySound, reproducción simple
- audio multimedia, función PlaySound
- audio, función PlaySound
- audio de onda, función PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995175"
---
# <a name="simple-audio-playback"></a>Reproducción de audio simple

Puede utilizar las siguientes funciones para reproducir audio de una onda en la aplicación en una única llamada de función.



| Función                                                      | Descripción                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Reproduce el sonido que corresponde a un nivel de alerta del sistema especificado.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Reproduce el sonido que corresponde al sonido del sistema escrito en el registro o el contenido del archivo especificado. |
| [**Reproducción**](/previous-versions//dd743680(v=vs.85))                                | Proporciona toda la funcionalidad de [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) y puede acceder directamente a los recursos.           |



 

La función **MessageBeep** es una parte estándar de la API de Win32; Dado que sus capacidades son muy limitadas y se documentan en otro lugar, no se trata aquí.

Las funciones enumeradas admiten los siguientes orígenes de audio de onda:

-   Archivos de audio de forma de onda asociados a los niveles de alerta del sistema
-   Forma de onda: archivos de audio especificados por entradas en el registro
-   Recursos de onda en memoria
-   Forma de onda-archivos de audio especificados por nombre

Las funciones [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) y [**PlaySound**](/previous-versions//dd743680(v=vs.85)) cargan un archivo de audio de onda completo en la memoria y, de hecho, limitan el tamaño del archivo que pueden reproducir. Use **sndPlaySound** y **PlaySound** para reproducir archivos de audio de forma de onda pequeños, de hasta 100 000. Estas dos funciones también requieren que los datos de sonido estén en un formato que se pueda reproducir con uno de los controladores de audio de forma de onda instalados, incluido el asignador de onda.

En el caso de archivos de sonido de mayor tamaño, utilice los servicios de media control Interface (MCI). Para obtener más información, consulte [MCI](mci.md).

 

 