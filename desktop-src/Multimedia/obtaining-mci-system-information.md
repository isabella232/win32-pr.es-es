---
title: Obtención de información del sistema MCI
description: Obtención de información del sistema MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Comando MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994130"
---
# <a name="obtaining-mci-system-information"></a><span data-ttu-id="8703f-104">Obtención de información del sistema MCI</span><span class="sxs-lookup"><span data-stu-id="8703f-104">Obtaining MCI System Information</span></span>

<span data-ttu-id="8703f-105">El comando [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) obtiene información del sistema acerca de los dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="8703f-105">The [sysinfo](sysinfo.md) ([**MCI\_SYSINFO**](mci-sysinfo.md)) command obtains system information about MCI devices.</span></span> <span data-ttu-id="8703f-106">MCI controla este comando sin retransmitirlo a ningún dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="8703f-106">MCI handles this command without relaying it to any MCI device.</span></span> <span data-ttu-id="8703f-107">En la interfaz de mensaje de comando, MCI devuelve la información del sistema en la estructura de [**\_ \_ parms de MCI SYSINFO**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8703f-107">For the command-message interface, MCI returns the system information in the [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

<span data-ttu-id="8703f-108">Puede usar el comando **sysinfo** (MCI \_ sysinfo) para recuperar información como el número de dispositivos MCI en un sistema, el número de dispositivos MCI de un tipo determinado, el número de dispositivos MCI abiertos y los nombres de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8703f-108">You can use the **sysinfo** (MCI\_SYSINFO) command to retrieve information such as the number of MCI devices on a system, the number of MCI devices of a particular type, the number of open MCI devices, and the names of the devices.</span></span> <span data-ttu-id="8703f-109">Este comando a menudo se llama más de una vez para recuperar una parte determinada de la información.</span><span class="sxs-lookup"><span data-stu-id="8703f-109">This command is often called more than once to retrieve a particular piece of information.</span></span> <span data-ttu-id="8703f-110">Por ejemplo, puede recuperar el número de dispositivos de un tipo determinado en la primera llamada y, a continuación, enumerar los nombres de los dispositivos en el siguiente.</span><span class="sxs-lookup"><span data-stu-id="8703f-110">For example, you might retrieve the number of devices of a particular type in the first call and then enumerate the names of the devices in the next.</span></span>

 

 




