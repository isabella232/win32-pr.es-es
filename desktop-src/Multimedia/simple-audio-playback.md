---
title: Reproducción de audio simple
description: Reproducción de audio simple
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimedia, forma de onda
- audio, forma de onda
- audio de forma de onda, reproducción simple
- Función MessageBeep
- Función sndPlaySound
- Función Play Sound, reproducción sencilla
- audio multimedia, función Play Sound
- audio, función Play Sound
- audio de forma de onda, función PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6388f9800f93080e995ae537c2458a22da033ab2149b4bfca114c25025d97434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688695"
---
# <a name="simple-audio-playback"></a>Reproducción de audio simple

Puede usar las siguientes funciones para reproducir audio de forma de onda en la aplicación en una sola llamada de función.



| Función                                                      | Descripción                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Reproduce el sonido que corresponde a un nivel de alerta del sistema especificado.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Reproduce el sonido que corresponde al sonido del sistema especificado en el registro o al contenido del archivo especificado. |
| [**PlaySound**](/previous-versions//dd743680(v=vs.85))                                | Proporciona toda la funcionalidad de [**sndPlaySound y**](/previous-versions//dd798676(v=vs.85)) puede acceder directamente a los recursos.           |



 

La **función MessageBeep** es una parte estándar de la API de Win32; dado que sus capacidades son muy limitadas y se documentan en otra parte, no se trata aquí.

Las funciones enumeradas admiten los siguientes orígenes de audio de forma de onda:

-   Archivos de audio de forma de onda asociados a niveles de alerta del sistema
-   Archivos de audio de forma de onda especificados por las entradas del Registro
-   Recursos de WAVE en memoria
-   Archivos de audio de forma de onda especificados por nombre

Las [**funciones sndPlaySound**](/previous-versions//dd798676(v=vs.85)) y [**PlaySound**](/previous-versions//dd743680(v=vs.85)) cargan un archivo de audio de forma de onda completo en la memoria y, en efecto, limitan el tamaño del archivo que pueden reproducir. Use **sndPlaySound** y **PlaySound para** reproducir archivos de audio de forma de onda pequeños, hasta unos 100 000. Estas dos funciones también requieren que los datos de sonido se puedan reproducir en uno de los controladores de audio de forma de onda instalados, incluido el asignador de onda.

Para archivos de sonido más grandes, use los servicios de la interfaz de control multimedia (MCI). Para obtener más información, vea [MCI](mci.md).

 

 