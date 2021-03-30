---
title: Detener, pausar y reanudar un dispositivo
description: Detener, pausar y reanudar un dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- Comando MCI_STOP
- Comando MCI_PAUSE
- Comando MCI_RESUME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776237"
---
# <a name="stopping-pausing-and-resuming-a-device"></a><span data-ttu-id="4ffec-106">Detener, pausar y reanudar un dispositivo</span><span class="sxs-lookup"><span data-stu-id="4ffec-106">Stopping, Pausing, and Resuming a Device</span></span>

<span data-ttu-id="4ffec-107">El comando [**detener**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) suspende la reproducción o grabación de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ffec-107">The [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command suspends the playing or recording of a device.</span></span> <span data-ttu-id="4ffec-108">Muchos dispositivos también admiten el comando [**pausar**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="4ffec-108">Many devices also support the [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="4ffec-109">La diferencia entre **detener** y **pausar** depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ffec-109">The difference between **stop** and **pause** depends on the device.</span></span> <span data-ttu-id="4ffec-110">Normalmente **pausa** suspende la operación, pero deja el dispositivo listo para reanudar la reproducción o grabación inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4ffec-110">Usually **pause** suspends operation but leaves the device ready to resume playing or recording immediately.</span></span>

<span data-ttu-id="4ffec-111">Con el comando [**reproducir**](play.md) ([**MCI \_ Play**](mci-play.md)) o [**registro**](record.md) ([**\_ registro de MCI**](mci-record.md)) para reiniciar un dispositivo, se restablecen las ubicaciones especificadas con las marcas "to" (MCI \_ to) y "from" (MCI \_ from) antes de que el dispositivo se haya pausado o detenido.</span><span class="sxs-lookup"><span data-stu-id="4ffec-111">Using the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) or [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command to restart a device resets the locations specified with the "to" (MCI\_TO) and "from" (MCI\_FROM) flags before the device was paused or stopped.</span></span> <span data-ttu-id="4ffec-112">Sin la marca "desde", estos comandos restablecen la ubicación inicial a la posición actual.</span><span class="sxs-lookup"><span data-stu-id="4ffec-112">Without the "from" flag, these commands reset the starting location to the current position.</span></span> <span data-ttu-id="4ffec-113">Sin la marca "para", restablecen la ubicación final al final del medio.</span><span class="sxs-lookup"><span data-stu-id="4ffec-113">Without the "to" flag, they reset the ending location to the end of the media.</span></span> <span data-ttu-id="4ffec-114">Para seguir reproduciendo o grabando sin restablecer una posición de detención especificada previamente, use la marca "para" del comando **Play** o **Record** para especificar una posición final.</span><span class="sxs-lookup"><span data-stu-id="4ffec-114">To continue playing or recording without resetting a previously specified stop position, use the **play** or **record** command's "to" flag to specify an ending position.</span></span>

<span data-ttu-id="4ffec-115">Algunos dispositivos admiten el comando [**reanudar**](resume.md) ([**\_ reanudar MCI**](mci-resume.md)) para reiniciar un dispositivo en pausa.</span><span class="sxs-lookup"><span data-stu-id="4ffec-115">Some devices support the [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)) command to restart a paused device.</span></span> <span data-ttu-id="4ffec-116">Este comando no cambia las ubicaciones "to" y "from" especificadas con el comando **Play** o **Record** que precedía al comando [**PAUSE**](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="4ffec-116">This command does not change the "to" and "from" locations specified with the **play** or **record** command that preceded the [**pause**](pause.md) command.</span></span>

 

 




