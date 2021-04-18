---
description: Objeto de grupo de portal
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Objeto de grupo de portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546894"
---
# <a name="portal-group-object"></a><span data-ttu-id="df275-103">Objeto de grupo de portal</span><span class="sxs-lookup"><span data-stu-id="df275-103">Portal Group Object</span></span>

<span data-ttu-id="df275-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="df275-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="df275-105">Un objeto de grupo de portal modela un grupo de portales iSCSI que se encuentra dentro de un destino iSCSI.</span><span class="sxs-lookup"><span data-stu-id="df275-105">A portal group object models an iSCSI portal group that is contained within an iSCSI target.</span></span>

<span data-ttu-id="df275-106">Use el método [**IVdsIscsiTarget:: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) para determinar los grupos de portal contenidos en un destino concreto.</span><span class="sxs-lookup"><span data-stu-id="df275-106">Use the [**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) method to determine the portal groups that are contained by a specific target.</span></span> <span data-ttu-id="df275-107">Use el método [**IVdsIscsiPortal:: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) para determinar los grupos de portal que están asociados a un portal especificado.</span><span class="sxs-lookup"><span data-stu-id="df275-107">Use the [**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) method to determine the portal groups that are associated with a specified portal.</span></span> <span data-ttu-id="df275-108">Los llamadores pueden obtener un puntero a un grupo de portal específico seleccionando el objeto de grupo de portal deseado de la enumeración que devuelve el método **QueryPortalGroups** o el método **QueryAssociatedPortalGroups** .</span><span class="sxs-lookup"><span data-stu-id="df275-108">Callers can get a pointer to a specific portal group by selecting the desired portal group object from the enumeration that is returned by the **QueryPortalGroups** method or the **QueryAssociatedPortalGroups** method.</span></span> <span data-ttu-id="df275-109">Con un objeto de grupo de portal, puede Agregar o quitar portales y consultas de propiedades de grupo de portal, portales asociados y el destino que contiene el grupo de portal.</span><span class="sxs-lookup"><span data-stu-id="df275-109">With a portal group object, you can add or remove portals and query for portal group properties, associated portals, and the target that contains the portal group.</span></span>

<span data-ttu-id="df275-110">Las propiedades del objeto de grupo del portal incluyen un [identificador de objeto](vds-data-types.md) y la etiqueta del grupo de portal.</span><span class="sxs-lookup"><span data-stu-id="df275-110">Portal group object properties include an [object identifier](vds-data-types.md) and the portal group tag.</span></span> <span data-ttu-id="df275-111">Para obtener más información acerca de las etiquetas de grupo de portal, consulte la especificación iSCSI en <https://go.microsoft.com/fwlink/p/?linkid=158752> .</span><span class="sxs-lookup"><span data-stu-id="df275-111">For more information about portal group tags, see the iSCSI specification at <https://go.microsoft.com/fwlink/p/?linkid=158752>.</span></span>

<span data-ttu-id="df275-112">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="df275-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="df275-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="df275-113">Type</span></span>                                                                                      | <span data-ttu-id="df275-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="df275-114">Element</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df275-115">Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0</span><span class="sxs-lookup"><span data-stu-id="df275-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="df275-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span><span class="sxs-lookup"><span data-stu-id="df275-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span></span>                                                                                              |
| <span data-ttu-id="df275-117">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="df275-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="df275-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df275-118">None.</span></span>                                                                                                                                              |
| <span data-ttu-id="df275-119">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="df275-119">Associated structures</span></span>                                                                     | <span data-ttu-id="df275-120">[**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) Notificación de grupo de [**\_ portal de \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)y PORTALGROUP de iSCSI.</span><span class="sxs-lookup"><span data-stu-id="df275-120">[**VDS\_ISCSI\_PORTALGROUP\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) and [**VDS\_PORTAL\_GROUP\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="df275-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df275-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df275-122">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="df275-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="df275-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="df275-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[<span data-ttu-id="df275-124">**IVdsIscsiTarget::QueryPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="df275-124">**IVdsIscsiTarget::QueryPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
