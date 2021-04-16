---
description: Un objeto de bloque de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Objeto de bloque de almacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678421"
---
# <a name="storage-pool-object"></a>Objeto de bloque de almacenamiento

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de bloque de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.

Un grupo de almacenamiento contiene extensiones de unidad de una o varias unidades administradas por el mismo proveedor de hardware.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| Enumeraciones asociadas                           | [**VDS \_ \_Tipo de RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ \_ \_ Estado del grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)y [**\_ \_ \_ tipo de grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).                                                                                                                                  |
| Estructuras asociadas                             | [**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ atributos de grupo de VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ atributos personalizados del grupo de VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ extensión de unidad del grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)y [**\_ \_ \_ Prop del grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop). |



 

 

 
