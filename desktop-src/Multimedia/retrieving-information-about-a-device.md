---
title: Recuperación de información acerca de un dispositivo
description: Recuperación de información acerca de un dispositivo
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- Comando MCI_GETDEVCAPS
- Comando MCI_STATUS
- Comando MCI_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994550"
---
# <a name="retrieving-information-about-a-device"></a><span data-ttu-id="a02b5-106">Recuperación de información acerca de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="a02b5-106">Retrieving Information About a Device</span></span>

<span data-ttu-id="a02b5-107">Cada dispositivo responde a los comandos [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI \_ status**](mci-status.md)) y [**info**](info.md) ([**MCI \_ info**](mci-info.md)).</span><span class="sxs-lookup"><span data-stu-id="a02b5-107">Every device responds to the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)), and [**info**](info.md) ([**MCI\_INFO**](mci-info.md)) commands.</span></span> <span data-ttu-id="a02b5-108">Estos comandos obtienen información sobre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a02b5-108">These commands obtain information about the device.</span></span> <span data-ttu-id="a02b5-109">Por ejemplo, el siguiente comando devuelve "true" Si un dispositivo **cdaudio** puede expulsar el disco:</span><span class="sxs-lookup"><span data-stu-id="a02b5-109">For example, the following command returns "true" if a **cdaudio** device can eject the disc:</span></span>


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="a02b5-110">Las marcas enumeradas para los comandos necesarios y básicos proporcionan una cantidad mínima de información sobre un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a02b5-110">The flags listed for the required and basic commands provide a minimum amount of information about a device.</span></span> <span data-ttu-id="a02b5-111">Muchos dispositivos complementan los comandos necesarios y básicos con marcas extendidas para proporcionar información adicional sobre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a02b5-111">Many devices supplement the required and basic commands with extended flags to provide additional information about the device.</span></span>

 

 




