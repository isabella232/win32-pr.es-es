---
description: Contiene información sobre el tamaño de un dispositivo. Esto se devuelve desde el código de control de la capacidad de lectura de almacenamiento de IOCTL \_ \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY estructura (Ntddstor. h)
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
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423259"
---
# <a name="storage_read_capacity-structure"></a>Estructura de capacidad de \_ lectura de almacenamiento \_

Contiene información sobre el tamaño de un dispositivo. Esto se devuelve desde el código de control de la [**capacidad de lectura de almacenamiento de ioctl \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .

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

El tamaño del disco en bytes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El archivo de encabezado Ntddstor. h está disponible en el kit de controladores de Windows (WDK).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2003 con SP1<br/>                          |
| Encabezado<br/>                   | <dl> <dt>Ntddstor. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_capacidad de \_ lectura de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




