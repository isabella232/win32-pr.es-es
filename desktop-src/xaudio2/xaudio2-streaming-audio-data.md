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
# <a name="xaudio2-streaming-audio-data"></a><span data-ttu-id="dd843-104">Datos de audio de streaming de XAudio2</span><span class="sxs-lookup"><span data-stu-id="dd843-104">XAudio2 Streaming Audio Data</span></span>

<span data-ttu-id="dd843-105">La transmisión por secuencias es el proceso de mantener solo una pequeña parte de la reproducción de un archivo de audio en la memoria.</span><span class="sxs-lookup"><span data-stu-id="dd843-105">Streaming is the process of maintaining only a small portion of a playing audio file in memory.</span></span> <span data-ttu-id="dd843-106">Esto permite reproducir archivos de audio de gran tamaño, como música de fondo, y no ocupar una gran cantidad de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd843-106">This allows large audio files such as background music to be played, and not take up a large amount of memory.</span></span>

<span data-ttu-id="dd843-107">Cuando se transmite un archivo de audio, sus datos se leen desde el disco en fragmentos, en lugar de cargar todo el archivo a la vez.</span><span class="sxs-lookup"><span data-stu-id="dd843-107">When an audio file is streamed, its data is read from disk in chunks rather than loading the entire file at once.</span></span> <span data-ttu-id="dd843-108">La transmisión por secuencias se realiza mediante la lectura asincrónica de datos de audio en una cola de búferes de disco.</span><span class="sxs-lookup"><span data-stu-id="dd843-108">Streaming is accomplished by asynchronously reading audio data into a queue of disk buffers.</span></span> <span data-ttu-id="dd843-109">Cada búfer se rellena y, a continuación, se envía a una voz de origen.</span><span class="sxs-lookup"><span data-stu-id="dd843-109">Each buffer is filled, and then submitted to a source voice.</span></span> <span data-ttu-id="dd843-110">Una vez que la voz finaliza la reproducción de un búfer, el búfer vuelve a estar disponible para su lectura.</span><span class="sxs-lookup"><span data-stu-id="dd843-110">After the voice finishes playing a buffer, the buffer becomes available for reading again.</span></span> <span data-ttu-id="dd843-111">El bucle de los búferes de disco de esta manera permite reproducir un archivo de audio de gran tamaño, mientras que solo se carga una parte de sus datos.</span><span class="sxs-lookup"><span data-stu-id="dd843-111">Looping through the disk buffers in this manner allows a large audio file to be played while only a portion of its data is loaded.</span></span> <span data-ttu-id="dd843-112">El código de streaming debe colocarse en un subproceso independiente, donde se puede suspender mientras se espera que finalicen las operaciones de disco y audio de larga duración.</span><span class="sxs-lookup"><span data-stu-id="dd843-112">The streaming code should be placed in a separate thread, where it can sleep while waiting for long-running disk and audio operations to finish.</span></span> <span data-ttu-id="dd843-113">Una clase de devolución de llamada se usa para reactivar el subproceso desencadenando eventos cuando se han completado las operaciones de audio.</span><span class="sxs-lookup"><span data-stu-id="dd843-113">A callback class is used to wake the thread by triggering events when audio operations have finished.</span></span>

<span data-ttu-id="dd843-114">Para ver un ejemplo de cómo se puede realizar el streaming con XAudio2, consulte [Cómo: transmitir un sonido desde un disco](how-to--stream-a-sound-from-disk.md).</span><span class="sxs-lookup"><span data-stu-id="dd843-114">For an example of how streaming can be accomplished with XAudio2, see [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd843-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd843-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd843-116">Transmisión de datos de audio</span><span class="sxs-lookup"><span data-stu-id="dd843-116">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="dd843-117">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="dd843-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



