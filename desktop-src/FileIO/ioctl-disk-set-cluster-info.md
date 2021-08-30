---
description: Establece la información del clúster en un disco.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: IOCTL_DISK_SET_CLUSTER_INFO código de control (Ntdddisk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 09aa5f228a1567cdccfac4faa67db8bd8209fc35ad68de174dcf9507c162d19a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107465"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a>Código de \_ control IOCTL DISK \_ SET CLUSTER \_ \_ INFO

Establece la información del clúster en un disco.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
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

Use **IOCTL \_ DISK SET CLUSTER INFO \_ \_ \_ para** esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a una estructura de [**datos \_ DISK CLUSTER \_ INFO**](disk-cluster-info.md) que contiene información de clúster para el disco.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

No se usa con esta operación. Se establece en **NULL.**

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes. Establezca en 0 (cero).

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
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Códigos de control de administración de discos](disk-management-control-codes.md)
</dt> <dt>

[**INFORMACIÓN DEL \_ CLÚSTER DE \_ DISCO**](disk-cluster-info.md)
</dt> <dt>

[**IOCTL \_ DISK \_ GET \_ CLUSTER \_ INFO**](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

