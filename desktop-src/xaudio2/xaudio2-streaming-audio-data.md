---
description: La transmisión por secuencias es el proceso de mantener solo una pequeña parte de la reproducción de un archivo de audio en la memoria. Esto permite reproducir archivos de audio de gran tamaño, como música de fondo, y no ocupar una gran cantidad de memoria.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Datos de audio de streaming de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707124"
---
# <a name="xaudio2-streaming-audio-data"></a>Datos de audio de streaming de XAudio2

La transmisión por secuencias es el proceso de mantener solo una pequeña parte de la reproducción de un archivo de audio en la memoria. Esto permite reproducir archivos de audio de gran tamaño, como música de fondo, y no ocupar una gran cantidad de memoria.

Cuando se transmite un archivo de audio, sus datos se leen desde el disco en fragmentos, en lugar de cargar todo el archivo a la vez. La transmisión por secuencias se realiza mediante la lectura asincrónica de datos de audio en una cola de búferes de disco. Cada búfer se rellena y, a continuación, se envía a una voz de origen. Una vez que la voz finaliza la reproducción de un búfer, el búfer vuelve a estar disponible para su lectura. El bucle de los búferes de disco de esta manera permite reproducir un archivo de audio de gran tamaño, mientras que solo se carga una parte de sus datos. El código de streaming debe colocarse en un subproceso independiente, donde se puede suspender mientras se espera que finalicen las operaciones de disco y audio de larga duración. Una clase de devolución de llamada se usa para reactivar el subproceso desencadenando eventos cuando se han completado las operaciones de audio.

Para ver un ejemplo de cómo se puede realizar el streaming con XAudio2, consulte [Cómo: transmitir un sonido desde un disco](how-to--stream-a-sound-from-disk.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transmisión de datos de audio](streaming-audio-data.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 



