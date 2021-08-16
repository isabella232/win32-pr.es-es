---
description: El código de control DISABLE LOCAL BUFFERING de IOCTL LMR deshabilita el almacenamiento en caché en memoria del lado cliente local de los datos al leer o escribir datos en \_ \_ un archivo \_ \_ remoto. Se trata de un código de control definido internamente que no está disponible en un encabezado público.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING código de control
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
ms.openlocfilehash: 88a6fff0955fb9e0c57c7ea5fae99f532c7c6d4dcc3578a75e07da3f35867f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827228"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>Código de control IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING

El código de control **\_ DISABLE LOCAL \_ \_ \_ BUFFERING de IOCTL LMR** deshabilita el almacenamiento en caché en memoria del lado cliente local de los datos al leer o escribir datos en un archivo remoto. Se trata de un código de control definido internamente que no está disponible en un encabezado público.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* \[ En\]
</dt> <dd>

Identificador del archivo remoto. Para obtener este identificador, llame a la [**función CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ En\]
</dt> <dd>

Código de control de la operación. Use el valor 0x140390 para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se usa, debe ser **NULL.**

</dd> <dt>

*nInBufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer de entrada, en bytes. Debe ser cero.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

No se usa, debe ser **NULL.**

</dd> <dt>

*nOutBufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer de salida, en bytes. Debe ser cero.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR INSUFFICIENT \_ \_ BUFFER** y *lpBytesReturned* es cero.

Si el *parámetro lpOverlapped* **es NULL,** *lpBytesReturned* no puede ser **NULL.** Incluso cuando una operación no devuelve datos de salida y el parámetro *lpOutBuffer* es **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned.* Después de esta operación, el valor *de lpBytesReturned* no tiene sentido.

Si *lpOverlapped* no es **NULL,** *lpBytesReturned* puede ser **NULL.** Si *lpOverlapped no* es **NULL** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se completa la operación superpuesta. Para recuperar el número de bytes devueltos, llame a la [**función GetOverlappedResult.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) Si el *parámetro hDevice* está asociado a un puerto de finalización de E/S, puede recuperar el número de bytes devueltos llamando a la función [**GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ En\]
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Si el *parámetro hDevice* se abrió sin especificar **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* se omite.

Si *hDevice se* abrió con la marca **FILE FLAG \_ \_ OVERLAPPED,** la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contenga un identificador para un objeto de evento. De lo contrario, se produce un error en la función de maneras imprevisibles.

Para las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no devuelve hasta que se ha completado la operación o hasta que se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

El sistema define internamente el código de control **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING** como 0x140390 en un archivo de encabezado público. Las aplicaciones de uso especial lo usan para deshabilitar el almacenamiento en caché en memoria del lado cliente local de los datos al leer o escribir datos en un archivo remoto. Una vez deshabilitado el almacenamiento en búfer local, la configuración permanece en vigor hasta que se cierran todos los identificadores abiertos del archivo y el redirector limpia sus estructuras de datos internas.

Las aplicaciones de uso general no deben usar **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING**, ya que puede provocar un tráfico de red excesivo y una pérdida de rendimiento asociada. El código de control **DISABLE \_ LOCAL \_ \_ \_ BUFFERING de IOCTL LMR** solo se debe usar en aplicaciones especializadas que mueven grandes cantidades de datos a través de la red al intentar maximizar el uso del ancho de banda de red. Por ejemplo, las [**funciones CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) y [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) usan **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING** para mejorar el rendimiento de la copia de archivos de gran tamaño.

**IOCTL \_ LMR \_ DISABLE \_ LOCAL \_ BUFFERING** no está implementado por sistemas de archivos locales y producirá el **error ERROR INVALID \_ \_ FUNCTION**. Al emitir el código de control **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING** en los identificadores de directorio remoto, se producirá **el error NO \_ \_ COMPATIBLE.**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
