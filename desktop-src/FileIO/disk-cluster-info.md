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
# <a name="disk_cluster_info-structure"></a><span data-ttu-id="9273d-103">\_Estructura de información del clúster de disco \_</span><span class="sxs-lookup"><span data-stu-id="9273d-103">DISK\_CLUSTER\_INFO structure</span></span>

<span data-ttu-id="9273d-104">Representa la información que se mantiene en el administrador de particiones sobre un disco que forma parte de un clúster.</span><span class="sxs-lookup"><span data-stu-id="9273d-104">Represents information maintained on the partition manager about a disk that is part of a cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="9273d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9273d-105">Syntax</span></span>


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a><span data-ttu-id="9273d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9273d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9273d-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="9273d-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="9273d-108">El número de versión.</span><span class="sxs-lookup"><span data-stu-id="9273d-108">The version number.</span></span> <span data-ttu-id="9273d-109">Este valor debe establecerse en el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="9273d-109">This value must be set to the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="9273d-110">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="9273d-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9273d-111">Combinación de marcas relacionadas con discos y clústeres.</span><span class="sxs-lookup"><span data-stu-id="9273d-111">A combination of flags related to disks and clusters.</span></span>



| <span data-ttu-id="9273d-112">Value</span><span class="sxs-lookup"><span data-stu-id="9273d-112">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="9273d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9273d-113">Meaning</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <span data-ttu-id="9273d-114"><dt>**Disco \_ de Marca de clúster \_ \_ habilitada**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9273d-114"><dt>**DISK\_CLUSTER\_FLAG\_ENABLED**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="9273d-115">El disco se usa como parte del servicio de Cluster Server.</span><span class="sxs-lookup"><span data-stu-id="9273d-115">The disk is used as part of the cluster service.</span></span><br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <span data-ttu-id="9273d-116"><dt>**Disco \_ de Marca de clúster \_ \_ CSV**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9273d-116"><dt>**DISK\_CLUSTER\_FLAG\_CSV**</dt> <dt>2</dt></span></span> </dl>                                                      | <span data-ttu-id="9273d-117">CSVFS expone los volúmenes del disco en todos los nodos del clúster.</span><span class="sxs-lookup"><span data-stu-id="9273d-117">Volumes on the disk are exposed by CSVFS on all nodes of the cluster.</span></span><br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <span data-ttu-id="9273d-118"><dt>**Disco \_ de \_Marca \_ de clúster en \_ mantenimiento**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9273d-118"><dt>**DISK\_CLUSTER\_FLAG\_IN\_MAINTENANCE**</dt> <dt>4</dt></span></span> </dl>                    | <span data-ttu-id="9273d-119">El recurso de clúster asociado a este disco está en modo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="9273d-119">The cluster resource associated with this disk is in maintenance mode.</span></span><br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <span data-ttu-id="9273d-120"><dt>**Disco \_ de Llegada de PNP de marca de clúster \_ \_ \_ \_ completada**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9273d-120"><dt>**DISK\_CLUSTER\_FLAG\_PNP\_ARRIVAL\_COMPLETE**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="9273d-121">El controlador de disco de clúster para el modo kernel (clusdisk) ha recibido la notificación de PnP de la llegada del disco.</span><span class="sxs-lookup"><span data-stu-id="9273d-121">The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the disk.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9273d-122">**FlagsMask**</span><span class="sxs-lookup"><span data-stu-id="9273d-122">**FlagsMask**</span></span>
</dt> <dd>

<span data-ttu-id="9273d-123">Marcas que se están modificando en el miembro **Flags** .</span><span class="sxs-lookup"><span data-stu-id="9273d-123">The flags that are being modified in the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="9273d-124">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="9273d-124">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="9273d-125">**True** para enviar una notificación de cambio de diseño; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9273d-125">**TRUE** to send a layout change notification; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9273d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9273d-126">Requirements</span></span>



| <span data-ttu-id="9273d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9273d-127">Requirement</span></span> | <span data-ttu-id="9273d-128">Value</span><span class="sxs-lookup"><span data-stu-id="9273d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9273d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9273d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9273d-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9273d-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="9273d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9273d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9273d-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9273d-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9273d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9273d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9273d-134"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9273d-134"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9273d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9273d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9273d-136">Estructuras de administración de discos</span><span class="sxs-lookup"><span data-stu-id="9273d-136">Disk Management Structures</span></span>](disk-management-structures.md)
</dt> <dt>

[<span data-ttu-id="9273d-137">**\_información de \_ clúster de obtención de disco de ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9273d-137">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="9273d-138">**\_ \_ \_ información del clúster de conjunto de discos ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="9273d-138">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




