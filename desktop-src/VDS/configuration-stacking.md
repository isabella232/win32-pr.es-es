---
description: Apilamiento de configuración
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Apilamiento de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104559528"
---
# <a name="configuration-stacking"></a><span data-ttu-id="aaab0-103">Apilamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="aaab0-103">Configuration Stacking</span></span>

<span data-ttu-id="aaab0-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aaab0-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="aaab0-105">La apilación implica la concatenación de un conjunto de asignaciones de bloques lógicos.</span><span class="sxs-lookup"><span data-stu-id="aaab0-105">Stacking involves the concatenating of a set of logical block mappings.</span></span> <span data-ttu-id="aaab0-106">Puede apilar varios LUN desde el mismo subsistema en un LUN.</span><span class="sxs-lookup"><span data-stu-id="aaab0-106">You can stack multiple LUNs from the same subsystem under one LUN.</span></span> <span data-ttu-id="aaab0-107">Puede apilar un LUN junto con volúmenes del mismo paquete en un volumen.</span><span class="sxs-lookup"><span data-stu-id="aaab0-107">You can stack a LUN together with volumes from the same pack under one volume.</span></span> <span data-ttu-id="aaab0-108">Además, puede apilar varios LUN que se exponen mediante subsistemas heterogéneos en un volumen.</span><span class="sxs-lookup"><span data-stu-id="aaab0-108">Further, you can stack multiple LUNs that are surfaced by heterogeneous subsystems under one volume.</span></span>

<span data-ttu-id="aaab0-109">Como se muestra en la siguiente ilustración, la creación de un volumen no cambia el enlace existente de un LUN contribuyente.</span><span class="sxs-lookup"><span data-stu-id="aaab0-109">As the following illustration shows, the creating of a volume does not change the existing binding of a contributing LUN.</span></span> <span data-ttu-id="aaab0-110">De forma similar, al Desenlazar un volumen no se deshace el enlace de un LUN contribuyente.</span><span class="sxs-lookup"><span data-stu-id="aaab0-110">Similarly, the unbinding of a volume does not unbind a contributing LUN.</span></span> <span data-ttu-id="aaab0-111">En la ilustración se muestra la configuración de RAID 0 1 (0 + 1).</span><span class="sxs-lookup"><span data-stu-id="aaab0-111">The illustration depicts the RAID 0 1 (0+1) configuration.</span></span> <span data-ttu-id="aaab0-112">Esta configuración conocida combina el seccionamiento (RAID 0) y la creación de reflejo (RAID 1), que empareja el acceso rápido a los datos de RAID 0 con la confiabilidad de RAID 1.</span><span class="sxs-lookup"><span data-stu-id="aaab0-112">This well-known configuration combines striping (RAID 0) and mirroring (RAID 1), which pairs the fast data access of RAID 0 with the reliability of RAID 1.</span></span>

![Diagrama que muestra una configuración de RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

<span data-ttu-id="aaab0-114">Los LUN de contribución pueden tener tipos de enlace diferentes.</span><span class="sxs-lookup"><span data-stu-id="aaab0-114">Contributing LUNs can have different binding types.</span></span> <span data-ttu-id="aaab0-115">Hay muchas configuraciones posibles con VDS, pero son muy poco probables, como la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="aaab0-115">Many configurations are possible with VDS but are highly unlikely, such as the next illustration.</span></span> <span data-ttu-id="aaab0-116">En este ejemplo, un Plex de volumen es un LUN seccionado y el otro es un LUN reflejado de tres vías.</span><span class="sxs-lookup"><span data-stu-id="aaab0-116">In this example, one volume plex is a striped LUN and the other is a three-way mirrored LUN.</span></span>

![Diagrama que muestra una configuración de VDS en la que un Plex de volumen es un LUN seccionado y el otro es un LUN reflejado de 3 vías.](images/vdsstacklunvol.png)

<span data-ttu-id="aaab0-118">Aunque no es práctico, este ejemplo muestra un aspecto importante del apilamiento.</span><span class="sxs-lookup"><span data-stu-id="aaab0-118">Although impractical, this example illustrates an important aspect of stacking.</span></span> <span data-ttu-id="aaab0-119">Dado que la apilación concatena complejos, VDS agrega los tres complejos de LUN a los dos complejos de volumen para un total de cinco complejos.</span><span class="sxs-lookup"><span data-stu-id="aaab0-119">Because stacking concatenates plexes, VDS adds the three LUN plexes to the two volume plexes for a total of five plexes.</span></span>

 

 
