---
description: Sincronizar la VMR con la frecuencia de actualización del monitor
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Sincronizar la VMR con la frecuencia de actualización del monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279016"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a><span data-ttu-id="8b62e-103">Sincronizar la VMR con la frecuencia de actualización del monitor</span><span class="sxs-lookup"><span data-stu-id="8b62e-103">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>

<span data-ttu-id="8b62e-104">En raras ocasiones, es posible que desee sincronizar con precisión la representación de vídeo con la frecuencia de actualización del monitor, de modo que se presente exactamente un nuevo fotograma cada vez que se actualice el monitor.</span><span class="sxs-lookup"><span data-stu-id="8b62e-104">In rare scenarios, you may wish to precisely synchronize video rendering with the monitor's refresh rate, so that exactly one new frame is presented each time the monitor refreshes.</span></span> <span data-ttu-id="8b62e-105">La forma más confiable de hacerlo es crear un asignador personalizado-presentador que use una operación de volteo en lugar de una operación de blit para escribir los bits de vídeo en la superficie principal.</span><span class="sxs-lookup"><span data-stu-id="8b62e-105">The most reliable way to do this is to create a custom allocator-presenter that uses a flip operation instead of a blit operation to write the video bits into the primary surface.</span></span> <span data-ttu-id="8b62e-106">Se llama a "Flip" cada vez que se actualiza el monitor, por lo que si la secuencia de vídeo no contiene ninguna marca de tiempo, la VMR se representará lo más rápido posible a la superficie principal, pero la superficie bloqueará la secuencia hasta que se complete la operación de volteo.</span><span class="sxs-lookup"><span data-stu-id="8b62e-106">"Flip" is called each time the monitor refreshes, so if your video stream contains no time stamps, the VMR will render as fast as possible to the primary surface, but the surface will block the stream until the Flip operation completes.</span></span> <span data-ttu-id="8b62e-107">Esto significa que, siempre que no se sobrecargará la CPU, el siguiente fotograma siempre estará esperando en la superficie principal cada vez que se actualice el monitor.</span><span class="sxs-lookup"><span data-stu-id="8b62e-107">This means that, as long as the CPU is not overburdened, the next frame will always be waiting in the primary surface each time the monitor refreshes.</span></span> <span data-ttu-id="8b62e-108">Sin embargo, si se está ejecutando algún otro proceso de uso intensivo de la CPU, podría privar el subproceso de streaming de DirectShow para que no pueda ofrecer fotogramas de vídeo lo suficientemente rápido a la superficie principal.</span><span class="sxs-lookup"><span data-stu-id="8b62e-108">However, if some other CPU-intensive process is running, it could possibly starve your DirectShow streaming thread so that it cannot deliver video frames fast enough to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b62e-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b62e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b62e-110">Modo de reproducción no representativo de VMR (asignador personalizado)</span><span class="sxs-lookup"><span data-stu-id="8b62e-110">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



