---
description: Esta estructura contiene información sobre una ranura de un dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: STORAGE_HW_FIRMWARE_SLOT_INFO estructura (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687009"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>\_Estructura de \_ información de ranura de firmware de hardware de \_ almacenamiento \_

Esta estructura contiene información sobre una ranura de un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Versión de esta estructura. Debe establecerse en sizeof (STORAGE \_ HW \_ firmware \_ slot \_ info).

</dd> <dt>

**Tamaño**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

**SlotNumber**
</dt> <dd>

El número de ranura de esta ranura.

</dd> <dt>

**ReadOnly**
</dt> <dd>

Indica si esta ranura es de solo lectura o no.

</dd> <dt>

**Reserved0**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**Revisión**
</dt> <dd>

La revisión del firmware en esta ranura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Winioctl. h. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ \_ Activar firmware de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**\_ \_ Activar firmware de HW de almacenamiento \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**\_descarga de \_ firmware de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**\_descarga de \_ firmware de hardware de almacenamiento \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**\_ \_ \_ obtener información de firmware de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**\_información de \_ firmware de HW de almacenamiento \_**](storage-hw-firmware-info.md)
</dt> <dt>

[**\_consulta de \_ información de firmware de HW de almacenamiento \_ \_**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




