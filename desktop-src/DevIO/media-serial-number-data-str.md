---
description: Contiene el número de serie de un dispositivo USB. Lo utiliza el código de control de número de serie del medio de almacenamiento de IOCTL \_ \_ \_ \_ \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Estructura de MEDIA_SERIAL_NUMBER_DATA
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
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105649321"
---
# <a name="media_serial_number_data-structure"></a>\_Estructura de \_ datos de número de serie de medios \_

Contiene el número de serie de un dispositivo USB. Lo utiliza el código de control de [**\_ número de \_ \_ \_ serie \_ del medio de almacenamiento de ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .

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

Tamaño de la cadena de **SerialNumberData** , en bytes.

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

No hay ningún archivo de encabezado disponible para la estructura de **datos del número de serie del medio \_ \_ \_** . Incluya la definición de la estructura en la parte superior de esta página en el código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>          |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**el \_ almacenamiento ioctl \_ obtiene el número de \_ serie del medio \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




