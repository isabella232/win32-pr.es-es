---
description: El streaming es el proceso de mantener solo una pequeña parte de un archivo de audio de reproducción en memoria. Esto permite reproducir archivos de audio grandes, como música de fondo, y no ocupa una gran cantidad de memoria.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Datos de audio de streaming de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df15420adce8f8807c3f969615a2cf6d5b51981e03fd7067e2c1c3348d1b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805395"
---
# <a name="xaudio2-streaming-audio-data"></a>Datos de audio de streaming de XAudio2

El streaming es el proceso de mantener solo una pequeña parte de un archivo de audio de reproducción en memoria. Esto permite reproducir archivos de audio grandes, como música de fondo, y no ocupa una gran cantidad de memoria.

Cuando se transmite un archivo de audio, sus datos se leen desde el disco en fragmentos en lugar de cargar todo el archivo a la vez. El streaming se realiza mediante la lectura asincrónica de datos de audio en una cola de búferes de disco. Cada búfer se rellena y, a continuación, se envía a una voz de origen. Una vez que la voz termina de reproducir un búfer, el búfer vuelve a estar disponible para su lectura. Recorrer en bucle los búferes de disco de esta manera permite reproducir un archivo de audio grande mientras solo se carga una parte de sus datos. El código de streaming debe colocarse en un subproceso independiente, donde puede suspensión mientras espera a que finalicen las operaciones de disco y audio de larga duración. Una clase de devolución de llamada se usa para reactivar el subproceso desencadenando eventos cuando finalizan las operaciones de audio.

Para obtener un ejemplo de cómo se puede realizar el streaming con XAudio2, vea Cómo: Transmitir [un sonido desde el disco.](how-to--stream-a-sound-from-disk.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Streaming de datos de audio](streaming-audio-data.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 



