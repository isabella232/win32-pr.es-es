---
description: Describe un disco duro, la creación de particiones y el registro de arranque maestro.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Dispositivos y particiones de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562601"
---
# <a name="disk-devices-and-partitions"></a><span data-ttu-id="80d3e-103">Dispositivos y particiones de disco</span><span class="sxs-lookup"><span data-stu-id="80d3e-103">Disk Devices and Partitions</span></span>

<span data-ttu-id="80d3e-104">Un disco duro se compone de un conjunto de discos apilados, cada uno de los cuales tiene datos almacenados de forma magnética en círculos concéntricos o *pistas*.</span><span class="sxs-lookup"><span data-stu-id="80d3e-104">A hard disk consists of a set of stacked platters, each of which has data stored electromagnetically in concentric circles, or *tracks*.</span></span> <span data-ttu-id="80d3e-105">Cada platter tiene dos cabezas, una en cada lado del platter, que lee o escribe datos a medida que el disco gira.</span><span class="sxs-lookup"><span data-stu-id="80d3e-105">Each platter has two heads, one on each side of the platter, that reads or writes data as the disk spins.</span></span> <span data-ttu-id="80d3e-106">Una *unidad de disco duro* controla el posicionamiento, la lectura y la escritura del disco duro.</span><span class="sxs-lookup"><span data-stu-id="80d3e-106">A *hard disk drive* controls the positioning, reading, and writing of the hard disk.</span></span> <span data-ttu-id="80d3e-107">Tenga en cuenta que los encabezados de todos los Platters están colocados como una unidad.</span><span class="sxs-lookup"><span data-stu-id="80d3e-107">Note that the heads of all platters are positioned as a unit.</span></span>

<span data-ttu-id="80d3e-108">La unidad más pequeña direccionable de una pista es un *sector*.</span><span class="sxs-lookup"><span data-stu-id="80d3e-108">The smallest addressable unit of a track is a *sector*.</span></span> <span data-ttu-id="80d3e-109">Un *cilindro* se define como el conjunto de pistas que aparecen en la misma ubicación en cada platter.</span><span class="sxs-lookup"><span data-stu-id="80d3e-109">A *cylinder* is defined as the set of tracks that appear in the same location on each platter.</span></span> <span data-ttu-id="80d3e-110">Por ejemplo, en el diagrama siguiente se muestra un disco duro con cuatro platters.</span><span class="sxs-lookup"><span data-stu-id="80d3e-110">For example, the following diagram shows a hard disk with four platters.</span></span> <span data-ttu-id="80d3e-111">El cilindro X está formado por ocho pistas (pista X desde cada lado de cada platter).</span><span class="sxs-lookup"><span data-stu-id="80d3e-111">Cylinder X consists of eight tracks (track X from each side of each platter).</span></span>

![disco duro, incluidos pistas, sectores y platters](images/diskdevice.png)

<span data-ttu-id="80d3e-113">Un disco duro puede contener una o varias regiones lógicas denominadas *particiones*.</span><span class="sxs-lookup"><span data-stu-id="80d3e-113">A hard disk can contain one or more logical regions called *partitions*.</span></span> <span data-ttu-id="80d3e-114">Las particiones se crean cuando el usuario da formato a un disco duro como *disco básico*.</span><span class="sxs-lookup"><span data-stu-id="80d3e-114">Partitions are created when the user formats a hard disk as a *basic disk*.</span></span> <span data-ttu-id="80d3e-115">Windows también admite *discos dinámicos*, que no se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="80d3e-115">Windows also supports *dynamic disks*, which are not discussed in this topic.</span></span> <span data-ttu-id="80d3e-116">Para obtener más información acerca de los discos básicos y los discos dinámicos, consulte [discos básicos y dinámicos](basic-and-dynamic-disks.md).</span><span class="sxs-lookup"><span data-stu-id="80d3e-116">For more information about basic disks and dynamic disks, see [Basic and Dynamic Disks](basic-and-dynamic-disks.md).</span></span>

<span data-ttu-id="80d3e-117">La creación de varias particiones en un disco permite la aparición de unidades de disco duro independientes.</span><span class="sxs-lookup"><span data-stu-id="80d3e-117">The creation of multiple partitions on a disk allows the appearance of having separate hard drives.</span></span> <span data-ttu-id="80d3e-118">Por ejemplo, un sistema con un disco duro que tiene una partición contiene un solo volumen, designado por el sistema como la unidad C. Un sistema con un disco duro con dos particiones normalmente contiene las unidades C y D. Tener varias particiones en un disco duro puede facilitar la administración del sistema, por ejemplo, para organizar archivos o para admitir varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="80d3e-118">For example, a system with one hard disk that has one partition contains a single volume, designated by the system as drive C. A system with a hard disk with two partitions typically contains drives C and D. Having multiple partitions on a hard disk can make it easier to manage the system, for example to organize files or to support multiple users.</span></span>

<span data-ttu-id="80d3e-119">El primer sector físico de un disco básico contiene una estructura de datos conocida como registro de arranque maestro (MBR).</span><span class="sxs-lookup"><span data-stu-id="80d3e-119">The first physical sector on a basic disk contains a data structure known as the Master Boot Record (MBR).</span></span> <span data-ttu-id="80d3e-120">El MBR contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="80d3e-120">The MBR contains the following:</span></span>

-   <span data-ttu-id="80d3e-121">Un programa de arranque (hasta 442 bytes de tamaño)</span><span class="sxs-lookup"><span data-stu-id="80d3e-121">A boot program (up to 442 bytes in size)</span></span>
-   <span data-ttu-id="80d3e-122">Una firma de disco (un número de 4 bytes único)</span><span class="sxs-lookup"><span data-stu-id="80d3e-122">A disk signature (a unique 4-byte number)</span></span>
-   <span data-ttu-id="80d3e-123">Una tabla de particiones (hasta cuatro entradas)</span><span class="sxs-lookup"><span data-stu-id="80d3e-123">A partition table (up to four entries)</span></span>
-   <span data-ttu-id="80d3e-124">Un marcador de fin de MBR (siempre 0x55AA)</span><span class="sxs-lookup"><span data-stu-id="80d3e-124">An end-of-MBR marker (always 0x55AA)</span></span>

## <a name="related-topics"></a><span data-ttu-id="80d3e-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80d3e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d3e-126">Acerca de la administración de volúmenes</span><span class="sxs-lookup"><span data-stu-id="80d3e-126">About Volume Management</span></span>](about-volume-management.md)
</dt> <dt>

[<span data-ttu-id="80d3e-127">Discos básicos y dinámicos</span><span class="sxs-lookup"><span data-stu-id="80d3e-127">Basic and Dynamic Disks</span></span>](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



