---
description: El protocolo Kerberos se compone de tres subprotocolos.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Subprotocolos Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277147"
---
# <a name="kerberos-subprotocols"></a><span data-ttu-id="8af41-103">Subprotocolos Kerberos</span><span class="sxs-lookup"><span data-stu-id="8af41-103">Kerberos Subprotocols</span></span>

<span data-ttu-id="8af41-104">El [*protocolo Kerberos*](../secgloss/k-gly.md) se compone de tres subprotocolos.</span><span class="sxs-lookup"><span data-stu-id="8af41-104">The [*Kerberos protocol*](../secgloss/k-gly.md) is composed of three subprotocols.</span></span>



| <span data-ttu-id="8af41-105">Subprotocolo</span><span class="sxs-lookup"><span data-stu-id="8af41-105">Subprotocol</span></span>                                                                         | <span data-ttu-id="8af41-106">Significado</span><span class="sxs-lookup"><span data-stu-id="8af41-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8af41-107">Intercambio del servicio de autenticación</span><span class="sxs-lookup"><span data-stu-id="8af41-107">Authentication Service Exchange</span></span>](authentication-service-exchange.md)<br/>   | <span data-ttu-id="8af41-108">En este subprotocolo, el [*centro de distribución de claves*](../secgloss/k-gly.md) (KDC) proporciona al cliente una [*clave de sesión*](../secgloss/s-gly.md) de inicio de sesión y un vale de concesión de vales (TGT).</span><span class="sxs-lookup"><span data-stu-id="8af41-108">In this subprotocol, the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) gives the client a logon [*session key*](../secgloss/s-gly.md) and a ticket-granting ticket (TGT).</span></span><br/> |
| [<span data-ttu-id="8af41-109">Intercambio del servicio de concesión de vales</span><span class="sxs-lookup"><span data-stu-id="8af41-109">Ticket-Granting Service Exchange</span></span>](ticket-granting-service-exchange.md)<br/> | <span data-ttu-id="8af41-110">En este subprotocolo, el KDC distribuye una clave de sesión de servicio y un vale para el servicio.</span><span class="sxs-lookup"><span data-stu-id="8af41-110">In this subprotocol, the KDC distributes a service session key and a ticket for the service.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="8af41-111">Intercambio de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="8af41-111">Client/Server Exchange</span></span>](client-server-exchange.md)<br/>                     | <span data-ttu-id="8af41-112">En este subprotocolo, el cliente presenta el vale para la admisión a un servicio.</span><span class="sxs-lookup"><span data-stu-id="8af41-112">In this subprotocol, the client presents the ticket for admission to a service.</span></span><br/>                                                                                                                                                                                                                         |



 

 

 
