---
description: El código de control FSCTL SRV REQUEST RESUME KEY se usa para recuperar una referencia de archivo opaca para su uso con el código de \_ \_ control \_ \_ COPYCHUNK de \_ IOCTL.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY código de control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: a3654cd78b3e337e07c8267a98a09e0dcabbbb5cb193238e3ca3ebe31c59b12b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161819"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>Código de control FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY

El código de control **FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY** se usa para recuperar una referencia de archivo opaca para su uso con el código de control [**\_ COPYCHUNK de IOCTL.**](ioctl-copychunk.md)

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* \[ En\]
</dt> <dd>

Identificador del archivo para el que se va a solicitar la clave de archivo de origen. Para obtener este identificador, llame a la [**función CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ En\]
</dt> <dd>

Código de control de la operación. Use **FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY para** esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se usa con esta operación; se establece en **NULL.**

</dd> <dt>

*nInBufferSize* \[ En\]
</dt> <dd>

No se usa con esta operación; se establece en cero.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Puntero al búfer de salida, una estructura **SRV \_ REQUEST RESUME \_ \_ KEY.** Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*nOutBufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR INSUFFICIENT \_ \_ BUFFER** y *lpBytesReturned* es cero.

Si el *parámetro lpOverlapped* **es NULL,** *lpBytesReturned* no puede ser **NULL.** Incluso cuando una operación no devuelve datos de salida y el parámetro *lpOutBuffer* es **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned.* Después de una operación de este tipo, el valor *de lpBytesReturned* no tiene sentido.

Si *lpOverlapped* no es **NULL,** *lpBytesReturned* puede ser **NULL.** Si *lpOverlapped no* es **NULL** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se completa la operación superpuesta. Para recuperar el número de bytes devueltos, llame a [**la función GetOverlappedResult.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) Si el *parámetro hDevice* está asociado a un puerto de finalización de E/S, puede recuperar el número de bytes devueltos llamando a la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ En\]
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Si el *parámetro hDevice* se abrió sin especificar **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* se omite.

Si *hDevice se* abrió con la marca **FILE FLAG \_ \_ OVERLAPPED,** la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contenga un identificador para un objeto de evento. De lo contrario, se produce un error en la función de maneras imprevisibles.

En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) se devuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no se devuelve hasta que se ha completado la operación o hasta que se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Este código de control no tiene ningún archivo de encabezado asociado. Debe definir el código de control y las estructuras de datos como se muestra a continuación.

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

Estos miembros se pueden describir de la siguiente manera.



| Miembro                                                                                                                       | Descripción                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**<br/>                 | Valor opaco que identifica el archivo de origen en el servidor.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**<br/>                 | Valor opaco que identifica la hora en que se abrió el archivo.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**<br/>                                         | Valor opaco que identifica el proceso que abrió el archivo.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Clave**<br/>                                         | Estructura **SRV \_ RESUME \_ KEY.** Para realizar una operación de copia del lado servidor, use esta estructura con el código de control [**\_ COPYCHUNK de IOCTL.**](ioctl-copychunk.md)<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**<br/> | Este miembro está reservado para uso del sistema; no use.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contexto**<br/>                         | Este miembro está reservado para uso del sistema; no use.<br/>                                                                                                              |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md)
</dt> </dl>

 

 
