---
title: Limitaciones de la autenticación mutua con Kerberos
description: Tanto la cuenta del cliente como la cuenta del servicio deben estar en dominios de modo nativo o mixto de Windows 2000, ya que los servicios de Kerberos no están disponibles en los dominios de nivel inferior.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486591"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a><span data-ttu-id="5ce17-103">Limitaciones de la autenticación mutua con Kerberos</span><span class="sxs-lookup"><span data-stu-id="5ce17-103">Limitations of Mutual Authentication with Kerberos</span></span>

<span data-ttu-id="5ce17-104">Tanto la cuenta del cliente como la cuenta del servicio deben estar en dominios de modo nativo o mixto de Windows 2000, ya que los servicios de Kerberos no están disponibles en los dominios de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="5ce17-104">Both the client's account and the service's account must be in Windows 2000 native or mixed-mode domains because Kerberos services are not available in downlevel domains.</span></span> <span data-ttu-id="5ce17-105">Además, las cuentas de cliente y de servicio deben estar en el mismo bosque porque el KDC del cliente usa el catálogo global para buscar el nombre de la entidad de seguridad de servicio.</span><span class="sxs-lookup"><span data-stu-id="5ce17-105">In addition, both client and service accounts must be in the same forest because the client's KDC uses the global catalog to search for the service principal name.</span></span>

<span data-ttu-id="5ce17-106">Tanto el servicio como el cliente deben ejecutarse en Windows 2000, de lo contrario, se producirá un error en la autenticación mutua con Kerberos porque las versiones anteriores de Windows no admiten Kerberos.</span><span class="sxs-lookup"><span data-stu-id="5ce17-106">Both service and client must be running on Windows 2000, otherwise mutual authentication with Kerberos will fail because earlier versions of Windows do not support Kerberos.</span></span>

<span data-ttu-id="5ce17-107">Los nombres de entidad de seguridad de servicio deben incluir el nombre DNS del servidor host en el que se está ejecutando el servicio.</span><span class="sxs-lookup"><span data-stu-id="5ce17-107">Service principal names must include the DNS name of the host server on which the service is running.</span></span> <span data-ttu-id="5ce17-108">Debe usar el nombre DNS.</span><span class="sxs-lookup"><span data-stu-id="5ce17-108">You must use the DNS name.</span></span>

 

 




