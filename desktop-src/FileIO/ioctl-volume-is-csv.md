---
description: Determina si un volumen es un volumen CSV.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: IOCTL_VOLUME_IS_CSV código de control (Ntddvol.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069922"
---
# <a name="ioctl_volume_is_csv-control-code"></a>Código de \_ control CSV DE IOCTL VOLUME \_ IS \_

Determina si un volumen es un volumen CSV.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador del volumen. Para recuperar un identificador de volumen, llame a la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Solo los administradores pueden abrir identificadores de volumen.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Use **IOCTL \_ VOLUME IS \_ CSV \_ para** esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se usa con esta operación; se establece en **NULL.**

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

No se usa con esta operación; se establece en cero (0).

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntero a **TRUE si** el volumen es un volumen CSV; De lo contrario, se produce un error en la llamada de función.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si *lpOverlapped* es **NULL,** *lpBytesReturned* no puede ser **NULL.** Incluso cuando una operación no devuelve datos de salida y *lpOutBuffer* es **NULL,** [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned.* Después de esta operación, el valor *de lpBytesReturned* no tiene sentido.

Si *lpOverlapped* no es **NULL,** *lpBytesReturned* puede ser **NULL.** Si este parámetro no es **NULL y** la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se completa la operación superpuesta. Para recuperar el número de bytes devueltos, llame [**a GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Si *hDevice* está asociado a un puerto de finalización de E/S, puede recuperar el número de bytes devueltos llamando a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Si *hDevice se* abrió sin especificar **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* se omite.

Si *hDevice se* abrió con la marca **FILE FLAG \_ \_ OVERLAPPED,** la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contenga un identificador a un objeto de evento. De lo contrario, se produce un error en la función de maneras imprevisibles.

Para las operaciones superpuestas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no devuelve hasta que se ha completado la operación o se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero (0). Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Ntddvol.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Códigos de control de administración del volumen](volume-management-control-codes.md)
</dt> </dl>

 

