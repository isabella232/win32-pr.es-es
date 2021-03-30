---
description: Los programadores y administradores del sistema utilizan programas de configuración de servicio para modificar o consultar la base de datos de servicios instalados.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programas de configuración de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154136"
---
# <a name="service-configuration-programs"></a><span data-ttu-id="5103b-103">Programas de configuración de servicio</span><span class="sxs-lookup"><span data-stu-id="5103b-103">Service Configuration Programs</span></span>

<span data-ttu-id="5103b-104">Los programadores y administradores del sistema utilizan programas de configuración de servicio para modificar o consultar la base de datos de servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="5103b-104">Programmers and system administrators use service configuration programs to modify or query the database of installed services.</span></span> <span data-ttu-id="5103b-105">También se puede tener acceso a la base de datos mediante las funciones del registro.</span><span class="sxs-lookup"><span data-stu-id="5103b-105">The database can also be accessed by using the registry functions.</span></span> <span data-ttu-id="5103b-106">Sin embargo, solo debe usar las funciones de configuración de SCM, que garantizan que el servicio esté correctamente instalado y configurado.</span><span class="sxs-lookup"><span data-stu-id="5103b-106">However, you should only use the SCM configuration functions, which ensure that the service is properly installed and configured.</span></span>

<span data-ttu-id="5103b-107">Las funciones de configuración de SCM requieren un identificador a un objeto SCManager o un identificador a un objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="5103b-107">The SCM configuration functions require either a handle to an SCManager object or a handle to a service object.</span></span> <span data-ttu-id="5103b-108">Para obtener estos identificadores, el programa de configuración del servicio debe:</span><span class="sxs-lookup"><span data-stu-id="5103b-108">To obtain these handles, the service configuration program must:</span></span>

1.  <span data-ttu-id="5103b-109">Utilice la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obtener un identificador de la base de datos SCM en un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="5103b-109">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="5103b-110">Utilice la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) o [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obtener un identificador para el objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="5103b-110">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="5103b-111">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="5103b-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="5103b-112">Instalación, eliminación y enumeración del servicio</span><span class="sxs-lookup"><span data-stu-id="5103b-112">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
-   [<span data-ttu-id="5103b-113">Configuración de servicio</span><span class="sxs-lookup"><span data-stu-id="5103b-113">Service Configuration</span></span>](service-configuration.md)
-   [<span data-ttu-id="5103b-114">Configuración de un servicio mediante SC</span><span class="sxs-lookup"><span data-stu-id="5103b-114">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)

 

 



