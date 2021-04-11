---
description: El direccionamiento local de vínculo IPv6 en los mensajes SOAP proporciona un desafío único, ya que las direcciones locales de vínculo IPv6 requieren un identificador de ámbito que sea significativo, pero el identificador de ámbito solo tiene significado para el equipo local.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Usar direcciones locales de vínculo IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155236"
---
# <a name="using-ipv6-link-local-addresses"></a><span data-ttu-id="081ef-103">Usar direcciones locales de vínculo IPv6</span><span class="sxs-lookup"><span data-stu-id="081ef-103">Using IPv6 Link-Local Addresses</span></span>

<span data-ttu-id="081ef-104">El direccionamiento local de vínculo IPv6 en los mensajes SOAP proporciona un desafío único, ya que las direcciones locales de vínculo IPv6 requieren un identificador de ámbito que sea significativo, pero el identificador de ámbito solo tiene significado para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="081ef-104">IPv6 link-local addressing in SOAP messages provides a unique challenge, as IPv6 link-local addresses require a scope ID to be meaningful, but the scope ID only has meaning for the local machine.</span></span> <span data-ttu-id="081ef-105">Todas las implementaciones de cliente y de dispositivo deben quitar el identificador de ámbito antes de enviar una dirección local de vínculo IPv6 en un mensaje SOAP.</span><span class="sxs-lookup"><span data-stu-id="081ef-105">All client and device implementations must remove the scope ID before sending an IPv6 link-local address in a SOAP message.</span></span> <span data-ttu-id="081ef-106">Además, cuando se recibe una dirección local de vínculo IPv6 en un mensaje, se debe conocer la interfaz en la que se recibió el mensaje, por lo que se puede reconstruir la dirección local del vínculo completo con el identificador de ámbito.</span><span class="sxs-lookup"><span data-stu-id="081ef-106">Additionally, when an IPv6 link-local address is received in a message, the interface the message was received on must be known so the complete link local address with scope ID can be reconstructed.</span></span>

 

 



