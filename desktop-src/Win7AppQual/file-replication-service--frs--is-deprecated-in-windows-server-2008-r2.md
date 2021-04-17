---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: El servicio de replicación de archivos (FRS) está en desuso en Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716130"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="0245b-103">El servicio de replicación de archivos (FRS) está en desuso en Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0245b-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="0245b-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="0245b-104">Platform</span></span>

 <span data-ttu-id="0245b-105">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0245b-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="0245b-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="0245b-106">Feature Impact</span></span>

 <span data-ttu-id="0245b-107">**Gravedad:** Calidad</span><span class="sxs-lookup"><span data-stu-id="0245b-107">**Severity -** High</span></span>  
<span data-ttu-id="0245b-108">**Frecuencia:** Calidad</span><span class="sxs-lookup"><span data-stu-id="0245b-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="0245b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0245b-109">Description</span></span>

<span data-ttu-id="0245b-110">En Windows Server 2008 R2, el servicio de replicación de archivos (FRS) no se puede usar para replicar carpetas Sistema de archivos distribuido (DFS) o datos personalizados (no SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="0245b-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="0245b-111">Un controlador de dominio de Windows Server 2008 R2 puede seguir usando FRS para replicar el contenido del recurso compartido SYSVOL en un dominio que usa FRS para replicar el recurso compartido SYSVOL entre controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="0245b-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="0245b-112">Sin embargo, los servidores de Windows Server 2008 R2 no pueden usar FRS para replicar el contenido de ningún conjunto de réplicas aparte del recurso compartido SYSVOL.</span><span class="sxs-lookup"><span data-stu-id="0245b-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="0245b-113">El servicio Replicación DFS es un sustituto de FRS y se puede usar para replicar el contenido del recurso compartido SYSVOL, carpetas DFS y otros datos personalizados (no SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="0245b-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="0245b-114">Migre todos los conjuntos de réplicas FRS que no sean de SYSVOL a Replicación DFS.</span><span class="sxs-lookup"><span data-stu-id="0245b-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="0245b-115">También se recomienda encarecidamente migrar la replicación del recurso compartido SYSVOL de FRS a Replicación DFS porque Replicación DFS es más robusta, escalable y tiene un mejor rendimiento de replicación que FRS.</span><span class="sxs-lookup"><span data-stu-id="0245b-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0245b-116">Manifestación</span><span class="sxs-lookup"><span data-stu-id="0245b-116">Manifestation</span></span>

<span data-ttu-id="0245b-117">La replicación de FRS de datos personalizados se interrumpirá de una actualización en contexto.</span><span class="sxs-lookup"><span data-stu-id="0245b-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="0245b-118">La única manera de recuperarse de esta situación sería volver a instalar un sistema operativo anterior en el servidor y reinicializar la replicación de FRS.</span><span class="sxs-lookup"><span data-stu-id="0245b-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="0245b-119">No se permite a los servidores que se han actualizado a Windows Server 2008 R2 participar en grupos de replicación FRS existentes.</span><span class="sxs-lookup"><span data-stu-id="0245b-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="0245b-120">Mitigación del impacto</span><span class="sxs-lookup"><span data-stu-id="0245b-120">Mitigation of Impact</span></span>

<span data-ttu-id="0245b-121">Para evitar problemas que pueden producirse como resultado de estos cambios, migre los conjuntos de replicación FRS personalizados a Replicación DFS.</span><span class="sxs-lookup"><span data-stu-id="0245b-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="0245b-122">El servicio Replicación DFS tiene muchas ventajas con respecto a FRS, como herramientas de administración mejoradas, mayor rendimiento y administración delegada.</span><span class="sxs-lookup"><span data-stu-id="0245b-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="0245b-123">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="0245b-123">Links to Other Resources</span></span>

-   <span data-ttu-id="0245b-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="0245b-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="0245b-125">Replicación del sistema de archivos distribuido: preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="0245b-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="0245b-126">Guía de migración de replicación de SYSVOL: Replicación de FRS a DFS</span><span class="sxs-lookup"><span data-stu-id="0245b-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
