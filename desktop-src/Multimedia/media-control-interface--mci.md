---
title: Media control Interface (MCI)
description: Media control Interface (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Multimedia de Windows, interfaz de control de medios (MCI)
- multimedia, media control Interface (MCI)
- audio multimedia, interfaz de control de medios (MCI)
- audio, interfaz de control de medios (MCI)
- Interfaz digital de instrumentos musicales (MIDI), interfaz de control de medios (MCI)
- MIDI (interfaz digital de instrumentos musicales), interfaz de control de medios (MCI)
- Media control Interface (MCI), interfaz digital de instrumentos musicales (MIDI)
- MCI (media control Interface), interfaz digital de instrumentos musicales (MIDI)
- Media control Interface (MCI), MIDI Sequencer
- MCI (media control Interface), MIDI Sequencer
- Secuenciador MIDI de MCI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075647"
---
# <a name="media-control-interface-mci"></a>Media control Interface (MCI)

MCI MIDI Sequencer es el componente del sistema MCI que reproduce archivos MIDI. Las aplicaciones pueden reproducir archivos MIDI fácilmente mediante MCI, pero MCI impone las siguientes restricciones en las capacidades MIDI:

-   MCI solo admite la salida MIDI.
-   MCI no permite la sincronización de cierre entre eventos MIDI y otros eventos en tiempo real (por ejemplo, vídeo).

Si necesita la sincronización de MIDI precisa, debe utilizar los búferes de secuencia o los servicios MIDI. Si necesita funciones de entrada MIDI, debe utilizar los servicios MIDI.

MCI MIDI Sequencer reproduce archivos MIDI estándar y archivos MIDI de formato de archivo de intercambio de recursos (RIFF), conocidos como archivos RMID. Los archivos MIDI estándar se ajustan a la especificación [estándar de los archivos midi 1,0](creating-midi-files.md) . Dado que los archivos RMID son archivos MIDI estándar con un encabezado RIFF, la información acerca de los archivos MIDI estándar también se aplica a los archivos RMID. Para obtener más información acerca de los archivos RIFF, vea [servicios de formato de archivo de intercambio de recursos](resource-interchange-file-format-services.md).

Aunque actualmente hay tres tipos de archivos MIDI estándar, MCI Sequencer solo reproduce dos de ellos: Format 0 y Format 1 archivos MIDI.

Para obtener más información sobre cómo controlar los dispositivos multimedia (incluidos los secuenciadores) mediante comandos MCI, consulte [MCI](mci.md).

 

 




