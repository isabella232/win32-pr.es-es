---
description: Establece diversa información de la batería.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: Código de control de IOCTL_BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909698"
---
# <a name="ioctl_battery_set_information-control-code"></a>\_Código de \_ control de información de conjunto de batería de ioctl \_

Establece diversa información de la batería. La estructura del parámetro de entrada, [**\_ \_ información del conjunto**](battery-set-information-str.md)de la batería, indica qué información de estado de la batería se va a establecer.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la batería en la que se va a establecer la información. Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use **la \_ \_ \_ información del conjunto de baterías de ioctl** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a una estructura [**de \_ \_ información de conjunto de batería**](battery-set-information-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

No se utiliza con esta operación; se establece en **null**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

No se utiliza con esta operación; se establece en cero.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos devueltos en el búfer de *lpOutBuffer* , en bytes.

Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código \_ insuficiente \_ búfer y el recuento de bytes devuelto es cero.

Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**, aunque *lpOutBuffer* sea **null**.

Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**. Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* se abrió con la marca de indicador de archivo \_ \_ superpuesto, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica). Si el dispositivo se ha abierto con la \_ marca de indicador de archivo \_ superpuesto y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.

Si *hDevice* se ha abierto sin especificar la marca de la marca de archivo \_ \_ superpuesta, *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no vuelve hasta que se ha completado la operación o hasta que se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Todas las solicitudes para establecer la información de la batería se completarán con el estado archivo de ERROR \_ \_ no \_ encontrado si la etiqueta de la batería de la solicitud no coincide con la de la etiqueta de la batería actual.

Para conocer las implicaciones de la e/s superpuesta en esta operación, consulte la sección Comentarios del tema [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información de la batería](battery-information.md)
</dt> <dt>

[Códigos de control de administración de energía](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_información del conjunto de batería \_**](battery-set-information-str.md)
</dt> <dt>

[**\_información de \_ consulta de batería ioctl \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**Estado de la \_ consulta de batería ioctl \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_etiqueta de \_ consulta ioctl Battery \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

