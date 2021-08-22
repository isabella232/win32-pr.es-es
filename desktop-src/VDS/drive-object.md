---
description: Objeto de unidad
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Objeto de unidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04ec68fab408c4ed6412990296c0ebb265b8c3e4c4c9b05645b1f4bd1e625fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603425"
---
# <a name="drive-object"></a>Objeto de unidad

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de unidad modela una unidad de disco físico que se encuentra dentro de un subsistema. Cada unidad se conecta a un bus, ocupa una ranura y contiene un conjunto de extensiones de unidad. Cada unidad puede contribuir con extensiones a cualquier número de LUN. Una unidad también se puede designar como reserva de acceso rápido.

Use el [**método IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) para determinar las unidades contenidas en un subsistema específico. Los llamadores pueden obtener un puntero a una unidad específica seleccionando el objeto de unidad deseado de la enumeración devuelta por el método **QueryDrives,** o invocando el método [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) y pasando el número de bus y ranura deseado. Con un objeto de unidad, puede establecer el estado de la unidad y consultar las propiedades de la unidad, las extensiones de unidad asociadas y el subsistema que contiene la unidad.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto de unidad incluyen el estado de la unidad, el estado y las marcas. el tamaño en bytes; y un número de bus y ranura.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Interfaces que puede exponer este objeto     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Enumeraciones asociadas                           | [**VDS \_ MARCA \_ DE UNIDAD,**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) [**ESTADO DE UNIDAD \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)y [**EXTENSIÓN DE UNIDAD \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Estructuras asociadas                             | [**VDS \_ DRIVE \_ PROP y**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) [**VDS DRIVE \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
