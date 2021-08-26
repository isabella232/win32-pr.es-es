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
ms.openlocfilehash: cbb007769238f0e6a4239366e8fe9956e61f892f7d3c98f2b638dc425dc9359f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053485"
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



## <a name="members"></a>Miembros

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

## <a name="remarks"></a>Comentarios

No hay ningún archivo de encabezado disponible para la **estructura MEDIA SERIAL NUMBER \_ \_ \_ DATA.** Incluya la definición de estructura en la parte superior de esta página en el código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ SERIAL \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




