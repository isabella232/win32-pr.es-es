---
title: Invertir reproducción
description: Invertir reproducción
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418667"
---
# <a name="reversing-playback"></a><span data-ttu-id="0d12e-104">Invertir reproducción</span><span class="sxs-lookup"><span data-stu-id="0d12e-104">Reversing Playback</span></span>

<span data-ttu-id="0d12e-105">Algunos dispositivos admiten la reproducción en dirección inversa.</span><span class="sxs-lookup"><span data-stu-id="0d12e-105">Some devices support playback in the reverse direction.</span></span> <span data-ttu-id="0d12e-106">Puede reproducir el contenido de este dispositivo en la dirección inversa mediante la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="0d12e-106">You can play the content of such a device in the reverse direction by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span> <span data-ttu-id="0d12e-107">Esta macro define el ámbito de reproducción desde la posición de reproducción actual hasta el principio del contenido.</span><span class="sxs-lookup"><span data-stu-id="0d12e-107">This macro defines the playback scope from the current playback position to the beginning of the content.</span></span> <span data-ttu-id="0d12e-108">El dispositivo de vídeo digital, MCIAVI. DRV, puede reproducirse hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="0d12e-108">The digital-video device, MCIAVI.DRV, can play backward.</span></span> <span data-ttu-id="0d12e-109">Los dispositivos que no pueden reproducirse hacia atrás, como el audio de CD, pueden emitir un mensaje de error cuando se invoca **MCIWndPlayReverse** .</span><span class="sxs-lookup"><span data-stu-id="0d12e-109">Devices that cannot play backward, such as CD audio, can issue an error message when **MCIWndPlayReverse** is invoked.</span></span>

 

 




