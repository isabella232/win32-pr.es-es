---
title: Interfaz de control multimedia (MCI)
description: Interfaz de control multimedia (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Windows multimedia,Interfaz de control multimedia (MCI)
- multimedia, Interfaz de control multimedia (MCI)
- audio multimedia, interfaz de control multimedia (MCI)
- audio,Interfaz de control multimedia (MCI)
- Interfaz digital instrumentada (MIDI), Interfaz de control multimedia (MCI)
- MIDI (Interfaz digital instrumentada),Interfaz de control multimedia (MCI)
- Interfaz de control multimedia (MCI),Interfaz digital instrumentada (MIDI)
- MCI (Interfaz de control multimedia),Interfaz digital de instrumentar música (MIDI)
- Interfaz de control multimedia (MCI), secuenciador MIDI
- MCI (interfaz de control multimedia), secuenciador DE LÍNEA
- Secuenciador DE MCI MIDI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071761"
---
# <a name="media-control-interface-mci"></a>Interfaz de control multimedia (MCI)

El secuenciador MCI MIDI es el componente del sistema MCI que reproduce archivos MIDI. Las aplicaciones pueden reproducir archivos MIDI fácilmente mediante MCI, pero MCI impone las restricciones siguientes en las funcionalidades de MIDI:

-   MCI solo admite la salida DE MIDI.
-   MCI no permite la sincronización estrecha entre eventos MIDI y otros eventos en tiempo real (como vídeo).

Si necesita una sincronización de MIDI precisa, debe usar los búferes de flujo o los servicios DE MIDI. Si necesita funcionalidades de entrada de MIDI, debe usar los servicios DE MIDI.

El secuenciador MCI MIDI reproduce archivos ESTÁNDAR DE MIDI y archivos DE FORMATO DE ARCHIVO DE INTERCAMBIO DE RECURSOS (RIFF), conocidos como archivos RMID. Los archivos MIDI estándar se ajustan a [la especificación Standard MIDI Files 1.0.](creating-midi-files.md) Dado que los archivos RMID son archivos MIDI estándar con un encabezado RIFF, la información sobre los archivos MIDI estándar también se aplica a los archivos RMID. Para obtener más información sobre los archivos RIFF, vea [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

Aunque actualmente hay tres tipos de archivos MIDI estándar, el secuenciador MCI reproduce solo dos de ellos: archivos MIDI de formato 0 y formato 1.

Para obtener más información sobre cómo controlar dispositivos multimedia (incluidos los secuenciadores) mediante comandos [MCI,](mci.md)vea MCI .

 

 




