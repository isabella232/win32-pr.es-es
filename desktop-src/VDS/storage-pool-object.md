---
description: Un objeto de grupo de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Storage Objeto Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890372"
---
# <a name="storage-pool-object"></a>Storage Objeto Pool

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de grupo de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.

Un grupo de almacenamiento contiene extensiones de unidad de una o varias unidades administradas por el mismo proveedor de hardware.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| Enumeraciones asociadas                           | [**VDS \_ TIPO \_ RAID,**](/windows/desktop/api/Vds/ne-vds-vds_raid_type) [**ESTADO DEL GRUPO DE ALMACENAMIENTO \_ \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)y [**TIPO DE GRUPO DE ALMACENAMIENTO \_ \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).                                                                                                                                  |
| Estructuras asociadas                             | [**VDS \_ HINTS2,**](/windows/desktop/api/Vds/ns-vds-vds_hints2) [**VDS \_ POOL \_ ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS \_ POOL CUSTOM \_ \_ ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS STORAGE POOL \_ DRIVE \_ \_ \_ EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)y [**VDS STORAGE POOL \_ \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop). |



 

 

 
