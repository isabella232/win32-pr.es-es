---
description: Objeto de puerto de controlador
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Objeto de puerto de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696312"
---
# <a name="controller-port-object"></a><span data-ttu-id="d730b-103">Objeto de puerto de controlador</span><span class="sxs-lookup"><span data-stu-id="d730b-103">Controller Port Object</span></span>

<span data-ttu-id="d730b-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d730b-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d730b-105">Un objeto de puerto de controlador modela un puerto de controlador en un subsistema.</span><span class="sxs-lookup"><span data-stu-id="d730b-105">A controller port object models a controller port in a subsystem.</span></span> <span data-ttu-id="d730b-106">Los equipos host pueden escribir y leer desde LUN a través de puertos de controlador.</span><span class="sxs-lookup"><span data-stu-id="d730b-106">Host computers can write to and read from LUNs through controller ports.</span></span> <span data-ttu-id="d730b-107">Los puertos de controlador están incluidos en los controladores de un subsistema.</span><span class="sxs-lookup"><span data-stu-id="d730b-107">Controller ports are contained by controllers in a subsystem.</span></span> <span data-ttu-id="d730b-108">En VDS 1,1 y VDS 2.0, cada uno de los puertos de controlador de un subsistema se establece en activo o inactivo con respecto a cada uno de los LUN que el subsistema Surfaces.</span><span class="sxs-lookup"><span data-stu-id="d730b-108">In VDS 1.1 and VDS2.0, each of a subsystem's controller ports is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span> <span data-ttu-id="d730b-109">Un puerto de un solo controlador, a continuación, se puede establecer simultáneamente en activo para un LUN e inactivo para otros.</span><span class="sxs-lookup"><span data-stu-id="d730b-109">A single controller port, then, can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="d730b-110">Un puerto de controlador que está activo para un LUN determinado conlleva la responsabilidad de controlar la entrada y la salida del LUN.</span><span class="sxs-lookup"><span data-stu-id="d730b-110">A controller port that is active for a given LUN carries responsibility for handling input to and output from the LUN.</span></span>

<span data-ttu-id="d730b-111">Los puertos de controlador activos sirven como uno de los puntos de conexión de rutas MPIO en Canal de fibra proveedores de hardware, en el que se pueden imponer las directivas de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="d730b-111">Active controller ports serve as one of the endpoints of MPIO paths in Fibre Channel hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="d730b-112">Use el método [**IVdsControllerControllerPort:: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) para determinar los puertos del controlador contenidos en un controlador específico.</span><span class="sxs-lookup"><span data-stu-id="d730b-112">Use the [**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) method to determine the controller ports that are contained by a specific controller.</span></span> <span data-ttu-id="d730b-113">Los llamadores pueden obtener un puntero a un puerto de controlador específico seleccionando el objeto de puerto del controlador deseado de la enumeración devuelta por el método **QueryControllerPorts** .</span><span class="sxs-lookup"><span data-stu-id="d730b-113">Callers can get a pointer to a specific controller port by selecting the desired controller port object from the enumeration that is returned by the **QueryControllerPorts** method.</span></span> <span data-ttu-id="d730b-114">Con un objeto de controlador, un llamador puede establecer el estado del puerto del controlador y la consulta para sus LUN asociadas.</span><span class="sxs-lookup"><span data-stu-id="d730b-114">With a controller object, a caller can set the controller port status and query for its associated LUNs.</span></span>

<span data-ttu-id="d730b-115">Las propiedades de objeto de controlador incluyen un identificador de objeto, un nombre, un número de serie y el estado del puerto del controlador.</span><span class="sxs-lookup"><span data-stu-id="d730b-115">Controller object properties include an object identifier, a name, a serial number, and the controller port status.</span></span>

<span data-ttu-id="d730b-116">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d730b-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="d730b-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="d730b-117">Type</span></span>                                                                                              | <span data-ttu-id="d730b-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="d730b-118">Element</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d730b-119">Interfaces que siempre expone este objeto en VDS 1,1 y 2,0 Canal de fibra proveedores</span><span class="sxs-lookup"><span data-stu-id="d730b-119">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="d730b-120">**IVdsControllerPort**</span><span class="sxs-lookup"><span data-stu-id="d730b-120">**IVdsControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| <span data-ttu-id="d730b-121">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="d730b-121">Associated enumerations</span></span>                                                                           | [<span data-ttu-id="d730b-122">**\_Estado del puerto VDS \_**</span><span class="sxs-lookup"><span data-stu-id="d730b-122">**VDS\_PORT\_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| <span data-ttu-id="d730b-123">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="d730b-123">Associated structures</span></span>                                                                             | <span data-ttu-id="d730b-124">[**VDS \_ \_Expulsión de Puerto**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) y [ **\_ \_ notificación de Puerto VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span><span class="sxs-lookup"><span data-stu-id="d730b-124">[**VDS\_PORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d730b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d730b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d730b-126">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="d730b-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="d730b-127">**IVdsControllerControllerPort::QueryControllerPorts**</span><span class="sxs-lookup"><span data-stu-id="d730b-127">**IVdsControllerControllerPort::QueryControllerPorts**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
