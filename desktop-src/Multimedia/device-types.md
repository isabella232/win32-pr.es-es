---
title: Tipos de dispositivo
description: Tipos de dispositivo
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371617"
---
# <a name="device-types"></a>Tipos de dispositivo

MCI reconoce un conjunto básico de tipos *de dispositivo.* Un tipo de dispositivo es un conjunto de controladores MCI que comparten un conjunto de comandos común y se usan para controlar archivos de datos o dispositivos multimedia similares. Muchos comandos MCI, como [**open**](open.md) [**(MCI \_ OPEN),**](mci-open.md)requieren que especifique un tipo de dispositivo.

En la tabla siguiente se enumeran los tipos de dispositivo definidos. La implementación actual de MCI incluye conjuntos de comandos para un subconjunto de estos dispositivos.



| Tipo de dispositivo      | Constante                      | Descripción                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | MCI \_ DEVTYPE \_ CD \_ AUDIO       | Reproductor de audio de CD                                  |
| **Dat**          | DAT \_ DE TIPO DEVTYPE de MCI \_             | Reproductor de cinta de audio digital                        |
| **digitalvideo** | VÍDEO DIGITAL \_ DE MCI DEVTYPE \_ \_  | Vídeo digital en una ventana (no basado en GDI)        |
| **Otro**        | MCI \_ DEVTYPE \_ OTHER           | Dispositivo MCI sin definir                             |
| **Superposición**      | SUPERPOSICIÓN \_ MCI DEVTYPE \_         | Dispositivo superpuesto (vídeo análogo en una ventana)        |
| **scanner**      | ANALIZADOR \_ DE MCI DEVTYPE \_         | Escáner de imágenes                                    |
| **sequencer**    | MCI \_ DEVTYPE \_ SEQUENCER       | Secuenciador DE LÍNEA                                   |
| **Vcr**          | MCI \_ DEVTYPE \_ VCR             | Reproductor o grabadora de vídeo                |
| **Videodisco**    | VÍDEO \_ DEVTYPE \_ DE MCIDISC       | Reproductor de Videodisc                                 |
| **waveaudio**    | AUDIO DE \_ FORMA DE ONDA DE DEVTYPE \_ \_ DE MCI | Dispositivo de audio que reproduce archivos de forma de onda digitalizados |



 

En este documento, los nombres de los tipos de dispositivo están en negrita. Los nombres de tipo de dispositivo se usan con la interfaz de cadena de comandos. Las constantes de tipo de dispositivo se usan con la interfaz command-message.

 

 




