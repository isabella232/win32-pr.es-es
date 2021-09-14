---
description: Objeto de unidad
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Objeto de unidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890401"
---
# <a name="drive-object"></a>Objeto de unidad

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de unidad modela una unidad de disco físico que se encuentra dentro de un subsistema. Cada unidad se conecta a un bus, ocupa una ranura y contiene un conjunto de extensiones de unidad. Cada unidad puede contribuir con extensiones a cualquier número de LUN. Una unidad también se puede designar como reserva de acceso rápido.

Use el [**método IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) para determinar las unidades contenidas en un subsistema específico. Los llamadores pueden obtener un puntero a una unidad específica seleccionando el objeto de unidad deseado de la enumeración que devuelve el método **QueryDrives,** o invocando el método [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) y pasando el número de bus y ranura deseado. Con un objeto de unidad, puede establecer el estado de la unidad y consultar las propiedades de la unidad, las extensiones de unidad asociadas y el subsistema que contiene la unidad.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto de unidad incluyen el estado de la unidad, el estado y las marcas. el tamaño en bytes; y un número de bus y ranura.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Interfaces que puede exponer este objeto     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Enumeraciones asociadas                           | [**VDS \_ MARCA \_ DE UNIDAD,**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) [**ESTADO DE UNIDAD \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)y [**EXTENSIÓN DE UNIDAD \_ \_ VDS.**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent) |
| Estructuras asociadas                             | [**VDS \_ DRIVE \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) y [**VDS DRIVE \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
