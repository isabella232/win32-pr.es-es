---
description: Representa la información que se mantiene en el administrador de particiones sobre un disco que forma parte de un clúster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: DISK_CLUSTER_INFO estructura (Ntdddisk. h)
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
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667485"
---
# <a name="disk_cluster_info-structure"></a>\_Estructura de información del clúster de disco \_

Representa la información que se mantiene en el administrador de particiones sobre un disco que forma parte de un clúster.

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



| Value                                                                                                                                                                                                                                                                                               | Significado                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**Disco \_ de Marca de clúster \_ \_ habilitada**</dt> <dt>1</dt> </dl>                                          | El disco se usa como parte del servicio de Cluster Server.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**Disco \_ de Marca de clúster \_ \_ CSV**</dt> <dt>2</dt> </dl>                                                      | CSVFS expone los volúmenes del disco en todos los nodos del clúster.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**Disco \_ de \_Marca \_ de clúster en \_ mantenimiento**</dt> <dt>4</dt> </dl>                    | El recurso de clúster asociado a este disco está en modo de mantenimiento.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**Disco \_ de Llegada de PNP de marca de clúster \_ \_ \_ \_ completada**</dt> <dt>8</dt> </dl> | El controlador de disco de clúster para el modo kernel (clusdisk) ha recibido la notificación de PnP de la llegada del disco.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Marcas que se están modificando en el miembro **Flags** .

</dd> <dt>

**Notificar**
</dt> <dd>

**True** para enviar una notificación de cambio de diseño; en caso contrario, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntdddisk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de administración de discos](disk-management-structures.md)
</dt> <dt>

[**\_información de \_ clúster de obtención de disco de ioctl \_ \_**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**\_ \_ \_ información del clúster de conjunto de discos ioctl \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




