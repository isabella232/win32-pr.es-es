---
title: Acerca de MIDI
description: Acerca de MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows multimedia, interfaz digital de instrumentos musicales (MIDI)
- multimedia, interfaz digital de instrumentos musicales (MIDI)
- audio multimedia, interfaz digital de instrumentos musicales (MIDI)
- audio, interfaz digital de instrumentos musicales (MIDI)
- Interfaz digital de instrumentos musicales (MIDI), acerca de
- MIDI (interfaz digital de instrumentos musicales), acerca de
- Interfaz digital de instrumentos musicales (MIDI), interfaz de control de medios (MCI)
- MIDI (interfaz digital de instrumentos musicales), interfaz de control de medios (MCI)
- Interfaz digital de instrumentos musicales (MIDI), búferes de secuencia
- MIDI (interfaz digital de instrumentos musicales), búferes de secuencia
- Interfaz digital de instrumentos musicales (MIDI), servicios MIDI
- MIDI (interfaz digital de instrumentos musicales), servicios MIDI
- Media control Interface (MCI), interfaz digital de instrumentos musicales (MIDI)
- MCI (media control Interface), interfaz digital de instrumentos musicales (MIDI)
- búferes de secuencia, acerca de
- Servicios MIDI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774461"
---
# <a name="about-midi"></a>Acerca de MIDI

La interfaz de programación de aplicaciones (API) de Microsoft Win32 proporciona los siguientes métodos para que las aplicaciones funcionen con datos MIDI:

-   La interfaz de control de medios (MCI). Aunque la manera más sencilla de reproducir un archivo MIDI es usar la clase de ventana MCIWnd, también puede usar comandos MCI para crear una interfaz personalizada para un dispositivo MIDI. Para obtener más información sobre la clase de ventana MCIWnd, consulte [clase de ventana MCIWnd](mciwnd-window-class.md). Para obtener más información acerca de MCI, consulte [MCI](mci.md)o [media control Interface (MCI)](media-control-interface--mci.md).
-   [Búferes de secuencia](stream-buffers.md). Este formato permite a una aplicación manipular los búferes de datos MIDI con marca de tiempo para la reproducción. Los búferes de secuencia son útiles para las aplicaciones que requieren un control más preciso de la salida que las ofertas de MCI.
-   [Servicios MIDI](midi-services.md). Las aplicaciones que necesitan el control más preciso de los datos MIDI suelen usar estos servicios de bajo nivel.

En los temas siguientes se describe cada uno de estos métodos y se proporciona información general sobre el asignador MIDI.

-   [El asignador MIDI](the-midi-mapper.md)
-   [Media control Interface (MCI)](media-control-interface--mci.md)
-   [Búferes de secuencia](stream-buffers.md)
-   [Servicios MIDI](midi-services.md)
-   [Reproducir archivos MIDI](playing-midi-files.md)
-   [Grabación de audio MIDI](recording-midi-audio.md)
-   [Procesamiento de datos MIDI de dos orígenes MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Crear archivos MIDI](creating-midi-files.md)

 

 




