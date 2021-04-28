---
description: 'STORAGE_HW_FIRMWARE_INFO_QUERY estructura: esta estructura contiene información sobre el firmware del dispositivo.'
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY estructura (Winioctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119403"
---
# <a name="storage_hw_firmware_info_query-structure"></a>ESTRUCTURA DE CONSULTA DE INFORMACIÓN DE FIRMWARE DE HARDWARE \_ \_ DE \_ \_ ALMACENAMIENTO

Esta estructura contiene información sobre el firmware del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Versión de esta estructura. Debe establecerse en sizeof(STORAGE \_ HW \_ FIRMWARE INFO \_ \_ QUERY)

</dd> <dt>

**Tamaño**
</dt> <dd>

Tamaño de esta estructura como búfer.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas asociadas a la consulta. Las siguientes son marcas que se pueden establecer en este miembro.



| Marcar                                             | Descripción                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| CONTROLADOR DE MARCA DE SOLICITUD DE FIRMWARE DE HARDWARE \_ \_ DE \_ \_ \_ ALMACENAMIENTO | Indica que el destino de la solicitud es distinto de la propia mano o el objeto del dispositivo. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 solo \[ aplicaciones de escritorio\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Winioctl.h.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ACTIVACIÓN DEL \_ FIRMWARE DE \_ ALMACENAMIENTO DE IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**ACTIVACIÓN DEL \_ FIRMWARE DEL HW DE \_ \_ ALMACENAMIENTO**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**DESCARGA DE \_ FIRMWARE DE \_ ALMACENAMIENTO DE IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**DESCARGA DE \_ FIRMWARE DE HARDWARE DE \_ \_ ALMACENAMIENTO**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**IOCTL \_ STORAGE \_ FIRMWARE \_ GET \_ INFO**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**INFORMACIÓN \_ DE FIRMWARE DEL HARDWARE DE \_ \_ ALMACENAMIENTO**](storage-hw-firmware-info.md)
</dt> <dt>

[**INFORMACIÓN DE \_ RANURA DE FIRMWARE DEL HARDWARE DE \_ \_ \_ ALMACENAMIENTO**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




