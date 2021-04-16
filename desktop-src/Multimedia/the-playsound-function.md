---
title: La función PlaySound
description: La función PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimedia, función PlaySound
- audio, función PlaySound
- audio de onda, función PlaySound
- Función PlaySound, acerca de
- sndPlaySound función)
- Función PlaySound, en comparación con la función sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270882"
---
# <a name="the-playsound-function"></a><span data-ttu-id="c6080-109">La función PlaySound</span><span class="sxs-lookup"><span data-stu-id="c6080-109">The PlaySound Function</span></span>

<span data-ttu-id="c6080-110">Puede usar la función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproducir audio de una onda si el sonido encaja en la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="c6080-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play waveform audio if the sound fits into available memory.</span></span> <span data-ttu-id="c6080-111">(La función [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) ofrece un subconjunto de las capacidades de PlaySound.</span><span class="sxs-lookup"><span data-stu-id="c6080-111">(The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function offers a subset of the capabilities of PlaySound.</span></span> <span data-ttu-id="c6080-112">Para maximizar la portabilidad de la aplicación basada en Win32, use **PlaySound**, no **sndPlaySound**).</span><span class="sxs-lookup"><span data-stu-id="c6080-112">To maximize the portability of your Win32-based application, use **PlaySound**, not **sndPlaySound**.)</span></span>

<span data-ttu-id="c6080-113">La función **PlaySound** le permite especificar un sonido de una de estas tres maneras:</span><span class="sxs-lookup"><span data-stu-id="c6080-113">The **PlaySound** function allows you to specify a sound in one of three ways:</span></span>

-   <span data-ttu-id="c6080-114">Como alerta del sistema, mediante el alias almacenado en el archivo WIN.INI o el registro</span><span class="sxs-lookup"><span data-stu-id="c6080-114">As a system alert, using the alias stored in the WIN.INI file or the registry</span></span>
-   <span data-ttu-id="c6080-115">Como nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="c6080-115">As a filename</span></span>
-   <span data-ttu-id="c6080-116">Como identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="c6080-116">As a resource identifier</span></span>

<span data-ttu-id="c6080-117">La función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) permite reproducir un sonido en un bucle continuo y finalizar solo cuando se vuelve a llamar a **PlaySound** , especificando **null** o el identificador de sonido de otro sonido para el parámetro *pszSound* .</span><span class="sxs-lookup"><span data-stu-id="c6080-117">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function allows you to play a sound in a continuous loop, ending only when you call **PlaySound** again, specifying either **NULL** or the sound identifier of another sound for the *pszSound* parameter.</span></span>

<span data-ttu-id="c6080-118">Puede usar **PlaySound** para reproducir el sonido de forma sincrónica o asincrónica, y para controlar el comportamiento de la función de otras maneras cuando debe compartir recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="c6080-118">You can use **PlaySound** to play the sound synchronously or asynchronously, and to control the behavior of the function in other ways when it must share system resources.</span></span>

<span data-ttu-id="c6080-119">Para obtener más información sobre el uso de PlaySound, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6080-119">For more information about using PlaySound, see the following topics:</span></span>

-   [<span data-ttu-id="c6080-120">Usar PlaySound para reproducir archivos de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="c6080-120">Using PlaySound to Play Waveform-Audio Files</span></span>](using-playsound-to-play-waveform-audio-files.md)
-   [<span data-ttu-id="c6080-121">Usar PlaySound para reproducir sonidos</span><span class="sxs-lookup"><span data-stu-id="c6080-121">Using PlaySound to Loop Sounds</span></span>](using-playsound-to-loop-sounds.md)
-   [<span data-ttu-id="c6080-122">Usar PlaySound para reproducir sonidos del sistema</span><span class="sxs-lookup"><span data-stu-id="c6080-122">Using PlaySound to Play System Sounds</span></span>](using-playsound-to-play-system-sounds.md)

<span data-ttu-id="c6080-123">Para obtener más ejemplos de cómo usar **PlaySound** en las aplicaciones basadas en Win32, vea [reproducir recursos de Wave](playing-wave-resources.md).</span><span class="sxs-lookup"><span data-stu-id="c6080-123">For more examples of how to use **PlaySound** in your Win32-based applications, see [Playing WAVE Resources](playing-wave-resources.md).</span></span>

 

 