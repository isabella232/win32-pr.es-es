---
title: Reproducir y colocar
description: Reproducir y colocar
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651296"
---
# <a name="playback-and-positioning"></a><span data-ttu-id="cbc8f-103">Reproducir y colocar</span><span class="sxs-lookup"><span data-stu-id="cbc8f-103">Playback and Positioning</span></span>

<span data-ttu-id="cbc8f-104">Una serie de comandos de MCI, como [**reproducir**](play.md) ([**MCI \_ Play**](mci-play.md)), [**detener**](stop.md) ([**MCI \_ Stop**](mci-stop.md)), [**pausar**](pause.md) (MCI [**\_ PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**\_ reanudación de MCI**](mci-resume.md)) y [**búsqueda**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), afectan a la reproducción o la ubicación de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-104">A number of MCI commands, such as [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)), and [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)), affect the playback or positioning of a multimedia file.</span></span> <span data-ttu-id="cbc8f-105">Si un dispositivo MCI recibe un comando de reproducción mientras otro comando de reproducción está en curso, acepta el comando y detiene o reemplaza el comando anterior.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-105">If an MCI device receives a playback command while another playback command is in progress, it accepts the command and either stops or supersedes the previous command.</span></span>

<span data-ttu-id="cbc8f-106">Muchos comandos de MCI, como [**set**](set.md) ([**\_ conjunto de MCI**](mci-set.md)), no afectan a la reproducción.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-106">Many MCI commands, such as [**set**](set.md) ([**MCI\_SET**](mci-set.md)), do not affect playback.</span></span> <span data-ttu-id="cbc8f-107">Una notificación de uno de estos comandos no interfiere con los comandos de reproducción o posición pendientes, siempre y cuando las notificaciones no se realicen desde la misma instancia del controlador.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-107">A notification from one of these commands does not interfere with pending playback or position commands as long as the notifications are not performed from the same instance of the driver.</span></span> <span data-ttu-id="cbc8f-108">Por ejemplo, puede emitir un comando **set** o [**status**](status.md) ([**\_ Estado de MCI**](mci-status.md)) mientras un dispositivo está realizando un comando **Seek** sin detener o reemplazar el comando **Seek** .</span><span class="sxs-lookup"><span data-stu-id="cbc8f-108">For example, you can issue a **set** or [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command while a device is performing a **seek** command without stopping or superseding the **seek** command.</span></span>

<span data-ttu-id="cbc8f-109">Sin embargo, solo puede haber una notificación pendiente.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-109">However, there can be only one pending notification.</span></span> <span data-ttu-id="cbc8f-110">Por ejemplo, si una aplicación solicita una notificación para que se **reproduzca** y sigue a esa solicitud con el **Estado** "Start Position Notify", la notificación de **reproducción** devolverá "Returned" y la notificación del comando status devolverá cuando termine.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-110">For example, if an application requests a notification for **play** and follows that request with **status** "start position notify," the **play** notification will return "superseded" and the notification for the status command will return when it is finished.</span></span> <span data-ttu-id="cbc8f-111">Sin embargo, en este caso, el comando **Play** seguirá teniendo éxito, aunque la aplicación no haya recibido la notificación.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-111">In this case, however, the **play** command will still succeed, even though the application did not receive the notification.</span></span>

 

 




