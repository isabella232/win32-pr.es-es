---
title: Interfaz de control multimedia (MCI)
description: Interfaz de control multimedia (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Windows multimedia,Interfaz de control multimedia (MCI)
- multimedia, Interfaz de control multimedia (MCI)
- audio multimedia, interfaz de control multimedia (MCI)
- audio,Media Control Interface (MCI)
- Interfaz digital de instrumentar música (MIDI),Interfaz de control multimedia (MCI)
- MIDI (Interfaz digital instrumentada),Interfaz de control multimedia (MCI)
- Interfaz de control multimedia (MCI),Interfaz digital de instrumentar música (MIDI)
- MCI (Interfaz de control multimedia),Interfaz digital de instrumentar música (MIDI)
- Interfaz de control multimedia (MCI), secuenciador DE LÍNEA
- MCI (interfaz de control multimedia),secuenciador DE LÍNEA
- Secuenciador DE MCI MIDI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8d21588754d0f66dbed97c74bbaabe4c005335059dace2997012691a24c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782985"
---
# <a name="media-control-interface-mci"></a>Interfaz de control multimedia (MCI)

El secuenciador MCI MIDI es el componente del sistema MCI que reproduce archivos MIDI. Las aplicaciones pueden reproducir archivos MIDI fácilmente mediante MCI, pero MCI impone las siguientes restricciones en las funcionalidades de MIDI:

-   MCI solo admite la salida de MIDI.
-   MCI no permite la sincronización de cierre entre eventos MIDI y otros eventos en tiempo real (por ejemplo, vídeo).

Si necesita una sincronización precisa de MIDI, debe usar los búferes de flujo o los servicios DE MIDI. Si necesita funcionalidades de entrada de MIDI, debe usar los servicios DE MIDI.

El secuenciador MCI MIDI reproduce archivos ESTÁNDAR y archivos DE FORMATO DE ARCHIVO DE INTERCAMBIO DE RECURSOS (RIFF), conocidos como archivos RMID. Los archivos MIDI estándar se ajustan a [la especificación Standard MIDI Files 1.0.](creating-midi-files.md) Dado que los archivos RMID son archivos MIDI estándar con un encabezado RIFF, la información sobre los archivos ESTÁNDAR DE MIDI también se aplica a los archivos RMID. Para obtener más información sobre los archivos RIFF, vea [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

Aunque actualmente hay tres tipos de archivos ESTÁNDAR DE MIDI, el secuenciador MCI reproduce solo dos de ellos: Formato 0 y Formato 1 archivos MIDI.

Para obtener más información sobre el control de dispositivos multimedia (incluidos los secuenciadores) mediante comandos MCI, vea [MCI](mci.md).

 

 




