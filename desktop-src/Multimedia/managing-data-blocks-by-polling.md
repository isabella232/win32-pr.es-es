---
title: Administrar bloques de datos mediante sondeo
description: Administrar bloques de datos mediante sondeo
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- audio de onda, bloqueos de datos de sondeo
- bloques de datos de audio, sondeo
- sondear bloques de datos de audio
- Estructura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077613"
---
# <a name="managing-data-blocks-by-polling"></a><span data-ttu-id="b3aa5-107">Administrar bloques de datos mediante sondeo</span><span class="sxs-lookup"><span data-stu-id="b3aa5-107">Managing Data Blocks by Polling</span></span>

<span data-ttu-id="b3aa5-108">Además de usar una función de devolución de llamada, puede sondear el miembro **dwFlags** de una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para determinar cuándo ha finalizado un dispositivo de audio con un bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-108">In addition to using a callback function, you can poll the **dwFlags** member of a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to determine when an audio device is finished with a data block.</span></span> <span data-ttu-id="b3aa5-109">A veces es mejor sondear **dwFlags** que esperar a que otro mecanismo reciba mensajes de los controladores.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-109">Sometimes it is better to poll **dwFlags** than to wait for another mechanism to receive messages from the drivers.</span></span> <span data-ttu-id="b3aa5-110">Por ejemplo, después de llamar a la función [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) para liberar bloques de datos pendientes, puede sondear inmediatamente para asegurarse de que se han liberado los bloques de datos antes de llamar a [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) y liberar memoria para el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-110">For example, after you call the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function to release pending data blocks, you can immediately poll to be sure that the data blocks have been released before calling [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) and freeing the memory for the data block.</span></span>

<span data-ttu-id="b3aa5-111">Puede usar la marca WHDR \_ Done para probar el miembro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="b3aa5-111">You can use the WHDR\_DONE flag to test the **dwFlags** member.</span></span> <span data-ttu-id="b3aa5-112">\_En cuanto se establece la marca WHDR done en el miembro **dwFlags** de la estructura **WAVEHDR** , el controlador finaliza con el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="b3aa5-112">As soon as the WHDR\_DONE flag is set in the **dwFlags** member of the **WAVEHDR** structure, the driver is finished with the data block.</span></span>

 

 