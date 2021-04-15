---
description: El \_ \_ código de control de LMR de ioctl deshabilitar el \_ \_ código de control de almacenamiento en búfer local deshabilita el almacenamiento en caché en memoria del cliente local al leer o escribir datos en un archivo remoto. Este es un código de control definido internamente que no está disponible en un encabezado público.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: Código de control de IOCTL_LMR_DISABLE_LOCAL_BUFFERING
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
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648159"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>IOCTL \_ LMR \_ deshabilitar el \_ \_ código de control de almacenamiento en búfer local

El código de control de LMR de ioctl deshabilitar el código de control de **\_ almacenamiento en \_ \_ \_ búfer local** deshabilita el almacenamiento en caché en memoria del cliente local al leer o escribir datos en un archivo remoto. Este es un código de control definido internamente que no está disponible en un encabezado público.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


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

*hDevice* \[ de\]
</dt> <dd>

Identificador del archivo remoto. Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ de\]
</dt> <dd>

Código de control de la operación. Use el valor 0x140390 para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se utiliza, debe ser **null**.

</dd> <dt>

*nInBufferSize* \[ de\]
</dt> <dd>

Tamaño del búfer de entrada, en bytes. Debe ser cero.

</dd> <dt>

*lpOutBuffer* \[ enuncia\]
</dt> <dd>

No se utiliza, debe ser **null**.

</dd> <dt>

*nOutBufferSize* \[ de\]
</dt> <dd>

Tamaño del búfer de salida, en bytes. Debe ser cero.

</dd> <dt>

*lpBytesReturned* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el **error \_ \_ búfer insuficiente** y *lpBytesReturned* es cero.

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

El sistema define internamente el código de control de **\_ almacenamiento en \_ \_ \_ búfer local de ioctl LMR** como 0x140390 y no en un archivo de encabezado público. Lo usan las aplicaciones de uso especial para deshabilitar el almacenamiento en caché local en memoria de los datos al leer o escribir datos en un archivo remoto. Una vez deshabilitado el almacenamiento en búfer local, el valor permanece en vigor hasta que se cierren todos los identificadores abiertos del archivo y el redirector Limpie sus estructuras de datos internas.

Las aplicaciones de uso general no deben usar **ioctl \_ LMR \_ deshabilitar el almacenamiento en \_ \_ búfer local**, ya que esto puede provocar un tráfico excesivo de red y una pérdida de rendimiento asociada. La LMR de ioctl deshabilitar el código de control de **\_ almacenamiento en \_ \_ \_ búfer local** solo debe usarse en aplicaciones especializadas que mueven grandes cantidades de datos a través de la red al intentar maximizar el uso del ancho de banda de red. Por ejemplo, las funciones [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) y [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) usan **ioctl \_ LMR \_ deshabilitar el \_ almacenamiento en \_ búfer local** para mejorar el rendimiento de la copia de archivos de gran tamaño.

**Ioctl \_ LMR \_ deshabilitar el \_ \_ almacenamiento en búfer local** no está implementado por sistemas de archivos locales y se producirá un error con la **\_ \_ función no válida**. Si se emite el código de control de **\_ almacenamiento en \_ \_ \_ búfer local de ioctl LMR** en los identificadores de directorio remoto, se producirá un **error que no se \_ \_ admite**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
