---
title: Control de errores de RAS
description: Cuando se produce un error, el administrador de conexiones de acceso remoto invoca el controlador de notificaciones del cliente.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS de servicio de acceso remoto, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778403"
---
# <a name="handling-ras-errors"></a><span data-ttu-id="3f700-104">Control de errores de RAS</span><span class="sxs-lookup"><span data-stu-id="3f700-104">Handling RAS Errors</span></span>

<span data-ttu-id="3f700-105">Cuando se produce un error, el administrador de conexiones de acceso remoto invoca el controlador de notificaciones del cliente.</span><span class="sxs-lookup"><span data-stu-id="3f700-105">When an error occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="3f700-106">La notificación indica el estado de conexión cuando se produjo el error y un código que identifica el error.</span><span class="sxs-lookup"><span data-stu-id="3f700-106">The notification indicates the connection state when the error occurred, and a code that identifies the error.</span></span> <span data-ttu-id="3f700-107">En estos casos, el controlador de notificación debe llamar a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para finalizar la conexión RAS.</span><span class="sxs-lookup"><span data-stu-id="3f700-107">In these cases, the notification handler should call [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) to end the RAS connection.</span></span>

<span data-ttu-id="3f700-108">Los códigos de error que identifican los errores de RAS se definen en el archivo raserror. h.</span><span class="sxs-lookup"><span data-stu-id="3f700-108">The error codes that identify RAS errors are defined in the file raserror.h.</span></span> <span data-ttu-id="3f700-109">El cliente RAS puede usar la función [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) para obtener una cadena de presentación que describa el error.</span><span class="sxs-lookup"><span data-stu-id="3f700-109">The RAS client can use the [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) function to get a display string describing the error.</span></span> <span data-ttu-id="3f700-110">Consulte [códigos de error de enrutamiento y acceso remoto](routing-and-remote-access-error-codes.md) para obtener una descripción de estos errores.</span><span class="sxs-lookup"><span data-stu-id="3f700-110">See [Routing and Remote Access Error Codes](routing-and-remote-access-error-codes.md) for a description of these errors.</span></span>

 

 




