---
description: Drive (objeto)
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Drive (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276983"
---
# <a name="drive-object"></a>Drive (objeto)

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de unidad modela una unidad de disco física incluida en un subsistema. Cada unidad se conecta a un bus, ocupa una ranura y contiene un conjunto de extensiones de unidad. Cada unidad puede aportar extensiones a cualquier número de LUN. También se puede designar una unidad como reserva activa.

Use el método [**IVdsSubSystem:: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) para determinar las unidades que contiene un subsistema específico. Los llamadores pueden obtener un puntero a una unidad específica seleccionando el objeto de unidad deseado de la enumeración devuelta por el método **QueryDrives** o invocando el método [**IVdsSubSystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) y pasando el bus y el número de ranura deseados. Con un objeto de unidad, puede establecer el estado de la unidad y la consulta de las propiedades de la unidad, las extensiones de unidad asociadas y el subsistema que contiene la unidad.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades de objeto de unidad incluyen el estado de la unidad, el estado y las marcas; tamaño en bytes; y un número de bus y ranura.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Interfaces que puede exponer este objeto     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Enumeraciones asociadas                           | [**VDS \_ \_Marca de unidad**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ Estado de unidad de VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)y [**\_ \_ extensión de unidad de VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Estructuras asociadas                             | [**VDS \_ GENERAR \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) una [**notificación de \_ unidad \_ de disco**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)y de Prop.                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
