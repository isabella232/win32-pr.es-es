---
description: COMREPL es una utilidad que replicará el catálogo de COM+ de un equipo de origen determinado en uno o varios equipos de destino.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: La utilidad de replicación COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000745"
---
# <a name="the-comrepl-replication-utility"></a><span data-ttu-id="ee04f-103">La utilidad de replicación COMREPL</span><span class="sxs-lookup"><span data-stu-id="ee04f-103">The COMREPL Replication Utility</span></span>

<span data-ttu-id="ee04f-104">COMREPL es una utilidad que replicará el catálogo de COM+ de un equipo de origen determinado en uno o varios equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="ee04f-104">COMREPL is a utility that will replicate the COM+ catalog from a given source computer to one or more target computers.</span></span> <span data-ttu-id="ee04f-105">Piense en el equipo de origen que representa una "configuración maestra".</span><span class="sxs-lookup"><span data-stu-id="ee04f-105">Think of the source computer representing a "master configuration."</span></span> <span data-ttu-id="ee04f-106">COMREPL se usa para replicar esta configuración maestra con el fin de mantener un conjunto de equipos configurados de forma idéntica.</span><span class="sxs-lookup"><span data-stu-id="ee04f-106">COMREPL is used to replicate this master configuration to maintain a set of identically configured computers.</span></span>

<span data-ttu-id="ee04f-107">La unidad de replicación es toda la configuración de COM+ en el equipo maestro.</span><span class="sxs-lookup"><span data-stu-id="ee04f-107">The unit of replication is the entire COM+ configuration on the master computer.</span></span> <span data-ttu-id="ee04f-108">Todas las aplicaciones COM+ del servidor principal se replican en los equipos de destino; es todo o nada.</span><span class="sxs-lookup"><span data-stu-id="ee04f-108">All COM+ applications on the master are replicated to the target computers; it's all or nothing.</span></span> <span data-ttu-id="ee04f-109">Además, todas las aplicaciones COM+ instaladas anteriormente en los equipos de destino, con la excepción de las aplicaciones COM+ preinstaladas, se eliminarán como parte del proceso de replicación.</span><span class="sxs-lookup"><span data-stu-id="ee04f-109">In addition, all COM+ applications previously installed on the target computers, with the exception of the COM+ preinstalled applications, will be deleted as part of the replication process.</span></span>

<span data-ttu-id="ee04f-110">COMREPL solo replica los datos de configuración de COM+.</span><span class="sxs-lookup"><span data-stu-id="ee04f-110">COMREPL replicates only COM+ configuration data.</span></span> <span data-ttu-id="ee04f-111">Esto incluye las aplicaciones COM+ y la configuración del equipo específico de COM+.</span><span class="sxs-lookup"><span data-stu-id="ee04f-111">This includes COM+ applications and COM+ specific computer settings.</span></span> <span data-ttu-id="ee04f-112">Microsoft Internet Information Services (IIS) tiene una utilidad similar (IISSync) que hace uso de COMREPL para replicar la configuración de IIS y COM+.</span><span class="sxs-lookup"><span data-stu-id="ee04f-112">Microsoft Internet Information Services (IIS) has a similar utility (IISSync), which makes use of COMREPL to replicate IIS and COM+ configuration.</span></span>

<span data-ttu-id="ee04f-113">Para obtener información detallada sobre cómo iniciar y usar COMREPL, vea los temas siguientes en esta sección:</span><span class="sxs-lookup"><span data-stu-id="ee04f-113">For detailed information on launching and using COMREPL, see the following topics in this section:</span></span>

-   [<span data-ttu-id="ee04f-114">Usar COMREPL</span><span class="sxs-lookup"><span data-stu-id="ee04f-114">Using COMREPL</span></span>](using-comrepl.md)
-   [<span data-ttu-id="ee04f-115">Lo que se replica</span><span class="sxs-lookup"><span data-stu-id="ee04f-115">What Gets Replicated</span></span>](what-gets-replicated.md)
-   [<span data-ttu-id="ee04f-116">Fases de replicación</span><span class="sxs-lookup"><span data-stu-id="ee04f-116">Replication Phases</span></span>](replication-phases.md)
-   [<span data-ttu-id="ee04f-117">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="ee04f-117">File Management</span></span>](file-management.md)
-   [<span data-ttu-id="ee04f-118">Registro e informes de errores</span><span class="sxs-lookup"><span data-stu-id="ee04f-118">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)

## <a name="related-topics"></a><span data-ttu-id="ee04f-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee04f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee04f-120">Crear paquetes de instalación para aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="ee04f-120">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="ee04f-121">Implementación de servidores proxy de aplicación</span><span class="sxs-lookup"><span data-stu-id="ee04f-121">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="ee04f-122">El catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="ee04f-122">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



