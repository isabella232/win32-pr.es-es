---
title: Tipos de dispositivos
description: Tipos de dispositivos
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778504"
---
# <a name="device-types"></a>Tipos de dispositivos

MCI reconoce un conjunto básico de *tipos de dispositivo*. Un tipo de dispositivo es un conjunto de controladores MCI que comparten un conjunto de comandos común y se usan para controlar dispositivos multimedia o archivos de datos similares. Muchos comandos MCI, como [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)), requieren que especifique un tipo de dispositivo.

En la tabla siguiente se enumeran los tipos de dispositivos definidos. La implementación actual de MCI incluye conjuntos de comandos para un subconjunto de estos dispositivos.



| Tipo de dispositivo      | Constante                      | Descripción                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | AUDIO de CD de MCI \_ DEVTYPE \_ \_       | Reproductor de audio de CD                                  |
| **incrementa**          | \_ \_ archivos DAT de MCI DEVTYPE             | Reproductor de cintas de audio digital                        |
| **digitalvideo** | \_ \_ vídeo digital de MCI DEVTYPE \_  | Vídeo digital en una ventana (no basada en GDI)        |
| **distinta**        | MCI \_ DEVTYPE \_ otro           | Dispositivo MCI sin definir                             |
| **cubrimiento**      | superposición de MCI \_ DEVTYPE \_         | Dispositivo superpuesto (vídeo analógico en una ventana)        |
| **scanner**      | \_escáner MCI DEVTYPE \_         | Escáner de imágenes                                    |
| **sequencer**    | \_ \_ secuenciador MCI DEVTYPE       | Secuenciador MIDI                                   |
| **vídeos**          | \_VCR DEVTYPE de MCI \_             | Grabadora o reproductor de casete de vídeo                |
| **videodisco**    | videodisco de MCI \_ DEVTYPE \_       | Reproductor de videodisco                                 |
| **waveaudio**    | \_audio de \_ onda \_ DEVTYPE de MCI | Dispositivo de audio que reproduce archivos de onda digitalizados |



 

En este documento, los nombres de los tipos de dispositivo aparecen en negrita. Los nombres de tipo de dispositivo se usan con la interfaz de cadena de comandos. Las constantes de tipo de dispositivo se usan con la interfaz de mensajes de comandos.

 

 




