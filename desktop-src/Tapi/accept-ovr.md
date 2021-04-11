---
description: En algunos entornos, no se avisa automáticamente a un usuario de una llamada de oferta, como por ejemplo, por timbre o por un mensaje en la pantalla del equipo.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Aceptar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275314"
---
# <a name="accept"></a><span data-ttu-id="3f005-103">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3f005-103">Accept</span></span>

<span data-ttu-id="3f005-104">En algunos entornos, no se avisa automáticamente a un usuario de una llamada de oferta, como por ejemplo, por timbre o por un mensaje en la pantalla del equipo.</span><span class="sxs-lookup"><span data-stu-id="3f005-104">In some environments, a user is not automatically alerted to an offering call, such as by ringing or by a message on their computer screen.</span></span> <span data-ttu-id="3f005-105">La operación de aceptación inicia el proceso de alertas (que normalmente suenan) y la operación de [respuesta](answer-ovr.md) tiene lugar después.</span><span class="sxs-lookup"><span data-stu-id="3f005-105">The accept operation starts the process of alerting (usually ringing), and the [answer](answer-ovr.md) operation takes place afterward.</span></span> <span data-ttu-id="3f005-106">Es posible que la aplicación [Quite](drop-ovr.md) la sesión, la [redirija](redirect-ovr.md) o la acepte.</span><span class="sxs-lookup"><span data-stu-id="3f005-106">The application may [drop](drop-ovr.md) the session, [redirect](redirect-ovr.md) it, or accept it.</span></span>

<span data-ttu-id="3f005-107">Si el proveedor de servicios actual lo admite, la aplicación tiene la opción de enviar información de usuario al usuario en el momento de la aceptación.</span><span class="sxs-lookup"><span data-stu-id="3f005-107">If the current service provider supports it, the application has the option to send user-user information at the time of the accept.</span></span> <span data-ttu-id="3f005-108">No hay ninguna garantía de que la red entregue esta información a la entidad que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="3f005-108">There is no guarantee that the network will deliver this information to the calling party.</span></span>

<span data-ttu-id="3f005-109">No todos los proveedores de servicios admiten el uso de esta operación.</span><span class="sxs-lookup"><span data-stu-id="3f005-109">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="3f005-110">**TAPI 2. x:** Vea [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span><span class="sxs-lookup"><span data-stu-id="3f005-110">**TAPI 2.x:** See [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span></span>

 

 
