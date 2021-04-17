---
description: Objetos de proveedor de hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objetos de proveedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105697902"
---
# <a name="hardware-provider-objects"></a><span data-ttu-id="fd757-103">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="fd757-103">Hardware Provider Objects</span></span>

<span data-ttu-id="fd757-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd757-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="fd757-105">El modelo de objetos de VDS incluye un conjunto de objetos para consultar y configurar entidades de proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="fd757-105">The VDS object model includes a set of objects to query and configure hardware provider entities.</span></span> <span data-ttu-id="fd757-106">(Tenga en cuenta que, aunque VDS incluye un proveedor de software, debe adquirir un proveedor de hardware y el hardware asociado por separado para aprovechar las ventajas de los objetos de proveedor de hardware). Estos objetos de proveedor de hardware representan dispositivos físicos (como subsistemas, unidades y controladores) y dispositivos virtuales (como LUN y complejos de LUN).</span><span class="sxs-lookup"><span data-stu-id="fd757-106">(Note that while VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider objects.) These hardware provider objects represent physical devices (such as subsystems, drives, and controllers) and virtual devices (such as LUNs and LUN plexes).</span></span>

<span data-ttu-id="fd757-107">Un proveedor de hardware debe crear un objeto COM para cada dispositivo físico o virtual.</span><span class="sxs-lookup"><span data-stu-id="fd757-107">A hardware provider should create one COM object for each physical or virtual device.</span></span>

<span data-ttu-id="fd757-108">La ilustración siguiente muestra la relación entre el objeto de proveedor y el conjunto de objetos de proveedor de hardware, así como la relación entre los distintos objetos de proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="fd757-108">The illustration that follows shows the relationship between the provider object and the set of hardware provider objects, as well as the relationship between the various hardware provider objects themselves.</span></span>

![<span data-ttu-id="fd757-109">Diagrama que muestra la relación entre el ' proveedor ' y el ' subsistema ', ' controlador ', ' LUN ', ' LUN Plex ', ' Drive ' y ' eje '.</span><span class="sxs-lookup"><span data-stu-id="fd757-109">Diagram that shows the relationship between the 'Provider' and 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive', and 'Spindle'.</span></span> ](images/vdshwobjects.png)

<span data-ttu-id="fd757-110">Un objeto de proveedor puede contener cualquier número de subsistemas.</span><span class="sxs-lookup"><span data-stu-id="fd757-110">A provider object can contain any number of subsystems.</span></span> <span data-ttu-id="fd757-111">Todos los proveedores de hardware pueden administrar varias instancias del mismo modelo de subsistema.</span><span class="sxs-lookup"><span data-stu-id="fd757-111">All hardware providers are capable of managing multiple instances of the same subsystem model.</span></span> <span data-ttu-id="fd757-112">Muchos proveedores de hardware también pueden administrar varias instancias de diferentes modelos de subsistema.</span><span class="sxs-lookup"><span data-stu-id="fd757-112">Many hardware providers are also capable of managing multiple instances of different subsystem models.</span></span> <span data-ttu-id="fd757-113">Un solo equipo puede hospedar cualquier número de proveedores de hardware.</span><span class="sxs-lookup"><span data-stu-id="fd757-113">A single computer can host any number of hardware providers.</span></span>

<span data-ttu-id="fd757-114">Un objeto de subsistema puede contener cualquier número de controladores y unidades, y puede mostrar cualquier número de LUN.</span><span class="sxs-lookup"><span data-stu-id="fd757-114">A subsystem object can contain any number of controllers and drives, and can surface any number of LUNs.</span></span> <span data-ttu-id="fd757-115">Un objeto LUN se compone de al menos un Plex de LUN y cada complejo de LUN se asigna a una o más unidades, dependiendo del tipo de Plex.</span><span class="sxs-lookup"><span data-stu-id="fd757-115">A LUN object comprises of at least one LUN plex, and each LUN plex maps to one or more drives, depending on the plex type.</span></span> <span data-ttu-id="fd757-116">Los objetos de controlador pueden administrar la entrada/salida de datos para cualquier número de objetos de LUN.</span><span class="sxs-lookup"><span data-stu-id="fd757-116">Controller objects can manage data input/output for any number of LUN objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd757-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd757-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd757-118">Modelo de objetos de VDS</span><span class="sxs-lookup"><span data-stu-id="fd757-118">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
