---
description: Esta estructura contiene información sobre el firmware del dispositivo.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO estructura (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668371"
---
# <a name="storage_hw_firmware_info-structure"></a>\_Estructura de \_ información de firmware de HW de almacenamiento \_

Esta estructura contiene información sobre el firmware del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Versión de esta estructura. Debe establecerse en sizeof (STORAGE \_ HW \_ firmware \_ info)

</dd> <dt>

**Tamaño**
</dt> <dd>

Tamaño de esta estructura como un búfer que incluye la ranura.

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

Indica que este firmware admite una actualización.

</dd> <dt>

**Reserved0**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**SlotCount**
</dt> <dd>

El número de ranuras de firmware en el dispositivo. Esta es la dimensión de la matriz de ranuras.

> [!Note]  
> Algunos dispositivos pueden almacenar más de una imagen de firmware, si tienen más de 1 ranura de firmware.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

La ranura de firmware que contiene la imagen de firmware actualmente activa o en ejecución.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

La ranura de firmware que está pendiente de activación.

</dd> <dt>

**FirmwareShared**
</dt> <dd>

Indica que el firmware se aplica tanto al dispositivo como al controlador o adaptador, por ejemplo, un SSD de NVMe.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

Alineación de la carga de la imagen, en número de bytes. El máximo es el \_ tamaño de página. El tamaño de la transferencia es un múltiple de este tamaño. Algunos protocolos requieren al menos el tamaño del sector. Cuando este valor se establece en 0, significa que este valor no es válido.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

Tamaño máximo de carga de la imagen, que se usa para un solo comando.

</dd> <dt>

**Slot**
</dt> <dd>

Contiene la información de la ranura de cada ranura del dispositivo, de tipo información de la [**ranura de firmware de hardware de almacenamiento \_ \_ \_ \_**](storage-hw-firmware-slot-info.md).

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

[**\_consulta de \_ información de firmware de HW de almacenamiento \_ \_**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**información de la ranura de firmware de \_ hardware de almacenamiento \_ \_ \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




