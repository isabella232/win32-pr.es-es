---
title: Iniciar, pausar y reanudar la reproducción
description: Iniciar, pausar y reanudar la reproducción
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay (macro)
- MCIWndPause (macro)
- MCIWndResume (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269403"
---
# <a name="starting-pausing-and-resuming-playback"></a><span data-ttu-id="e2b90-106">Iniciar, pausar y reanudar la reproducción</span><span class="sxs-lookup"><span data-stu-id="e2b90-106">Starting, Pausing, and Resuming Playback</span></span>

<span data-ttu-id="e2b90-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) es la macro de reproducción más general.</span><span class="sxs-lookup"><span data-stu-id="e2b90-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) is the most general playback macro.</span></span> <span data-ttu-id="e2b90-108">Esta macro permite reproducir un archivo o un dispositivo desde la posición de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="e2b90-108">This macro lets you play a file or device from the current playback position.</span></span> <span data-ttu-id="e2b90-109">La reproducción continúa hasta el final del contenido a menos que se interrumpa.</span><span class="sxs-lookup"><span data-stu-id="e2b90-109">Playback continues through the end of the content unless it is interrupted.</span></span>

<span data-ttu-id="e2b90-110">Puede interrumpir temporalmente un dispositivo que se está reproduciendo con la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) .</span><span class="sxs-lookup"><span data-stu-id="e2b90-110">You can temporarily interrupt a device that is playing by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="e2b90-111">Para reanudar la reproducción desde la posición en pausa, use la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) .</span><span class="sxs-lookup"><span data-stu-id="e2b90-111">To resume playback from the paused position, use the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="e2b90-112">Algunos dispositivos no admiten los comandos pausar y reanudar.</span><span class="sxs-lookup"><span data-stu-id="e2b90-112">Some devices do not support the pause and resume commands.</span></span> <span data-ttu-id="e2b90-113">Normalmente, estos dispositivos asignan **MCIWndPause** a la macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , que detiene la reproducción o grabación.</span><span class="sxs-lookup"><span data-stu-id="e2b90-113">These devices usually map **MCIWndPause** to the [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) macro, which stops playback or recording.</span></span> <span data-ttu-id="e2b90-114">Puede reiniciar un dispositivo que no admita pausar o reanudar mediante **MCIWndPlay**, que inicia la reproducción desde la posición de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="e2b90-114">You can restart a device that does not support pause or resume by using **MCIWndPlay**, which starts playback from the current playback position.</span></span>

 

 




