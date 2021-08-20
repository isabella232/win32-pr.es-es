---
description: Representa información mantenida en el administrador de particiones sobre un disco que forma parte de un clúster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: DISK_CLUSTER_INFO estructura (Ntdddisk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: be4db89e888778c3d92090a32243f0203b527337b3734328a183b551a6181f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813797"
---
# <a name="disk_cluster_info-structure"></a>Estructura DE \_ INFORMACIÓN DE CLÚSTER DE \_ DISCO

Representa información mantenida en el administrador de particiones sobre un disco que forma parte de un clúster.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

El número de versión. Este valor debe establecerse en el tamaño de esta estructura.

</dd> <dt>

**Marcas**
</dt> <dd>

Combinación de marcas relacionadas con discos y clústeres.



| Valor                                                                                                                                                                                                                                                                                               | Significado                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**DISCO \_ CLUSTER \_ FLAG \_ ENABLED**</dt> <dt>1</dt> </dl>                                          | El disco se usa como parte del servicio de clúster.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**DISCO \_ CLUSTER \_ FLAG \_ CSV**</dt> <dt>2</dt> </dl>                                                      | CSVFS expone los volúmenes del disco en todos los nodos del clúster.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**DISCO \_ MARCA \_ DE CLÚSTER EN \_ \_ MANTENIMIENTO**</dt> <dt>4</dt> </dl>                    | El recurso de clúster asociado a este disco está en modo de mantenimiento.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**DISCO \_ CLUSTER \_ FLAG \_ PNP ARRIVAL \_ \_ COMPLETE**</dt> <dt>8</dt> </dl> | El controlador de disco de clúster para el modo kernel (clusdisk) ha recibido una notificación PnP de la llegada del disco.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Marcas que se modifican en el **miembro Flags.**

</dd> <dt>

**Notificar**
</dt> <dd>

**TRUE** para enviar una notificación de cambio de diseño; de lo contrario, **FALSE**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de administración de discos](disk-management-structures.md)
</dt> <dt>

[**IOCTL \_ DISK \_ GET \_ CLUSTER \_ INFO**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**INFORMACIÓN DEL \_ CLÚSTER DEL CONJUNTO DE DISCOS \_ \_ DE \_ IOCTL**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




