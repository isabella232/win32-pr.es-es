---
title: Cerrar un dispositivo
description: Cerrar un dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Comando MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418402"
---
# <a name="closing-a-device"></a><span data-ttu-id="93ca0-104">Cerrar un dispositivo</span><span class="sxs-lookup"><span data-stu-id="93ca0-104">Closing a Device</span></span>

<span data-ttu-id="93ca0-105">El comando [**cerrar**](close.md) ([**\_ cerrar MCI**](mci-close.md)) libera el acceso a un dispositivo o a un archivo.</span><span class="sxs-lookup"><span data-stu-id="93ca0-105">The [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) command releases access to a device or file.</span></span> <span data-ttu-id="93ca0-106">MCI libera un dispositivo cuando todas las tareas que usan un dispositivo lo han cerrado.</span><span class="sxs-lookup"><span data-stu-id="93ca0-106">MCI frees a device when all tasks using a device have closed it.</span></span> <span data-ttu-id="93ca0-107">Para ayudar a MCI a administrar los dispositivos, la aplicación debe cerrar cada dispositivo o archivo cuando haya terminado de usarlo.</span><span class="sxs-lookup"><span data-stu-id="93ca0-107">To help MCI manage the devices, your application must close each device or file when it is finished using it.</span></span>

<span data-ttu-id="93ca0-108">Cuando se cierra un dispositivo MCI externo que usa su propio medio en lugar de archivos (por ejemplo, audio de CD), el controlador deja el dispositivo en su modo de funcionamiento actual.</span><span class="sxs-lookup"><span data-stu-id="93ca0-108">When you close an external MCI device that uses its own media instead of files (such as CD audio), the driver leaves the device in its current mode of operation.</span></span> <span data-ttu-id="93ca0-109">Por lo tanto, si cierra un dispositivo de audio de CD que se está reproduciendo, aunque el controlador de dispositivo se libere de la memoria, el dispositivo de audio de CD seguirá reproduciéndose hasta que llegue al final de su contenido.</span><span class="sxs-lookup"><span data-stu-id="93ca0-109">Thus, if you close a CD audio device that is playing, even though the device driver is released from memory, the CD audio device will continue to play until it reaches the end of its content.</span></span>

> [!Note]  
> <span data-ttu-id="93ca0-110">Cerrar una aplicación con dispositivos MCI abiertos puede impedir que otras aplicaciones usen esos dispositivos hasta que se reinicie Windows.</span><span class="sxs-lookup"><span data-stu-id="93ca0-110">Closing an application with open MCI devices can prevent other applications from using those devices until Windows is restarted.</span></span>

 

 

 




