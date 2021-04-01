---
description: La mayoría de las operaciones GET y set solo se ocupan de un componente de la información. La función phoneGetStatus devuelve información de estado completa sobre un dispositivo telefónico a una aplicación.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Estado (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909617"
---
# <a name="status-telephony-api"></a><span data-ttu-id="e94c5-104">Estado (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="e94c5-104">Status (Telephony API)</span></span>

<span data-ttu-id="e94c5-105">La mayoría de las operaciones GET y set solo se ocupan de un componente de la información.</span><span class="sxs-lookup"><span data-stu-id="e94c5-105">Most of the get and set operations deal with one component of information only.</span></span> <span data-ttu-id="e94c5-106">La función [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) devuelve información de estado completa sobre un dispositivo telefónico a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e94c5-106">The [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) function returns complete status information about a phone device to an application.</span></span>

<span data-ttu-id="e94c5-107">Como se mencionó anteriormente, cada vez que un elemento de estado cambia en el dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la función de aplicación.</span><span class="sxs-lookup"><span data-stu-id="e94c5-107">As mentioned earlier, whenever a status item changes on the phone device, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function.</span></span> <span data-ttu-id="e94c5-108">Los parámetros de este mensaje incluyen un identificador del dispositivo telefónico y una indicación del elemento de estado que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e94c5-108">This message's parameters include a handle to the phone device and an indication of the status item that changed.</span></span>

<span data-ttu-id="e94c5-109">Una aplicación puede utilizar [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) para seleccionar los cambios de estado específicos para los que desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e94c5-109">An application can use [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) to select the specific status changes for which it wants to be notified.</span></span> <span data-ttu-id="e94c5-110">En consecuencia, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) devuelve los cambios de estado para los que la aplicación desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e94c5-110">Correspondingly, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) returns the status changes for which the application wants to be notified.</span></span>

 

 



