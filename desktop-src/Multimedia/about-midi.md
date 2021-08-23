---
title: Acerca de MIDI
description: Acerca de MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows multimedia,Interfaz digital de instrumentar música (MIDI)
- multimedia, Interfaz digital instrumenta de Música (MIDI)
- audio multimedia, interfaz digital instrumenta de Música (MIDI)
- audio,Instrument Digital Interface (MIDI)
- Interfaz digital de instrumentar música (MIDI), acerca de
- MIDI (Interfaz digital de instrumentado), acerca de
- Interfaz digital instrumentada (MIDI), Interfaz de control multimedia (MCI)
- MIDI (Interfaz digital instrumentada),Interfaz de control multimedia (MCI)
- Interfaz digital instrumentable (MIDI), búferes de secuencia
- MIDI (Interfaz digital instrumenta de música), búferes de secuencia
- Interfaz digital instrumentable (MIDI), servicios DE MIDI
- MIDI (Interfaz digital instrumenta de música), servicios DE MIDI
- Interfaz de control multimedia (MCI),Interfaz digital instrumentada (MIDI)
- MCI (Interfaz de control multimedia),Interfaz digital instrumentada (MIDI)
- búferes de flujo, acerca de
- Servicios DE MIDI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1ce20164c42342c52defd27e7f3ccdfb0a44ec9a4e0a6679c1b190270fc62e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526695"
---
# <a name="about-midi"></a>Acerca de MIDI

La interfaz de programación de aplicaciones (API) Win32 de Microsoft proporciona los métodos siguientes para que las aplicaciones funcionen con datos DE MIDI:

-   Interfaz de control multimedia (MCI). Aunque la manera más sencilla de reproducir un archivo MIDI es usar la clase de ventana MCIWnd, también puede usar comandos MCI para crear una interfaz personalizada para un dispositivo MIDI. Para obtener más información sobre la clase de ventana MCIWnd, vea [Clase de ventana MCIWnd](mciwnd-window-class.md). Para obtener más información sobre MCI, vea [MCI](mci.md)o [Interfaz de control multimedia (MCI).](media-control-interface--mci.md)
-   [Búferes de secuencia.](stream-buffers.md) Este formato permite a una aplicación manipular búferes de datos DE MIDI con marca de tiempo para la reproducción. Los búferes de flujo son útiles para las aplicaciones que requieren un control más preciso sobre la salida que las ofertas de MCI.
-   [Servicios DE MIDI](midi-services.md). Las aplicaciones que necesitan el control más preciso de los datos DE MIDI suelen usar estos servicios de bajo nivel.

En los temas siguientes se describe cada uno de estos métodos y se proporciona información general sobre el asignador de MIDI.

-   [Asignador de MIDI](the-midi-mapper.md)
-   [Interfaz de control multimedia (MCI)](media-control-interface--mci.md)
-   [Búferes de flujo](stream-buffers.md)
-   [Servicios DE MIDI](midi-services.md)
-   [Reproducir archivos MIDI](playing-midi-files.md)
-   [Grabación de audio MIDI](recording-midi-audio.md)
-   [Procesamiento de datos DE MIDI de dos orígenes DE MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Crear archivos MIDI](creating-midi-files.md)

 

 




