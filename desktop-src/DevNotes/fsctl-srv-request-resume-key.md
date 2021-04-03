---
description: El código de control de la \_ \_ clave de la solicitud del archivo FSCTL SRV \_ \_ se usa para recuperar una referencia de archivo opaca para su uso con el \_ código de control COPYCHUNK de ioctl.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Código de control de FSCTL_SRV_REQUEST_RESUME_KEY
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
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906996"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>\_Código de \_ control de \_ clave de recuperación de solicitud \_ de FSCTL SRV

El código de control de la clave de la solicitud del archivo **FSCTL \_ SRV \_ \_ \_** se usa para recuperar una referencia de archivo opaca para su uso con el código de control [**\_ COPYCHUNK de ioctl**](ioctl-copychunk.md) .

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


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

*hDevice* \[ de\]
</dt> <dd>

Identificador del archivo para el que se va a solicitar la clave del archivo de código fuente. Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ de\]
</dt> <dd>

Código de control de la operación. Use **la \_ \_ \_ \_ clave de reanudación de solicitud de FSCTL SRV** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se utiliza con esta operación; se establece en **null**.

</dd> <dt>

*nInBufferSize* \[ de\]
</dt> <dd>

No se utiliza con esta operación; se establece en cero.

</dd> <dt>

*lpOutBuffer* \[ enuncia\]
</dt> <dd>

Un puntero al búfer de salida, una estructura de **\_ \_ \_ clave de reanudación de solicitud SRV** . Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*nOutBufferSize* \[ de\]
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente** y *lpBytesReturned* es cero.

Si el parámetro *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**. Incluso cuando una operación no devuelve datos de salida y el parámetro *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*. Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.

Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**. Si *lpOverlapped* no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta. Para recuperar el número de bytes devueltos, llame a la función [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ de\]
</dt> <dd>

Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Si el parámetro *hDevice* se ha abierto sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.

Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento. De lo contrario, se produce un error imprevisible en la función.

En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no devuelve ningún resultado hasta que la operación se haya completado o hasta que se produzca un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Este código de control no tiene ningún archivo de encabezado asociado. Debe definir el código de control y las estructuras de datos como se indica a continuación.

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

Estos miembros se pueden describir como se indica a continuación.



| Miembro                                                                                                                       | Descripción                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**<br/>                 | Un valor opaco que identifica el archivo de origen en el servidor.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Indicaciones**<br/>                 | Un valor opaco que identifica la hora en que se abrió el archivo.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**ID**<br/>                                         | Un valor opaco que identifica el proceso que abrió el archivo.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Clave**<br/>                                         | Una estructura de **\_ \_ clave de reanudación de SRV** . Para realizar una operación de copia en el lado servidor, use esta estructura con el código de control [**ioctl \_ COPYCHUNK**](ioctl-copychunk.md) .<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**<br/> | Este miembro está reservado para uso del sistema. No use.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contexto**<br/>                         | Este miembro está reservado para uso del sistema. No use.<br/>                                                                                                              |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md)
</dt> </dl>

 

 
