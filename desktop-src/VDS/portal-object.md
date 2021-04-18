---
description: Objeto de portal
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Objeto de portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697747"
---
# <a name="portal-object"></a><span data-ttu-id="8c4a9-103">Objeto de portal</span><span class="sxs-lookup"><span data-stu-id="8c4a9-103">Portal Object</span></span>

<span data-ttu-id="8c4a9-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8c4a9-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="8c4a9-105">Un objeto de portal modela un portal iSCSI incluido en un subsistema iSCSI.</span><span class="sxs-lookup"><span data-stu-id="8c4a9-105">A portal object models an iSCSI portal that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="8c4a9-106">Use el método [**IVdsSubSystemIscsi:: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) para determinar los portales iSCSI del subsistema.</span><span class="sxs-lookup"><span data-stu-id="8c4a9-106">Use the [**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) method to determine the iSCSI portals of the subsystem.</span></span> <span data-ttu-id="8c4a9-107">Los llamadores pueden obtener un puntero a un portal específico seleccionando el objeto de portal deseado de la enumeración que devuelve el método **QueryPortals** .</span><span class="sxs-lookup"><span data-stu-id="8c4a9-107">Callers can get a pointer to a specific portal by selecting the desired portal object from the enumeration that is returned by the **QueryPortals** method.</span></span> <span data-ttu-id="8c4a9-108">Con un objeto de portal, puede establecer el estado del portal y la consulta para las propiedades del portal, los grupos de portales asociados y el subsistema que contiene el portal.</span><span class="sxs-lookup"><span data-stu-id="8c4a9-108">With a portal object, you can set the portal status and query for portal properties, associated portal groups, and the subsystem that contains the portal.</span></span>

<span data-ttu-id="8c4a9-109">Un objeto de portal solo se puede asociar a un grupo de portal de un destino especificado.</span><span class="sxs-lookup"><span data-stu-id="8c4a9-109">A portal object can only be associated with at most one portal group of a specified target.</span></span>

<span data-ttu-id="8c4a9-110">Los portales sirven como uno de los extremos de rutas de acceso de MPIO en proveedores de hardware iSCSI, en el que se pueden imponer las directivas de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="8c4a9-110">Portals serve as one of the endpoints of MPIO paths in iSCSI hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="8c4a9-111">Las propiedades del objeto de portal incluyen un identificador de objeto, una dirección IP y un puerto, y el estado del portal.</span><span class="sxs-lookup"><span data-stu-id="8c4a9-111">Portal object properties include an object identifier, an IP address and port, and the portal status.</span></span>

<span data-ttu-id="8c4a9-112">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8c4a9-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="8c4a9-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c4a9-113">Type</span></span>                                                                                      | <span data-ttu-id="8c4a9-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c4a9-114">Element</span></span>                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4a9-115">Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0</span><span class="sxs-lookup"><span data-stu-id="8c4a9-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="8c4a9-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span><span class="sxs-lookup"><span data-stu-id="8c4a9-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span></span>                                                                             |
| <span data-ttu-id="8c4a9-117">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="8c4a9-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="8c4a9-118">[**VDS \_ \_ \_ Estado del portal de iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span><span class="sxs-lookup"><span data-stu-id="8c4a9-118">[**VDS\_ISCSI\_PORTAL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span></span>                                                          |
| <span data-ttu-id="8c4a9-119">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="8c4a9-119">Associated structures</span></span>                                                                     | <span data-ttu-id="8c4a9-120">[**VDS \_ \_ \_ Propuesta del portal de iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) y [**\_ \_ notificación del puerto VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span><span class="sxs-lookup"><span data-stu-id="8c4a9-120">[**VDS\_ISCSI\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8c4a9-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c4a9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c4a9-122">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="8c4a9-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="8c4a9-123">**IVdsSubSystemIscsi::QueryPortals**</span><span class="sxs-lookup"><span data-stu-id="8c4a9-123">**IVdsSubSystemIscsi::QueryPortals**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
