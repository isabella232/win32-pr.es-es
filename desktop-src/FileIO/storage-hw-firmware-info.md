---
description: 'STORAGE_HW_FIRMWARE_INFO estructura: esta estructura contiene información sobre el firmware del dispositivo.'
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO estructura (Winioctl.h)
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
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090963"
---
# <a name="storage_hw_firmware_info-structure"></a>Estructura DE \_ INFORMACIÓN DE FIRMWARE DE HARDWARE DE \_ \_ ALMACENAMIENTO

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

Versión de esta estructura. Debe establecerse en sizeof(STORAGE \_ HW \_ FIRMWARE \_ INFO)

</dd> <dt>

**Tamaño**
</dt> <dd>

Tamaño de esta estructura como búfer, incluida la ranura.

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

Número de ranuras de firmware del dispositivo. Esta es la dimensión de la matriz Slot.

> [!Note]  
> Algunos dispositivos pueden almacenar más de una imagen de firmware, si tienen más de una ranura de firmware.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

Ranura de firmware que contiene la imagen de firmware actualmente activa o en ejecución.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

La ranura de firmware que está pendiente de activación.

</dd> <dt>

**FirmwareShared**
</dt> <dd>

Indica que el firmware se aplica tanto al dispositivo como al controlador o adaptador, por ejemplo, al SSD NVMe.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

Alineación de la carga de la imagen, en número de bytes. El máximo es PAGE \_ SIZE. El tamaño de transferencia es un mutliple de este tamaño. Algunos protocolos requieren al menos un tamaño de sector. Cuando este valor se establece en 0, significa que este valor no es válido.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

Tamaño máximo de la carga de la imagen, que se usa para un solo comando.

</dd> <dt>

**Slot**
</dt> <dd>

Contiene la información de ranura para cada ranura del dispositivo, de tipo [**STORAGE HW FIRMWARE SLOT \_ \_ \_ \_ INFO**](storage-hw-firmware-slot-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 solo \[ aplicaciones de escritorio\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Winioctl.h.h (incluye Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

[**CONSULTA \_ DE INFORMACIÓN DE FIRMWARE DEL HARDWARE DE \_ \_ \_ ALMACENAMIENTO**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**INFORMACIÓN DE \_ RANURA DE FIRMWARE DEL HARDWARE DE \_ \_ \_ ALMACENAMIENTO**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




