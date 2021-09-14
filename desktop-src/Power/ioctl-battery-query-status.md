---
description: Recupera el estado actual de la batería.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS código de control (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062861"
---
# <a name="ioctl_battery_query_status-control-code"></a>Código de \_ control DE ESTADO DE LA CONSULTA DE LA BATERÍA \_ \_ DE IOCTL

Recupera el estado actual de la batería.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la batería de la que se va a devolver información. Para recuperar un identificador de dispositivo, llame a la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use **IOCTL \_ BATTERY QUERY \_ STATUS \_ para** esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a una estructura [**BATTERY \_ WAIT \_ STATUS.**](battery-wait-status-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntero a una estructura [**BATTERY \_ STATUS.**](battery-status-str.md)

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos devueltos en el *búfer lpOutBuffer,* en bytes.

Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error **ERROR INSUFFICIENT \_ \_ BUFFER** y el recuento de bytes devuelto es cero.

Si *lpOverlapped* es **NULL** (E/S nooverlapped), *lpBytesReturned* no puede ser **NULL.**

Si *lpOverlapped* no es **NULL** (E/S superpuesta), *lpBytesReturned* puede ser **NULL.** Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos llamando a la [**función GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Si *hDevice* está asociado a un puerto de finalización de E/S, puede obtener el número de bytes devueltos llamando a la [**función GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Si *hDevice se* abrió con la marca **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* debe apuntar a una [**estructura OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica). Si el dispositivo se abrió con la marca **\_ FILE FLAG \_ OVERLAPPED** y *lpOverlapped* es **NULL,** se produce un error en la función de maneras imprevisibles.

Si *hDevice* se abrió sin especificar la marca **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no se devuelve hasta que se haya completado la operación o hasta que se produzca un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta IOCTL de batería recupera el estado de la batería en el momento en que se devuelve la operación. La estructura de parámetros de entrada, [**BATTERY \_ WAIT \_ STATUS**](battery-wait-status-str.md), indica cuándo se va a procesar y devolver el estado de la batería.

Las solicitudes de estado de la batería pueden ser para la devolución inmediata o se pueden establecer para esperar una condición determinada antes de completarse. Por ejemplo, se puede realizar una solicitud de información de batería que espere hasta que la capacidad de la batería alcance un punto especificado o cambie el estado de la batería.

Todas las solicitudes de información de la batería se completarán con el estado ARCHIVO DE ERROR NO ENCONTRADO siempre que el elemento **BatteryTag** de la solicitud no coincida con el de la etiqueta de batería actual. **\_ \_ \_** (Consulte [Etiquetas de batería](battery-information.md) para obtener más información). Esto se usa para asegurarse de que la información de la batería devuelta coincide con la de la batería solicitada.

Para ver las implicaciones de la E/S superpuesta en esta operación, consulte la sección Comentarios del [**tema DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, consulte [Enumeración de dispositivos de batería.](enumerating-battery-devices.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información de batería](battery-information.md)
</dt> <dt>

[Códigos de control de administración de energía](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**ESTADO DE \_ LA BATERÍA**](battery-status-str.md)
</dt> <dt>

[**ESTADO DE \_ ESPERA DE \_ LA BATERÍA**](battery-wait-status-str.md)
</dt> <dt>

[**INFORMACIÓN DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**ETIQUETA DE CONSULTA \_ DE BATERÍA \_ DE IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**INFORMACIÓN DEL CONJUNTO \_ DE \_ BATERÍAS DE IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

