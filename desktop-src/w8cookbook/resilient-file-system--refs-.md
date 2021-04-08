---
title: Sistema de archivos resistente
description: Sistema de archivos resistente
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104078547"
---
# <a name="resilient-file-system"></a><span data-ttu-id="a8eae-103">Sistema de archivos resistente</span><span class="sxs-lookup"><span data-stu-id="a8eae-103">Resilient file system</span></span>

## <a name="platform"></a><span data-ttu-id="a8eae-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="a8eae-104">Platform</span></span>

<span data-ttu-id="a8eae-105">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8eae-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="a8eae-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8eae-106">Description</span></span>

<span data-ttu-id="a8eae-107">El sistema de archivos resistente (ReFS) es un nuevo sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="a8eae-107">Resilient File System (ReFS) is a new local file system.</span></span> <span data-ttu-id="a8eae-108">Maximiza la disponibilidad de los datos, a pesar de los errores que históricamente podrían provocar la pérdida de datos o el tiempo de inactividad.</span><span class="sxs-lookup"><span data-stu-id="a8eae-108">It maximizes data availability, despite errors that would historically cause data loss or downtime.</span></span> <span data-ttu-id="a8eae-109">La integridad de los datos garantiza que los datos críticos para la empresa estén protegidos frente a errores y estén disponibles cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a8eae-109">Data integrity ensures that business critical data is protected from errors and available when needed.</span></span> <span data-ttu-id="a8eae-110">Su arquitectura está diseñada para proporcionar escalabilidad y rendimiento en una era de tamaños de conjunto de datos y cargas de trabajo dinámicas en constante crecimiento.</span><span class="sxs-lookup"><span data-stu-id="a8eae-110">Its architecture is designed to provide scalability and performance in an era of constantly growing data set sizes and dynamic workloads.</span></span>

<span data-ttu-id="a8eae-111">Las principales características de ReFS son:</span><span class="sxs-lookup"><span data-stu-id="a8eae-111">The key features of ReFS are:</span></span>

-   <span data-ttu-id="a8eae-112">**Integridad**: ReFS almacena datos para que estén protegidos frente a muchos de los errores comunes que pueden provocar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="a8eae-112">**Integrity**: ReFS stores data so that it is protected from many of the common errors that can cause data loss.</span></span> <span data-ttu-id="a8eae-113">Los metadatos del sistema de archivos siempre están protegidos.</span><span class="sxs-lookup"><span data-stu-id="a8eae-113">File system metadata is always protected.</span></span> <span data-ttu-id="a8eae-114">Opcionalmente, los datos de usuario se pueden proteger por volumen, por directorio o por archivo.</span><span class="sxs-lookup"><span data-stu-id="a8eae-114">Optionally, user data can be protected on a per-volume, per-directory, or per-file basis.</span></span> <span data-ttu-id="a8eae-115">Si se producen daños, ReFS puede detectar y, cuando se configuran con espacios de almacenamiento, corregir automáticamente los daños.</span><span class="sxs-lookup"><span data-stu-id="a8eae-115">If corruption occurs, ReFS can detect and, when configured with Storage Spaces, automatically correct the corruption.</span></span> <span data-ttu-id="a8eae-116">En caso de que se produzca un error del sistema, ReFS está diseñado para recuperarse rápidamente del error, sin pérdida de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8eae-116">In the event of a system error, ReFS is designed to recover from that error rapidly, with no loss of user data.</span></span>
-   <span data-ttu-id="a8eae-117">**Disponibilidad**: ReFS está diseñado para priorizar la disponibilidad de los datos.</span><span class="sxs-lookup"><span data-stu-id="a8eae-117">**Availability**: ReFS is designed to prioritize the availability of data.</span></span> <span data-ttu-id="a8eae-118">Con ReFS, si se producen daños y no puede repararse automáticamente, el proceso de recuperación en línea se localiza en el área de daños, por lo que no se requiere tiempo de inactividad del volumen.</span><span class="sxs-lookup"><span data-stu-id="a8eae-118">With ReFS, if corruption occurs, and it cannot be repaired automatically, the online salvage process is localized to the area of corruption, requiring no volume down-time.</span></span> <span data-ttu-id="a8eae-119">En Resumen, si se producen daños, ReFS permanecerá en línea.</span><span class="sxs-lookup"><span data-stu-id="a8eae-119">In short, if corruption occurs, ReFS will stay online.</span></span>
-   <span data-ttu-id="a8eae-120">**Escalabilidad**: ReFS está diseñado para los tamaños de los conjuntos de datos de hoy y los tamaños de los conjuntos de datos de mañana. está optimizado para una alta escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="a8eae-120">**Scalability**: ReFS is designed for the data set sizes of today and the data set sizes of tomorrow; it’s optimized for high scalability.</span></span>
-   <span data-ttu-id="a8eae-121">**Compatibilidad de aplicaciones**: para maximizar AppCompat, ReFS admite un subconjunto de características de NTFS más las API de Win32 que se han adoptado ampliamente.</span><span class="sxs-lookup"><span data-stu-id="a8eae-121">**App Compatibility**: To maximize AppCompat, ReFS supports a subset of NTFS features plus Win32 APIs that are widely adopted.</span></span>
-   <span data-ttu-id="a8eae-122">**Identificación de errores proactivo**: las capacidades de integridad de ReFS las aprovecha un escáner de integridad de datos (un "limpiador") que examina periódicamente el volumen, intenta identificar daños latentes y, después, desencadena de forma proactiva una reparación de los datos dañados.</span><span class="sxs-lookup"><span data-stu-id="a8eae-122">**Proactive Error Identification**: The integrity capabilities of ReFS are leveraged by a data integrity scanner (a “scrubber”) that periodically scans the volume, attempts to identify latent corruption, and then proactively triggers a repair of that corrupt data.</span></span>

## <a name="resources"></a><span data-ttu-id="a8eae-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="a8eae-123">Resources</span></span>

-   [<span data-ttu-id="a8eae-124">Publicación de blog de Windows 8: compilar el sistema de archivos de la próxima generación para Windows: ReFS</span><span class="sxs-lookup"><span data-stu-id="a8eae-124">Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS</span></span>](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [<span data-ttu-id="a8eae-125">Compatibilidad de aplicaciones y ReFS</span><span class="sxs-lookup"><span data-stu-id="a8eae-125">Application Compatibility and ReFS</span></span>](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 