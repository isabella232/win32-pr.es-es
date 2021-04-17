---
description: El \_ código de control COPYCHUNK de ioctl inicia una copia del lado servidor de un intervalo de datos, también denominado fragmento.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Código de control de IOCTL_COPYCHUNK
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666161"
---
# <a name="ioctl_copychunk-control-code"></a>\_Código de control COPYCHUNK de ioctl

El código de control **\_ COPYCHUNK de ioctl** inicia una copia del lado servidor de un intervalo de datos, también denominado fragmento.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

Identificador del archivo que es el destino de la operación de copia del lado servidor. Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ de\]
</dt> <dd>

Código de control de la operación. Use **ioctl \_ COPYCHUNK** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Un puntero al búfer de entrada, una estructura de **\_ \_ copia de COPYCHUNK SRV** . Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*nInBufferSize* \[ de\]
</dt> <dd>

Tamaño del búfer de entrada, en bytes.

</dd> <dt>

*lpOutBuffer* \[ enuncia\]
</dt> <dd>

Un puntero al búfer de salida, una estructura de **\_ \_ respuesta COPYCHUNK SRV** . Para obtener más información, vea la sección Comentarios.

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
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

Estos miembros se pueden describir como se indica a continuación.



| Miembro                                                                                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**<br/>                     | Desplazamiento, en bytes, desde el principio del archivo de código fuente hasta el fragmento que se va a copiar.<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**<br/> | Desplazamiento, en bytes, desde el principio del archivo de destino hasta la ubicación donde se va a copiar el fragmento.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Longitud**<br/>                                             | El número de bytes de datos en el fragmento que se va a copiar. Debe ser mayor que cero y menor o igual que 1 MB. **Longitud** \* **ChunkCount** debe ser menor o igual que 16 MB.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | Clave que representa el archivo de código fuente con los datos que se van a copiar. Esta clave se obtiene a través de la [**\_ \_ \_ \_ clave de reanudación de solicitud de FSCTL SRV**](fsctl-srv-request-resume-key.md).<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | El número de fragmentos que se van a copiar. Debe ser mayor que cero y menor o igual que 256.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Sector**<br/>                                     | Este miembro está reservado para uso del sistema. No use.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Paquete**<br/>                                                 | Una matriz de estructuras **ChunkCount** **SRV \_ COPYCHUNK** , una para cada fragmento que se va a copiar. La longitud, en bytes, de esta matriz debe ser **ChunkCount** \* sizeof (**SRV \_ COPYCHUNK**).<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**<br/>                 | Si se produjo un error en la operación con un **\_ \_ parámetro no válido**, este valor indica el número máximo de fragmentos que el servidor aceptará en una única solicitud, que es 256. De lo contrario, este valor indica el número de fragmentos que se escribieron correctamente.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | Si se produjo un error en la operación con un **\_ \_ parámetro no válido**, este valor indica el número máximo de bytes que el servidor permitirá escribir en un único fragmento, que es 1 MB. De lo contrario, este valor indica el número de bytes que se escribieron correctamente en el último fragmento que no se procesó correctamente (si se produjo una escritura parcial).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | Si se produjo un error en la operación con un **\_ \_ parámetro no válido**, este valor indica el número máximo de bytes que el servidor copiará en una única solicitud, que es de 16 MB. De lo contrario, este valor indica el número de bytes que se escribieron correctamente.<br/>                                                                                                 |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_clave de \_ \_ reanudación de solicitud \_ de FSCTL SRV**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
