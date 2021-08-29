---
description: Un objeto de grupo de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Storage Objeto Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee6ddd225c3c6e92f29bc4b4f338d9c3ef7ffc0cf0cc5e748d4bc71da319d19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986735"
---
# <a name="storage-pool-object"></a>Storage Objeto Pool

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de grupo de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.

Un grupo de almacenamiento contiene extensiones de unidad de una o varias unidades administradas por el mismo proveedor de hardware.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| Enumeraciones asociadas                           | [**VDS \_ TIPO \_ RAID,**](/windows/desktop/api/Vds/ne-vds-vds_raid_type) [**ESTADO DEL GRUPO DE ALMACENAMIENTO \_ \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)y [**TIPO DE GRUPO DE ALMACENAMIENTO \_ \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).                                                                                                                                  |
| Estructuras asociadas                             | [**VDS \_ HINTS2,**](/windows/desktop/api/Vds/ns-vds-vds_hints2) [**VDS \_ POOL \_ ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS \_ POOL CUSTOM \_ \_ ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS STORAGE POOL \_ DRIVE \_ \_ \_ EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)y [**VDS STORAGE POOL \_ \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop). |



 

 

 
