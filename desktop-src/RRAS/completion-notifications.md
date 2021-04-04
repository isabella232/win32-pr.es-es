---
title: Notificaciones de finalización
description: El administrador de conexiones de acceso remoto continúa con las notificaciones de progreso hasta que se completa la operación de conexión.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075763"
---
# <a name="completion-notifications"></a><span data-ttu-id="03c89-103">Notificaciones de finalización</span><span class="sxs-lookup"><span data-stu-id="03c89-103">Completion Notifications</span></span>

<span data-ttu-id="03c89-104">El administrador de conexiones de acceso remoto continúa con las notificaciones de progreso hasta que se completa la operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="03c89-104">The Remote Access Connection Manager continues progress notifications until the connection operation has been completed.</span></span> <span data-ttu-id="03c89-105">Esto sucede en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="03c89-105">This occurs in the following situations:</span></span>

-   <span data-ttu-id="03c89-106">El controlador recibe una \_ notificación RASCS conectada o RASCS \_ desconectada.</span><span class="sxs-lookup"><span data-stu-id="03c89-106">The handler receives a RASCS\_Connected, or RASCS\_Disconnected notification.</span></span> <span data-ttu-id="03c89-107">La aplicación cliente RAS puede salir sin interrumpir ninguna conexión establecida.</span><span class="sxs-lookup"><span data-stu-id="03c89-107">The RAS client application can exit without breaking any established connection.</span></span>
-   <span data-ttu-id="03c89-108">Se produce un error.</span><span class="sxs-lookup"><span data-stu-id="03c89-108">An error occurs.</span></span> <span data-ttu-id="03c89-109">El controlador recibe una notificación que indica el error y el estado de conexión cuando se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="03c89-109">The handler receives a notification indicating the error and the connection state when the error occurred.</span></span> <span data-ttu-id="03c89-110">La aplicación cliente RAS puede salir.</span><span class="sxs-lookup"><span data-stu-id="03c89-110">The RAS client application can exit.</span></span>

<span data-ttu-id="03c89-111">La aplicación cliente RAS no debe suponer que la operación de conexión se ha completado después de llamar a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span><span class="sxs-lookup"><span data-stu-id="03c89-111">The RAS client application should not assume the connection operation is complete after calling [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span></span> <span data-ttu-id="03c89-112">Antes de salir, debe esperar a una de las condiciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="03c89-112">It should wait for one of the preceding conditions before exiting.</span></span>

 

 




