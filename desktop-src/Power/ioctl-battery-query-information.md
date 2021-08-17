---
description: Recupera una variedad de información para la batería.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION código de control (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: a48514b81ddf5d8f7c0d84d4404eb01752413e73ade43db089fbb6dade673bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143546"
---
# <a name="ioctl_battery_query_information-control-code"></a>Código de \_ control IOCTL BATTERY \_ QUERY \_ INFORMATION

Recupera una variedad de información para la batería.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la batería en la que se va a devolver información. Para recuperar un identificador de dispositivo, llame a la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use **LA INFORMACIÓN DE CONSULTA DE LA BATERÍA \_ \_ \_ DE IOCTL** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a una estructura [**BATTERY \_ QUERY \_ INFORMATION.**](battery-query-information-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntero al búfer de devolución. El tipo de datos (y, por tanto, el tamaño) del búfer devuelto depende de la información solicitada en el miembro **BATTERY \_ QUERY INFORMATION \_ \_ LEVEL** de la estructura [**BATTERY QUERY INFORMATION \_ \_ de**](battery-query-information-str.md) entrada.

En la tabla siguiente se muestran los datos devueltos por un nivel de información determinado.



| Nivel de información                 | Datos devueltos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | **Cadena** Unicode terminada en NULL que especifica el nombre de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | ULONG **que** especifica el tiempo de ejecución estimado de la batería, en segundos. Si la velocidad de purga proporcionada en el miembro **AtRate** de la estructura [**BATTERY QUERY \_ \_ INFORMATION**](battery-query-information-str.md) es cero, este cálculo se basa en la tasa actual de purga. Si **AtRate** es distinto de cero, el tiempo devuelto es el tiempo de ejecución esperado para la tasa determinada. Si se desconoce el tiempo estimado (por ejemplo, la batería no se descarga y **AtRate** es cero), se devuelve **BATTERY UNKNOWN \_ \_ TIME.** Tenga en cuenta que este valor no es muy preciso en algunos sistemas de batería. El valor puede variar ampliamente en función del uso actual de energía, lo que podría verse afectado por la actividad del disco y otros factores. No hay ningún mecanismo de notificación para los cambios en este valor. |
| **BatteryGranularityInformation** | Matriz de longitud variable de estructuras [**BATTERY \_ REPORTING \_ SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) que contiene la granularidad de informes para la capacidad de la batería que se devuelve de ESTADO DE CONSULTA DE BATERÍA [**\_ \_ DE \_ IOCTL**](ioctl-battery-query-status.md). Se devuelven varias entradas cuando la granularidad depende de la capacidad actual de la batería. Vea **BATTERY \_ REPORTING SCALE \_ para** la interpretación de la matriz de entradas. El número de entradas se indica por el tamaño del búfer devuelto y se puede calcular como (*lpBytesReturned/* sizeof (**BATTERY \_ REPORTING \_ SCALE**)). El número máximo de entradas que se devolverán es cuatro.                                                                                                |
| **BatteryInformation**            | Estructura [**BATTERY \_ INFORMATION.**](battery-information-str.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Estructura [**BATTERY \_ MANUFACTURE \_ DATE.**](battery-manufacture-date-str.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | **Cadena** Unicode terminada en NULL que contiene el nombre del fabricante de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | **Cadena** Unicode terminada en NULL que contiene el número de serie de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | ULONG **que** contiene la temperatura actual de la batería, en 10ths of a degree Kelvin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | **Cadena** Unicode terminada en NULL que identifica de forma única la batería. Este valor se puede usar para realizar un seguimiento de una batería específica. En el caso de las baterías inteligentes, este identificador será la concatenación del nombre del fabricante, el nombre del dispositivo, la fecha de fabricación y una representación imprimible del número de serie. Este valor no está pensado para mostrarse al usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes. Según el nivel de información de los datos solicitados, puede ser un búfer de tamaño variable.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos devueltos en el búfer *lpOutBuffer,* en bytes.

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

Parte de la información sobre las baterías es opcional o puede que no tenga sentido para algunas baterías. Si el tipo determinado de datos solicitados no está disponible para la batería actual, **se devuelve ERROR INVALID \_ \_ FUNCTION.**

Todas las solicitudes de información de batería se completarán con el estado ARCHIVO DE ERROR NO ENCONTRADO siempre que el elemento **BatteryTag** de la solicitud no coincida con el de la etiqueta de batería actual. **\_ \_ \_** Esto garantiza que la información de la batería devuelta coincida con la de la batería solicitada. (Consulte [Etiquetas de batería](battery-information.md) para obtener más información).

## <a name="remarks"></a>Comentarios

Esta IOCTL de batería recupera una variedad de información para la batería. La estructura de parámetros de entrada, [**BATTERY \_ QUERY \_ INFORMATION**](battery-query-information-str.md), indica el tipo de información que se va a devolver y cuándo se debe devolver la información de la batería. El tipo de datos y el contenido del búfer de salida varían en función de los datos solicitados.

Para ver las implicaciones de la E/S superpuesta en esta operación, consulte la sección Comentarios del [**tema DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, consulte [Enumeración de dispositivos de batería.](enumerating-battery-devices.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información de la batería](battery-information.md)
</dt> <dt>

[Códigos de control de administración de energía](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**INFORMACIÓN DE \_ CONSULTA DE \_ BATERÍA**](battery-query-information-str.md)
</dt> <dt>

[**ESCALA \_ DE INFORMES DE \_ BATERÍA**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**ESTADO DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**ETIQUETA DE CONSULTA \_ DE \_ BATERÍA DE \_ IOCTL**](ioctl-battery-query-tag.md)
</dt> <dt>

[**INFORMACIÓN DEL \_ CONJUNTO DE \_ BATERÍAS DE IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

