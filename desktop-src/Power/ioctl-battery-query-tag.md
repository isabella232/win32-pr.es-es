---
description: Recupera la etiqueta actual de las baterías.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG código de control (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062858"
---
# <a name="ioctl_battery_query_tag-control-code"></a>Código de \_ control IOCTL BATTERY \_ QUERY \_ TAG

Recupera la etiqueta actual de la batería.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la batería de la que se va a recuperar la etiqueta. Para recuperar un identificador de dispositivo, llame a la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use **LA ETIQUETA DE CONSULTA DE LA BATERÍA \_ \_ \_ DE IOCTL** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a un búfer **de entrada ULONG.** El valor indica el número de milisegundos que hay que esperar si no hay batería. Un valor de -1 indica que la solicitud esperará indefinidamente (o hasta que se cancele por algún otro evento).

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntero a un búfer **de salida ULONG.** Si se ejecuta correctamente, este búfer contiene la etiqueta de batería actual, que puede ser cualquier valor excepto BATTERY \_ TAG \_ INVALID. En caso de error, [**si GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error **ARCHIVO DE ERROR NO \_ \_ \_ ENCONTRADO,** este búfer contiene el valor **BATTERY TAG \_ \_ INVALID**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer *lpOutBuffer,* en bytes.

Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error **ERROR INSUFFICIENT \_ \_ BUFFER** y el recuento de bytes devuelto es cero.

Si *lpOverlapped* es **NULL** (E/S nooverlapped), *lpBytesReturned* no puede ser **NULL.**

Si *lpOverlapped no* es **NULL** (E/S superpuesta), *lpBytesReturned* puede ser **NULL.** Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos llamando a la [**función GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Si *hDevice* está asociado a un puerto de finalización de E/S, puede obtener el número de bytes devueltos llamando a la función [**GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Si *hDevice se* abrió con la marca **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* debe apuntar a una estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica). Si el dispositivo se abrió con la marca **\_ FILE FLAG \_ OVERLAPPED** y *lpOverlapped* es **NULL,** la función produce un error de manera imprevisible.

Si *hDevice* se abrió sin especificar la marca **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no se devuelve hasta que se ha completado la operación o hasta que se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta IOCTL de batería recupera la etiqueta actual de la batería. La etiqueta de batería es un valor distinto de cero único que cambia cuando la batería física se reinserta, se reemplaza o se somete a cualquier cambio de característica. Consulte la sección Etiquetas de batería del tema Información general de la batería para obtener más información sobre cuándo cambia una etiqueta de batería, cómo detectar el cambio y cómo debe continuar una aplicación después de un cambio de etiqueta de batería. [](battery-information.md) Cuando una batería no está presente, esta solicitud esperará el tiempo indicado y, si todavía no hay batería presente, devolverá **ERROR \_ FILE NOT \_ \_ FOUND** y establecerá la etiqueta de batería en **BATTERY TAG \_ \_ INVALID**. (Consulte La información de la batería para obtener más información).

Todas las solicitudes de otra información de batería requieren que el autor de la llamada proporcione la etiqueta de batería correspondiente. Esto garantiza que el autor de la llamada recibe información para la misma batería para cada solicitud y garantiza que el autor de la llamada sea consciente de los cambios en la batería sin sondeo constante.

Para ver las implicaciones de la E/S superpuesta en esta operación, consulte la sección Comentarios del [**tema DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, consulte [Enumeración de dispositivos de batería.](enumerating-battery-devices.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información de la batería](battery-information.md)
</dt> <dt>

[Códigos de control de administración de energía](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**INFORMACIÓN DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**ESTADO DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**INFORMACIÓN DEL \_ CONJUNTO DE \_ BATERÍAS DE IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

