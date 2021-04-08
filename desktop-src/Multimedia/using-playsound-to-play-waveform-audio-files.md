---
title: Usar PlaySound para reproducir archivos de Waveform-Audio
description: Usar PlaySound para reproducir archivos de Waveform-Audio
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- audio de onda, función PlaySound
- audio de onda, reproducir archivos
- audio de onda, extensión de nombre de archivo WAV
- Función PlaySound, reproducir archivos de audio de onda
- reproducir la onda-archivos de audio, función PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995248"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a><span data-ttu-id="bc7c1-108">Usar PlaySound para reproducir archivos de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="bc7c1-108">Using PlaySound to Play Waveform-Audio Files</span></span>

<span data-ttu-id="bc7c1-109">La mayoría de los archivos de audio de onda usan. Extensión de nombre de archivo WAV.</span><span class="sxs-lookup"><span data-stu-id="bc7c1-109">Most waveform-audio files use the .WAV filename extension.</span></span>

<span data-ttu-id="bc7c1-110">La siguiente instrucción reproduce las \\ campanas C: Sounds \\ . Archivo WAV:</span><span class="sxs-lookup"><span data-stu-id="bc7c1-110">The following statement plays the C:\\SOUNDS\\BELLS.WAV file:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



<span data-ttu-id="bc7c1-111">Si el archivo especificado no existe, o si el archivo no cabe en la memoria disponible, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) reproduce el sonido predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="bc7c1-111">If the specified file does not exist, or if the file does not fit into the available memory, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) plays the default system sound.</span></span> <span data-ttu-id="bc7c1-112">Si no se ha definido ningún sonido del sistema predeterminado, se produce un error en **PlaySound** sin generar ningún sonido.</span><span class="sxs-lookup"><span data-stu-id="bc7c1-112">If no default system sound has been defined, **PlaySound** fails without producing any sound.</span></span> <span data-ttu-id="bc7c1-113">Si no desea que se reproduzca el sonido del sistema predeterminado, especifique la \_ marca SND nodefault, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bc7c1-113">If you do not want the default system sound to play, specify the SND\_NODEFAULT flag, as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 