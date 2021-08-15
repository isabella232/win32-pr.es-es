---
description: Contiene información sobre el tamaño de un dispositivo. Esto se devuelve desde el código de control CAPACIDAD DE LECTURA DE ALMACENAMIENTO \_ DE IOCTL. \_ \_
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY estructura (Ntddstor.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: 3a138f6594e241c96526ebf6955c61374aa0f48a5aa66f364ef82c1591b64594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404976"
---
# <a name="storage_read_capacity-structure"></a>ESTRUCTURA \_ DE CAPACIDAD DE LECTURA DE \_ ALMACENAMIENTO

Contiene información sobre el tamaño de un dispositivo. Esto se devuelve desde el código de control [**DE CAPACIDAD DE LECTURA DE ALMACENAMIENTO \_ \_ \_ DE IOCTL.**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Versión de esta estructura. El autor de la llamada debe establecer este miembro en `sizeof(STORAGE_READ_CAPACITY)` .

</dd> <dt>

**Tamaño**
</dt> <dd>

Tamaño de los datos devueltos.

</dd> <dt>

**BlockLength**
</dt> <dd>

Número de bytes por bloque.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

Número total de bloques en el disco.

</dd> <dt>

**DiskLength**
</dt> <dd>

Tamaño del disco en bytes.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El archivo de encabezado Ntddstor.h está disponible en Windows Driver Kit (WDK).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2003 con SP1<br/>                          |
| Header<br/>                   | <dl> <dt>Ntddstor.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CAPACIDAD DE \_ LECTURA DE ALMACENAMIENTO DE \_ \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




