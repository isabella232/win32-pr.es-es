---
title: Publicación en un objeto de equipo
description: Normalmente, los servicios basados en host crean los SCP en el objeto de equipo para el equipo host. Los servicios basados en host están estrechamente relacionados con un solo equipo host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904477"
---
# <a name="publishing-under-a-computer-object"></a><span data-ttu-id="3b56c-104">Publicación en un objeto de equipo</span><span class="sxs-lookup"><span data-stu-id="3b56c-104">Publishing Under a Computer Object</span></span>

<span data-ttu-id="3b56c-105">Normalmente, los servicios basados en host crean los SCP en el objeto de equipo para el equipo host.</span><span class="sxs-lookup"><span data-stu-id="3b56c-105">Typically, host-based services create SCPs under the computer object for the host computer.</span></span> <span data-ttu-id="3b56c-106">Los servicios basados en host están estrechamente relacionados con un solo equipo host.</span><span class="sxs-lookup"><span data-stu-id="3b56c-106">Host-based services are services closely tied to a single host computer.</span></span>

<span data-ttu-id="3b56c-107">**Para crear SCP en un objeto de equipo**</span><span class="sxs-lookup"><span data-stu-id="3b56c-107">**To create SCPs under a computer object**</span></span>

1.  <span data-ttu-id="3b56c-108">Llame a la función [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) para obtener el nombre distintivo (DN) en el directorio del objeto de equipo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="3b56c-108">Call the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the distinguished name (DN) in the directory of the computer object for the local computer.</span></span>
2.  <span data-ttu-id="3b56c-109">Use ese DN para enlazar con el objeto de equipo y crear el SCP.</span><span class="sxs-lookup"><span data-stu-id="3b56c-109">Use that DN to bind to the computer object and create the SCP.</span></span>

<span data-ttu-id="3b56c-110">Para obtener más información y un ejemplo de código, vea [cómo los clientes buscan y usan un punto de conexión de servicio](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="3b56c-110">For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="3b56c-111">Tenga en cuenta que solo los equipos miembros del dominio tienen objetos de equipo válidos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="3b56c-111">Be aware that only domain-member computers have valid computer objects in the directory.</span></span>

<span data-ttu-id="3b56c-112">Para obtener el nombre DNS o NetBIOS del equipo local, llame a la función [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .</span><span class="sxs-lookup"><span data-stu-id="3b56c-112">To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span>

 

 