---
description: Esta estructura contiene información sobre el firmware del dispositivo.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY estructura (Winioctl. h)
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
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687537"
---
# <a name="storage_hw_firmware_info_query-structure"></a>\_Estructura de \_ consulta de información de firmware de hardware de \_ almacenamiento \_

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

Versión de esta estructura. Debe establecerse en sizeof (STORAGE \_ HW \_ firmware \_ info \_ Query).

</dd> <dt>

**Tamaño**
</dt> <dd>

Tamaño de esta estructura como un búfer.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas asociadas a la consulta. A continuación se indican las marcas que se pueden establecer en este miembro.



| Marca                                             | Descripción                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| \_controlador de \_ indicador de solicitud de firmware de hardware de \_ \_ almacenamiento \_ | Indica que el destino de la solicitud que no sea la mano del dispositivo o el propio objeto. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

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

[**información de la ranura de firmware de \_ hardware de almacenamiento \_ \_ \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




