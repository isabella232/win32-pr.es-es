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
# <a name="portal-group-object"></a>Objeto de grupo de portal

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de grupo de portal modela un grupo de portales iSCSI que se encuentra dentro de un destino iSCSI.

Use el método [**IVdsIscsiTarget:: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) para determinar los grupos de portal contenidos en un destino concreto. Use el método [**IVdsIscsiPortal:: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) para determinar los grupos de portal que están asociados a un portal especificado. Los llamadores pueden obtener un puntero a un grupo de portal específico seleccionando el objeto de grupo de portal deseado de la enumeración que devuelve el método **QueryPortalGroups** o el método **QueryAssociatedPortalGroups** . Con un objeto de grupo de portal, puede Agregar o quitar portales y consultas de propiedades de grupo de portal, portales asociados y el destino que contiene el grupo de portal.

Las propiedades del objeto de grupo del portal incluyen un [identificador de objeto](vds-data-types.md) y la etiqueta del grupo de portal. Para obtener más información acerca de las etiquetas de grupo de portal, consulte la especificación iSCSI en <https://go.microsoft.com/fwlink/p/?linkid=158752> .

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0 | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Enumeraciones asociadas                                                                   | Ninguno.                                                                                                                                              |
| Estructuras asociadas                                                                     | [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) Notificación de grupo de [**\_ portal de \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)y PORTALGROUP de iSCSI. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
