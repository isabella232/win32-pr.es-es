---
description: Contiene el número de serie de un dispositivo USB. Lo usa el código de control IOCTL \_ STORAGE GET MEDIA SERIAL \_ \_ \_ \_ NUMBER.
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: MEDIA_SERIAL_NUMBER_DATA estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164362"
---
# <a name="media_serial_number_data-structure"></a>ESTRUCTURA DE \_ DATOS DE NÚMERO DE SERIE \_ \_ MULTIMEDIA

Contiene el número de serie de un dispositivo USB. Lo usa el código de control [**IOCTL \_ STORAGE GET MEDIA SERIAL \_ \_ \_ \_ NUMBER.**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**SerialNumberLength**
</dt> <dd>

Tamaño de la cadena **SerialNumberData,** en bytes.

</dd> <dt>

**Resultado**
</dt> <dd>

Estado de la solicitud.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**SerialNumberData**
</dt> <dd>

El número de serie del dispositivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No hay ningún archivo de encabezado disponible para la **estructura MEDIA SERIAL NUMBER \_ \_ \_ DATA.** Incluya la definición de estructura en la parte superior de esta página en el código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ SERIAL \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




