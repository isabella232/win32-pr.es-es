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
# <a name="portal-object"></a>Objeto de portal

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de portal modela un portal iSCSI incluido en un subsistema iSCSI.

Use el método [**IVdsSubSystemIscsi:: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) para determinar los portales iSCSI del subsistema. Los llamadores pueden obtener un puntero a un portal específico seleccionando el objeto de portal deseado de la enumeración que devuelve el método **QueryPortals** . Con un objeto de portal, puede establecer el estado del portal y la consulta para las propiedades del portal, los grupos de portales asociados y el subsistema que contiene el portal.

Un objeto de portal solo se puede asociar a un grupo de portal de un destino especificado.

Los portales sirven como uno de los extremos de rutas de acceso de MPIO en proveedores de hardware iSCSI, en el que se pueden imponer las directivas de equilibrio de carga.

Las propiedades del objeto de portal incluyen un identificador de objeto, una dirección IP y un puerto, y el estado del portal.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0 | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Enumeraciones asociadas                                                                   | [**VDS \_ \_ \_ Estado del portal de iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).                                                          |
| Estructuras asociadas                                                                     | [**VDS \_ \_ \_ Propuesta del portal de iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) y [**\_ \_ notificación del puerto VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
