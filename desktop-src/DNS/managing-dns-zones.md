---
title: Administrar Zonas DNS
description: Una zona DNS es una base de datos de entradas de RR que corresponde a parte del espacio de nombres jerárquico de DNS. Las zonas DNS se utilizan para delimitar qué servidores DNS son autoritativos para resolver consultas de resolución de nombres para una sección determinada de la jerarquía de DNS.
ms.assetid: d4aa94e0-36f7-4b97-8a0a-c677c8a826a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c4cc991821f88076d3c3e9b2bfcbddc3ab662d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777959"
---
# <a name="managing-dns-zones"></a><span data-ttu-id="baf9f-104">Administrar Zonas DNS</span><span class="sxs-lookup"><span data-stu-id="baf9f-104">Managing DNS Zones</span></span>

<span data-ttu-id="baf9f-105">Una zona DNS es una base de datos de entradas de RR que corresponde a parte del espacio de nombres jerárquico de DNS.</span><span class="sxs-lookup"><span data-stu-id="baf9f-105">A DNS zone is a database of RR entries that corresponds to part of the DNS hierarchical name space.</span></span> <span data-ttu-id="baf9f-106">Las zonas DNS se utilizan para delimitar qué servidores DNS son autoritativos para resolver consultas de resolución de nombres para una sección determinada de la jerarquía de DNS.</span><span class="sxs-lookup"><span data-stu-id="baf9f-106">DNS zones are used to delineate which DNS Servers are authoritative for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="baf9f-107">Pasos de administración</span><span class="sxs-lookup"><span data-stu-id="baf9f-107">Administration Steps</span></span>

<span data-ttu-id="baf9f-108">El proveedor WMI de DNS permite la administración de zonas DNS desde el propio servidor DNS autoritativo o desde hosts remotos.</span><span class="sxs-lookup"><span data-stu-id="baf9f-108">The DNS WMI Provider enables the administration of DNS zones from the authoritative DNS Server itself, or from remote hosts.</span></span> <span data-ttu-id="baf9f-109">Los pasos generales necesarios para administrar una zona mediante el proveedor WMI de DNS son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="baf9f-109">The general steps necessary to administer a zone using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="baf9f-110">Conexión al proveedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="baf9f-110">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="baf9f-111">Obtener una instancia de zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-111">Getting a zone instance</span></span>
-   <span data-ttu-id="baf9f-112">Enumerar o modificar una propiedad de zona, o usar un método</span><span class="sxs-lookup"><span data-stu-id="baf9f-112">Listing or modifying a zone property, or using a method</span></span>

<span data-ttu-id="baf9f-113">Las siguientes tareas están vinculadas a sus ejemplos de scripting asociados:</span><span class="sxs-lookup"><span data-stu-id="baf9f-113">The following tasks are linked to their associated scripting samples:</span></span>

-   [<span data-ttu-id="baf9f-114">Creación de una zona DNS</span><span class="sxs-lookup"><span data-stu-id="baf9f-114">Creating a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-115">Modificar una zona DNS</span><span class="sxs-lookup"><span data-stu-id="baf9f-115">Modifying a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-116">Eliminación de una zona DNS</span><span class="sxs-lookup"><span data-stu-id="baf9f-116">Deleting a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-117">Adición de una dirección IP de zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-117">Adding a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-118">Eliminación de una dirección IP de zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-118">Deleting a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-119">Pausar una zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-119">Pausing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-120">Reanudación de una zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-120">Resuming a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-121">Actualización de una zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-121">Updating a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-122">Recarga de una zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-122">Reloading a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="baf9f-123">Actualización de una zona</span><span class="sxs-lookup"><span data-stu-id="baf9f-123">Refreshing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)

 

 




