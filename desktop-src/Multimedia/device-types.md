---
title: Tipos de dispositivo
description: Tipos de dispositivo
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167eedddfc61960de35e979480c44b8f2efab5bf89738047446196b81a95a5b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497165"
---
# <a name="device-types"></a>Tipos de dispositivo

MCI reconoce un conjunto básico de tipos *de dispositivo.* Un tipo de dispositivo es un conjunto de controladores MCI que comparten un conjunto de comandos común y se usan para controlar archivos de datos o dispositivos multimedia similares. Muchos comandos de MCI, como [**open**](open.md) [**(MCI \_ OPEN),**](mci-open.md)requieren que especifique un tipo de dispositivo.

En la tabla siguiente se enumeran los tipos de dispositivo definidos. La implementación actual de MCI incluye conjuntos de comandos para un subconjunto de estos dispositivos.



| Tipo de dispositivo      | Constante                      | Descripción                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | AUDIO DE \_ CD MCI DEVTYPE \_ \_       | Reproductor de audio de CD                                  |
| **Dat**          | DAT \_ DE TIPO DEVTYPE de MCI \_             | Reproductor de cinta de audio digital                        |
| **digitalvideo** | VÍDEO DIGITAL \_ DE MCI DEVTYPE \_ \_  | Vídeo digital en una ventana (no basado en GDI)        |
| **Otro**        | MCI \_ DEVTYPE \_ OTHER           | Dispositivo MCI sin definir                             |
| **Superposición**      | SUPERPOSICIÓN \_ DE DEVTYPE DE MCI \_         | Dispositivo superpuesto (vídeo análogo en una ventana)        |
| **scanner**      | ANALIZADOR \_ DE MCI DEVTYPE \_         | Escáner de imágenes                                    |
| **sequencer**    | SECUENCIADOR \_ DEVTYPE DE MCI \_       | Secuenciador DE LÍNEA                                   |
| **Vcr**          | VCR \_ DEVTYPE de MCI \_             | Grabadora o reproductor de video-recorder                |
| **Videodisco**    | VÍDEO \_ DEVTYPE DE \_ MCIDISC       | Reproductor de Videodisc                                 |
| **waveaudio**    | AUDIO DE \_ FORMA DE ONDA DE DEVTYPE \_ DE MCI \_ | Dispositivo de audio que reproduce archivos de forma de onda digitalizados |



 

En este documento, los nombres de los tipos de dispositivo están en negrita. Los nombres de tipo de dispositivo se usan con la interfaz de cadena de comandos. Las constantes de tipo de dispositivo se usan con la interfaz command-message.

 

 




