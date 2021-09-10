---
title: Acerca de MIDI
description: Acerca de MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows multimedia,Interfaz digital de instrumentar música (MIDI)
- multimedia, Interfaz digital de instrumentar música (MIDI)
- audio multimedia, interfaz digital de instrumentar música (MIDI)
- audio,Interfaz digital de instrumentar música (MIDI)
- Interfaz digital de instrumentar música (MIDI), acerca de
- MIDI (Interfaz digital de instrumentar música), acerca de
- Interfaz digital de instrumentar música (MIDI),Interfaz de control multimedia (MCI)
- MIDI (Interfaz digital instrumentada),Interfaz de control multimedia (MCI)
- Interfaz digital de instrumentar música (MIDI), búferes de flujo
- MIDI (Interfaz digital de instrumentar música), búferes de flujo
- Interfaz digital de instrumentar música (MIDI), servicios DE MIDI
- MIDI (Interfaz digital de instrumentar música), servicios DE MIDI
- Interfaz de control multimedia (MCI),Interfaz digital de instrumentar música (MIDI)
- MCI (Interfaz de control multimedia),Interfaz digital de instrumentar música (MIDI)
- búferes de flujo, acerca de
- Servicios DE MIDI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370795"
---
# <a name="about-midi"></a>Acerca de MIDI

La interfaz de programación de aplicaciones (API) de Microsoft Win32 proporciona los métodos siguientes para que las aplicaciones funcionen con datos DE MIDI:

-   La interfaz de control multimedia (MCI). Aunque la manera más sencilla de reproducir un archivo MIDI es usar la clase de ventana MCIWnd, también puede usar comandos MCI para crear una interfaz personalizada para un dispositivo MIDI. Para obtener más información sobre la clase de ventana MCIWnd, vea [Clase de ventana MCIWnd](mciwnd-window-class.md). Para obtener más información sobre MCI, vea [MCI](mci.md)o [Interfaz de control multimedia (MCI).](media-control-interface--mci.md)
-   [Búferes de flujo](stream-buffers.md). Este formato permite que una aplicación manipule búferes de datos DE MIDI con marca de tiempo para la reproducción. Los búferes de flujo son útiles para las aplicaciones que requieren un control más preciso sobre la salida que las ofertas de MCI.
-   [Servicios DE MIDI](midi-services.md). Las aplicaciones que necesitan el control más preciso de los datos DE MIDI suelen usar estos servicios de bajo nivel.

En los temas siguientes se describe cada uno de estos métodos y se proporciona información general sobre el asignador de MIDI.

-   [Asignador de MIDI](the-midi-mapper.md)
-   [Interfaz de control multimedia (MCI)](media-control-interface--mci.md)
-   [Búferes de flujo](stream-buffers.md)
-   [Servicios DE MIDI](midi-services.md)
-   [Reproducir archivos MIDI](playing-midi-files.md)
-   [Grabación de audio DE AUDIO DE AUDIO](recording-midi-audio.md)
-   [Procesamiento de datos DE MIDI de dos orígenes DE MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Creación de archivos MIDI](creating-midi-files.md)

 

 




