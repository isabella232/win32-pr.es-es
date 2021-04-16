---
title: Instrucciones para tareas en segundo plano en Servicios de Escritorio remoto
description: Para maximizar la disponibilidad de la CPU para todos los usuarios, deshabilite las tareas en segundo plano cuando se ejecute en un entorno de Servicios de Escritorio remoto o cree tareas en segundo plano eficaces que no consuman muchos recursos.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685504"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a><span data-ttu-id="edec4-103">Instrucciones para tareas en segundo plano en Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="edec4-103">Guidelines for background tasks in Remote Desktop Services</span></span>

<span data-ttu-id="edec4-104">Tareas en segundo plano: las tareas que se realizan cuando el bucle de mensajes de una aplicación está inactiva, proporcionan un mecanismo para controlar las tareas de prioridad baja en un entorno de un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="edec4-104">Background tasks—tasks performed when an application's message loop is idle—provide a mechanism for handling low-priority tasks in a single-user environment.</span></span> <span data-ttu-id="edec4-105">En un entorno de Servicios de Escritorio remoto, sin embargo, la tarea en segundo plano de un usuario compite en los ciclos de la CPU con las tareas en primer plano de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="edec4-105">In a Remote Desktop Services environment, however, one user's background task competes for CPU cycles with another user's foreground tasks.</span></span> <span data-ttu-id="edec4-106">Cuando varios usuarios ejecutan tareas en primer plano y en segundo plano, las demandas de la CPU son mucho mayores que cuando todos los usuarios ejecutan solo tareas en primer plano.</span><span class="sxs-lookup"><span data-stu-id="edec4-106">When multiple users are running both foreground and background tasks, the CPU demands are much higher than when all users are running only foreground tasks.</span></span> <span data-ttu-id="edec4-107">Para maximizar la disponibilidad de la CPU para todos los usuarios, deshabilite las tareas en segundo plano cuando se ejecute en un entorno de Servicios de Escritorio remoto o cree tareas en segundo plano eficaces que no consuman muchos recursos.</span><span class="sxs-lookup"><span data-stu-id="edec4-107">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

<span data-ttu-id="edec4-108">Para obtener más información, consulte [detectar el entorno de servicios de escritorio remoto](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="edec4-108">For more information, see [Detecting the Remote Desktop Services environment](detecting-the-terminal-services-environment.md).</span></span> <span data-ttu-id="edec4-109">Después de detectar el entorno de Servicios de Escritorio remoto, puede deshabilitar o volver a configurar las tareas en segundo plano de la aplicación mediante el mismo conjunto de API que utilizó para administrar las tareas.</span><span class="sxs-lookup"><span data-stu-id="edec4-109">After you detect the Remote Desktop Services environment, you can disable or reconfigure background tasks for the application using the same set of APIs that you used to manage the tasks.</span></span>

 

 




