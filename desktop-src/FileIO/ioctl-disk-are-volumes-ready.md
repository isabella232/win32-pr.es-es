---
description: Espera a que todos los volúmenes del disco especificado estén listos para su uso.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: IOCTL_DISK_ARE_VOLUMES_READY código de control (Ntdddisk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: cba83d8f850151e217460595f5f4fc8831b99ee5ee30fc0bb908c0ca04a9cdce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981975"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a>EL DISCO IOCTL \_ SON EL CÓDIGO DE control LISTO PARA \_ \_ \_ VOLÚMENES

Espera a que todos los volúmenes del disco especificado estén listos para su uso.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador del disco.

Para recuperar un identificador de dispositivo, llame a la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación.

Use **IOCTL \_ DISK ARE VOLUMES READY \_ \_ \_ para** esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se usa con esta operación. Se establece en **NULL.**

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes. Establezca en 0 (cero).

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

No se usa con esta operación. Se establece en **NULL.**

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

No se usa con esta operación. Establezca en 0 (cero).

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

No se usa con esta operación. Se establece en **NULL.**

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Si *hDevice se* abrió sin especificar **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* se omite.

Si *hDevice se* abrió con la marca **FILE FLAG \_ \_ OVERLAPPED,** la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contenga un identificador a un objeto de evento. De lo contrario, se produce un error en la función de maneras imprevisibles.

Para las operaciones superpuestas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no devuelve hasta que se ha completado la operación o se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, lo que indica que todos los volúmenes del disco están listos para su uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Códigos de control de administración de discos](disk-management-control-codes.md)
</dt> </dl>

 

