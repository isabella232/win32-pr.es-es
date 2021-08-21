---
description: Objeto de grupo del portal
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Objeto de grupo del portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1021d74a3c8a6a612372db56952be1dabe5380e8e4a49b1b83c5ae2fe54754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057963"
---
# <a name="portal-group-object"></a>Objeto de grupo del portal

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de grupo de portal modela un grupo de portales iSCSI que se encuentra dentro de un destino iSCSI.

Use el [**método IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) para determinar los grupos del portal contenidos por un destino específico. Use el [**método IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) para determinar los grupos del portal asociados a un portal especificado. Los llamadores pueden obtener un puntero a un grupo de portal específico seleccionando el objeto de grupo de portal deseado de la enumeración que devuelve el método **QueryPortalGroups** o el método **QueryAssociatedPortalGroups.** Con un objeto de grupo del portal, puede agregar o quitar portales y consultar las propiedades del grupo del portal, los portales asociados y el destino que contiene el grupo del portal.

Las propiedades del objeto de grupo del portal incluyen un [identificador de objeto](vds-data-types.md) y la etiqueta de grupo del portal. Para obtener más información sobre las etiquetas de grupo del portal, consulte la especificación de iSCSI en <https://go.microsoft.com/fwlink/p/?linkid=158752> .

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en proveedores de iSCSI VDS 1.1 y 2.0 | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Enumeraciones asociadas                                                                   | Ninguno.                                                                                                                                              |
| Estructuras asociadas                                                                     | [**VDS \_ ISCSI \_ PORTALGROUP \_ PROP y**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) [**VDS PORTAL GROUP \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
