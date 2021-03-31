---
description: Información general de configuración
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Información general de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001074"
---
# <a name="configuration-overview"></a><span data-ttu-id="f13f8-103">Información general de configuración</span><span class="sxs-lookup"><span data-stu-id="f13f8-103">Configuration Overview</span></span>

<span data-ttu-id="f13f8-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f13f8-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="f13f8-105">Si no está familiarizado con los objetos definidos por VDS, consulte el modelo de [objetos de VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="f13f8-105">If you are unfamiliar with the objects that are defined by VDS, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="f13f8-106">La complejidad de la configuración de un disco virtual puede variar de muy fácil a ajustar.</span><span class="sxs-lookup"><span data-stu-id="f13f8-106">The configuration complexity of a virtual disk can range from very simple to finely tuned.</span></span> <span data-ttu-id="f13f8-107">Los discos virtuales de empresa, sin necesidad de asistencia y de asistencia médica, definen tres perspectivas de configuración típicas.</span><span class="sxs-lookup"><span data-stu-id="f13f8-107">No-care, free-from-care, and enterprise virtual disks define three typical configuration perspectives.</span></span> <span data-ttu-id="f13f8-108">Cada perspectiva presenta requisitos ligeramente diferentes:</span><span class="sxs-lookup"><span data-stu-id="f13f8-108">Each perspective presents somewhat different requirements:</span></span>

-   <span data-ttu-id="f13f8-109">Los discos virtuales sin asistencia se configuran de manera ligera, quizás solo para automatizar la creación de particiones y el formato de discos nuevos, o para crear temporalmente un volumen reflejado para migrar datos de un disco a otro sin tiempo de inactividad.</span><span class="sxs-lookup"><span data-stu-id="f13f8-109">No-care virtual disks are lightly configured, perhaps only to automate the partitioning and formatting of new disks, or to temporarily create a mirrored volume for migrating data from one disk to another without downtime.</span></span> <span data-ttu-id="f13f8-110">Estos discos son buenos para equipos portátiles y otros sistemas con uno o varios discos.</span><span class="sxs-lookup"><span data-stu-id="f13f8-110">Such disks are good for notebook computers and other systems with one or a few disks.</span></span>
-   <span data-ttu-id="f13f8-111">Los discos virtuales gratuitos proporcionan almacenamiento que aparece autoconfigurable, recuperación automática y disponible; usa volúmenes seccionados y LUN para lograr un mejor rendimiento; utiliza volúmenes reflejados y LUN para lograr una mejor disponibilidad. y usa los paquetes para que los modos de error se limpien y contengan.</span><span class="sxs-lookup"><span data-stu-id="f13f8-111">Free-from-care virtual disks provide storage that appears self-configuring, self-healing, and available; uses striped volumes and LUNs to achieve better performance; uses mirrored volumes and LUNs to achieve better availability; and uses packs to make the failure modes clean and contained.</span></span> <span data-ttu-id="f13f8-112">Este nivel de configuración es ideal cuando se reemplazan los discos del sistema antiguos, pequeños y lentos con discos nuevos, grandes y rápidos.</span><span class="sxs-lookup"><span data-stu-id="f13f8-112">This configuration level is ideal when replacing old, small, slow system disks with new, large, fast disks is routine.</span></span> <span data-ttu-id="f13f8-113">También es ideal para la creación de reflejo de datos con la reserva activa automatizada: un único eje de reserva puede proteger muchos ejes.</span><span class="sxs-lookup"><span data-stu-id="f13f8-113">It is also ideal for mirroring data with automated hot sparing—a single spare spindle can protect many spindles.</span></span> <span data-ttu-id="f13f8-114">Para obtener más información, consulte [reserva activa](hot-sparing.md).</span><span class="sxs-lookup"><span data-stu-id="f13f8-114">For details, see [Hot Sparing](hot-sparing.md).</span></span>

    <span data-ttu-id="f13f8-115">Las San a pequeña escala dependen de la flexibilidad y la automatización que ofrece este nivel de configuración, al igual que los dispositivos de almacenamiento conectado a la red (NAS).</span><span class="sxs-lookup"><span data-stu-id="f13f8-115">Small-scale SANs depend on the flexibility and automation that is offered by this configuration level, as do Network Attached Storage (NAS) appliances.</span></span> <span data-ttu-id="f13f8-116">Los discos virtuales gratuitos de asistencia simplifican la tarea de consolidar el almacenamiento de aplicaciones, por ejemplo, el almacenamiento de SQL y Exchange, sin consolidar los servidores.</span><span class="sxs-lookup"><span data-stu-id="f13f8-116">Free-from-care virtual disks simplify the task of consolidating application storage—for example, the storage for SQL and Exchange—without consolidating the servers.</span></span>

-   <span data-ttu-id="f13f8-117">Los discos virtuales de empresa contienen configuraciones empresariales muy grandes o complejas con requisitos adicionales específicos del sitio o específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f13f8-117">Enterprise virtual disks contain very large or complex enterprise configurations with additional site-specific or application-specific requirements.</span></span> <span data-ttu-id="f13f8-118">Los administradores ajustan el subsistema de almacenamiento para una aplicación única que podría ejecutarse solo con poca frecuencia, como un trabajo de informes de Batch mensual en un sistema de transacciones que toma un pedido.</span><span class="sxs-lookup"><span data-stu-id="f13f8-118">Administrators tune the storage subsystem for a single application that might run only infrequently, such as a monthly batch reporting job on an order-taking transaction system.</span></span> <span data-ttu-id="f13f8-119">Los discos virtuales empresariales deben escalarse, Mostrar la actividad en tiempo real del subsistema de almacenamiento y cumplir los requisitos de los administradores prácticos.</span><span class="sxs-lookup"><span data-stu-id="f13f8-119">Enterprise virtual disks must scale, show the real-time activity of the storage subsystem, and satisfy the requirements of hands-on administrators.</span></span>

<span data-ttu-id="f13f8-120">Para obtener más información acerca de los reflejos, las franjas y las demás opciones de configuración de VDS, consulte [enlace de volumen y LUN](volume-and-lun-binding.md).</span><span class="sxs-lookup"><span data-stu-id="f13f8-120">For additional information about mirrors, stripes, and the other configuration options in VDS, see [Volume and LUN Binding](volume-and-lun-binding.md).</span></span> <span data-ttu-id="f13f8-121">Una técnica de configuración avanzada, denominada apilamiento, le permite combinar las configuraciones que están asociadas a volúmenes y LUN existentes.</span><span class="sxs-lookup"><span data-stu-id="f13f8-121">An advanced configuration technique, called stacking, enables you to combine the configurations that are associated with existing volumes and LUNs.</span></span> <span data-ttu-id="f13f8-122">Para obtener más información, consulte [Stacking de configuración](configuration-stacking.md).</span><span class="sxs-lookup"><span data-stu-id="f13f8-122">For details, see [Configuration Stacking](configuration-stacking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f13f8-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f13f8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f13f8-124">Servicio de disco virtual</span><span class="sxs-lookup"><span data-stu-id="f13f8-124">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="f13f8-125">Modelo de objetos de VDS</span><span class="sxs-lookup"><span data-stu-id="f13f8-125">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="f13f8-126">Reserva activa</span><span class="sxs-lookup"><span data-stu-id="f13f8-126">Hot Sparing</span></span>](hot-sparing.md)
</dt> <dt>

[<span data-ttu-id="f13f8-127">Enlace de volúmenes y LUN</span><span class="sxs-lookup"><span data-stu-id="f13f8-127">Volume and LUN Binding</span></span>](volume-and-lun-binding.md)
</dt> <dt>

[<span data-ttu-id="f13f8-128">Apilamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="f13f8-128">Configuration Stacking</span></span>](configuration-stacking.md)
</dt> </dl>

 

 
