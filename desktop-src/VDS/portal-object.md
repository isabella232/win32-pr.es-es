---
description: Objeto del portal
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Objeto del portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7004f648b11b16c8c6279a0a74bae775fa539d8f0a93fc83d7effccea68915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864525"
---
# <a name="portal-object"></a>Objeto del portal

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de portal modela un portal iSCSI que se encuentra dentro de un subsistema iSCSI.

Use el [**método IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) para determinar los portales iSCSI del subsistema. Los llamadores pueden obtener un puntero a un portal específico seleccionando el objeto de portal deseado de la enumeración que devuelve el **método QueryPortals.** Con un objeto de portal, puede establecer el estado del portal y consultar las propiedades del portal, los grupos del portal asociados y el subsistema que contiene el portal.

Un objeto de portal solo se puede asociar a un grupo de portal de un destino especificado como máximo.

Los portales sirven como uno de los puntos de conexión de las rutas de acceso de MPIO en los proveedores de hardware iSCSI, en los que se pueden imponer directivas de equilibrio de carga.

Las propiedades del objeto del portal incluyen un identificador de objeto, una dirección IP y un puerto, y el estado del portal.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en proveedores de iSCSI VDS 1.1 y 2.0 | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Enumeraciones asociadas                                                                   | [**VDS \_ ESTADO DEL \_ PORTAL \_ ISCSI.**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status)                                                          |
| Estructuras asociadas                                                                     | [**VDS \_ ISCSI \_ PORTAL \_ PROP y**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) [**VDS PORT \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
