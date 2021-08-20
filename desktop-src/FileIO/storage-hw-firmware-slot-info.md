---
description: Esta estructura contiene información sobre una ranura en un dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: STORAGE_HW_FIRMWARE_SLOT_INFO estructura (Winioctl.h)
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
ms.openlocfilehash: 6db9bc5341bf3efec18390d171c205cc57b933afe166af6df48657b668cc85ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996459"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>Estructura \_ STORAGE HW FIRMWARE SLOT \_ \_ \_ INFO

Esta estructura contiene información sobre una ranura en un dispositivo.

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

Versión de esta estructura. Debe establecerse en sizeof(STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO)

</dd> <dt>

**Tamaño**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

**SlotNumber**
</dt> <dd>

Número de ranura de esta ranura.

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

Revisión del firmware en esta ranura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Winioctl.h.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACTIVACIÓN DEL \_ FIRMWARE DE ALMACENAMIENTO \_ DE IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**ACTIVACIÓN \_ DEL FIRMWARE DEL HARDWARE DE \_ \_ ALMACENAMIENTO**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**DESCARGA DE \_ FIRMWARE DE ALMACENAMIENTO \_ DE IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**DESCARGA \_ DE FIRMWARE DEL HARDWARE DE \_ \_ ALMACENAMIENTO**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**IOCTL \_ STORAGE \_ FIRMWARE \_ GET \_ INFO**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**INFORMACIÓN \_ DE FIRMWARE DEL HARDWARE DE \_ \_ ALMACENAMIENTO**](storage-hw-firmware-info.md)
</dt> <dt>

[**CONSULTA \_ DE INFORMACIÓN DE FIRMWARE DEL HARDWARE DE \_ \_ \_ ALMACENAMIENTO**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




