---
description: La finalización de la sesión puede provenir de una solicitud de usuario, de una desconexión remota por parte de la otra o de razones específicas de la aplicación.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Finalizar una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688749"
---
# <a name="terminate-a-session"></a><span data-ttu-id="0fe66-103">Finalizar una sesión</span><span class="sxs-lookup"><span data-stu-id="0fe66-103">Terminate a Session</span></span>

<span data-ttu-id="0fe66-104">La finalización de la sesión puede provenir de una solicitud de usuario, de una desconexión remota por parte de la otra o de razones específicas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0fe66-104">Session termination may originate with a user request, remote disconnection by the other party, or for application-specific reasons.</span></span> <span data-ttu-id="0fe66-105">Cuando finaliza una sesión, el [identificador de sesión](session-identifier-ovr.md) sigue siendo válido hasta que se libera específicamente y se puede usar para recopilar datos posteriores a la conexión.</span><span class="sxs-lookup"><span data-stu-id="0fe66-105">When a session is terminated, the [session identifier](session-identifier-ovr.md) remains valid until specifically released and can be used to gather post-connection data.</span></span>

<span data-ttu-id="0fe66-106">La finalización de la sesión se completa desasignando y liberando los recursos asociados a la sesión.</span><span class="sxs-lookup"><span data-stu-id="0fe66-106">Session termination is completed by deallocating and releasing the resources associated with the session.</span></span> <span data-ttu-id="0fe66-107">Si una sesión simplemente se quita o se desconecta pero no se liberan recursos, el resultado es una pérdida de memoria en la aplicación y posiblemente también en el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="0fe66-107">If a session is merely dropped or disconnected but resources are not released, the result is a memory leak in the application and possibly in the service provider as well.</span></span>

<span data-ttu-id="0fe66-108">**TAPI 2. x:** Vea [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span><span class="sxs-lookup"><span data-stu-id="0fe66-108">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span></span>

<span data-ttu-id="0fe66-109">**TAPI 3. x:** Vea [**ITBasicCallControl::D Ulta**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), realizar una versión com estándar en el puntero del objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="0fe66-109">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), perform a standard COM release on the Call object pointer.</span></span>

 

 
