---
description: En este tema se describe cómo buscar durante la reproducción mediante MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Cómo buscar durante la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687120"
---
# <a name="how-to-seek-during-playback"></a><span data-ttu-id="adee4-103">Cómo buscar durante la reproducción</span><span class="sxs-lookup"><span data-stu-id="adee4-103">How to Seek During Playback</span></span>

<span data-ttu-id="adee4-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="adee4-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="adee4-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="adee4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="adee4-106">\]</span><span class="sxs-lookup"><span data-stu-id="adee4-106">\]</span></span>

<span data-ttu-id="adee4-107">En este tema se describe cómo buscar durante la reproducción mediante MFPlay.</span><span class="sxs-lookup"><span data-stu-id="adee4-107">This topic describes how to seek during playback using MFPlay.</span></span>

<span data-ttu-id="adee4-108">**Para buscar durante la reproducción**</span><span class="sxs-lookup"><span data-stu-id="adee4-108">**To Seek During Playback**</span></span>

1.  <span data-ttu-id="adee4-109">Inicialice un **PROPVARIANT** para que contenga el tiempo de búsqueda en unidades de 100-nanosegundos, como un tipo **\_ entero grande** (**VT \_ i8**).</span><span class="sxs-lookup"><span data-stu-id="adee4-109">Initialize a **PROPVARIANT** to hold the seek time in 100-nanosecond units, as a **LARGE\_INTEGER** (**VT\_I8**) type.</span></span>
2.  <span data-ttu-id="adee4-110">Llame a [**IMFPMediaPlayer:: SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span><span class="sxs-lookup"><span data-stu-id="adee4-110">Call [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span></span> <span data-ttu-id="adee4-111">Especifique **MFP \_ POSITIONTYPE de \_ 100 NS** para el primer parámetro y pase el **PROPVARIANT** para el segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="adee4-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter, and pass in the **PROPVARIANT** for the second parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="adee4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adee4-112">Requirements</span></span>

<span data-ttu-id="adee4-113">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="adee4-113">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adee4-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="adee4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adee4-115">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="adee4-115">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



