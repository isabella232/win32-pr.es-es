---
description: Recupera una gran variedad de información de la batería.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: Código de control de IOCTL_BATTERY_QUERY_INFORMATION (Poclass. h)
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
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001957"
---
# <a name="ioctl_battery_query_information-control-code"></a>\_Código de \_ control de información de consulta de batería ioctl \_

Recupera una gran variedad de información de la batería.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


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

Identificador de la batería en la que se va a devolver información. Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Utilice **la \_ \_ \_ información de consulta** de la batería de ioctl para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a una estructura [**de \_ \_ información de consulta**](battery-query-information-str.md) de la batería.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntero al búfer de retorno. El tipo de datos (y, por lo tanto, el tamaño) del búfer de retorno depende de la información solicitada en el miembro del **\_ nivel de \_ información \_ de consulta** de la batería de la estructura de información de consulta de la batería de entrada. [**\_ \_**](battery-query-information-str.md)

En la tabla siguiente se muestran los datos devueltos por un nivel de información determinado.



| Nivel de información                 | Datos devueltos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | Cadena Unicode terminada en **null** que especifica el nombre de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | **ULong** que especifica el tiempo de ejecución estimado de la batería, en segundos. Si la tasa de purga proporcionada en el miembro **AtRate** de la estructura de [**\_ \_ información de consulta**](battery-query-information-str.md) de la batería es cero, este cálculo se basa en la tasa de consumo actual. Si **AtRate** es distinto de cero, la hora devuelta es el tiempo de ejecución esperado para la tasa especificada. Si el tiempo estimado es desconocido (por ejemplo, la batería no se está descargando y **AtRate** es cero), se devuelve la **\_ \_ hora desconocida** de la batería. Tenga en cuenta que este valor no es muy preciso en algunos sistemas de batería. El valor puede variar considerablemente en función del uso de energía presente, que podría verse afectado por la actividad del disco y otros factores. No hay ningún mecanismo de notificación para los cambios en este valor. |
| **BatteryGranularityInformation** | Una matriz de longitud variable de estructuras de [**\_ \_ escalado de informes de batería**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) que contiene la granularidad de los informes para la capacidad de la batería que se devuelve del estado de las consultas de la [**batería de ioctl \_ \_ \_**](ioctl-battery-query-status.md). Se devuelven varias entradas cuando la granularidad depende de la capacidad actual de la batería. Vea **\_ \_ escalado de informes de batería** para la interpretación de la matriz de entradas. El número de entradas se indica por el tamaño del búfer devuelto y se puede calcular como (*lpBytesReturned* /sizeof (escala de **generación \_ de \_ informes de batería**)). El número máximo de entradas que se devolverá es cuatro.                                                                                                |
| **BatteryInformation**            | Estructura [**de \_ información**](battery-information-str.md) de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Una estructura de [**\_ \_ fecha de fabricación**](battery-manufacture-date-str.md) de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | Cadena Unicode terminada en **null** que contiene el nombre del fabricante de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | Cadena Unicode terminada en **null** que contiene el número de serie de la batería.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | **ULong** que contiene la temperatura actual de la batería, en décimas de grado Kelvin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | Cadena Unicode terminada en **null** que identifica de forma única la batería. Este valor se puede usar para realizar el seguimiento de una batería específica. En el caso de las baterías inteligentes, este identificador será la concatenación del nombre del fabricante, el nombre del dispositivo, la fecha de fabricación y una representación imprimible del número de serie. Este valor no está diseñado para mostrarse al usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes. Dependiendo del nivel de información de los datos solicitados, puede tratarse de un búfer de tamaño variable.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos devueltos en el búfer de *lpOutBuffer* , en bytes.

Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código **\_ insuficiente \_ búfer** y el recuento de bytes devuelto es cero.

Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**.

Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**. Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica). Si el dispositivo se ha abierto con la marca de **indicador de archivo \_ \_ superpuesto** y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.

Si *hDevice* se ha abierto sin especificar la marca de la **marca de archivo \_ \_ superpuesta** , *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no vuelve hasta que se ha completado la operación o hasta que se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Parte de la información sobre las baterías es opcional o puede no tener sentido para algunas baterías. Si el tipo de datos solicitado no está disponible para la batería actual, se devuelve un **error de \_ \_ función no válida** .

Todas las solicitudes de información de batería se completarán con el estado **\_ \_ no \_ se encontró el archivo de error** cuando el elemento **BatteryTag** de la solicitud no coincide con el de la etiqueta de la batería actual. Esto garantiza que la información de la batería devuelta coincida con la de la batería solicitada. (Consulte [etiquetas de batería](battery-information.md) para obtener más información).

## <a name="remarks"></a>Observaciones

Este IOCTL de la batería recupera una gran variedad de información de la batería. La estructura de parámetros de entrada, [**\_ \_ información de consulta**](battery-query-information-str.md)de la batería, indica el tipo de información que se va a devolver y cuándo se debe devolver la información de la batería. El tipo de datos y el contenido del búfer de salida varían en función de los datos solicitados.

Para conocer las implicaciones de la e/s superpuesta en esta operación, consulte la sección Comentarios del tema [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, consulte [enumeración de dispositivos de batería](enumerating-battery-devices.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>BatClass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información de la batería](battery-information.md)
</dt> <dt>

[Códigos de control de administración de energía](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_información de consulta de la batería \_**](battery-query-information-str.md)
</dt> <dt>

[**\_escala de informes de batería \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**Estado de la \_ consulta de batería ioctl \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_etiqueta de \_ consulta ioctl Battery \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_información del \_ conjunto de baterías de ioctl \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

