---
description: Contiene información de consulta de batería.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: BATTERY_QUERY_INFORMATION estructura (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 9049517108cbb31df1164cc88640a78e104e2902d3a8a4b8dec4b8bfb48e8a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143688"
---
# <a name="battery_query_information-structure"></a>ESTRUCTURA BATTERY \_ QUERY \_ INFORMATION

Contiene información de consulta de batería. Esta estructura se usa con el código de control [**IOCTL \_ BATTERY QUERY \_ \_ INFORMATION**](ioctl-battery-query-information.md) para especificar el tipo de información que se va a devolver.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BATTERY_QUERY_INFORMATION {
  ULONG                           BatteryTag;
  BATTERY_QUERY_INFORMATION_LEVEL InformationLevel;
  LONG                            AtRate;
} BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BatteryTag**
</dt> <dd>

La etiqueta de batería actual de la batería. Solo se puede devolver información de una batería que coincida con la etiqueta. Siempre que este valor no coincida con la etiqueta actual de la batería, la solicitud IOCTL se completará con ERROR \_ FILE \_ NOT \_ FOUND. Esto indica al autor de la llamada que la batería asociada a la etiqueta ya existe. El autor de la llamada puede optar por usar la operación [**IOCTL \_ BATTERY QUERY \_ \_ TAG**](ioctl-battery-query-tag.md) para determinar la etiqueta de la batería recién instalada, si existe. (Consulte [Etiquetas de batería](battery-information.md) para obtener más información).

Cuando se realiza una solicitud de información de consulta, se comprueba este valor. Además, si la solicitud está en curso mientras este valor cambia, la solicitud se anula con el estado ERROR \_ FILE \_ NOT \_ FOUND.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Nivel de la información de la batería que se está consultando. Los datos devueltos por la IOCTL dependen de este valor. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | Cadena Unicode terminada en NULL que contiene el nombre de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | ULONG **que** especifica el tiempo de ejecución estimado de la batería, en segundos. Si la velocidad de purga proporcionada en el **miembro AtRate** de la estructura **BATTERY QUERY \_ \_ INFORMATION** es cero, este cálculo se basa en la tasa actual de purga. Si **AtRate** es distinto de cero, el tiempo devuelto es el tiempo de ejecución esperado para la velocidad determinada. Si se desconoce el tiempo estimado (por ejemplo, la batería no se descarga y el valor de **AtRate** especificado es cero), el valor devuelto es BATTERY \_ UNKNOWN \_ TIME. Tenga en cuenta que este valor no es muy preciso en algunos sistemas de batería y puede variar ampliamente en función del uso actual de energía, lo que podría verse afectado por la actividad del disco y otros factores. No hay ningún mecanismo de notificación para los cambios en este valor.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | Matriz de estructuras [**BATTERY \_ REPORTING \_ SCALE,**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) nunca más de cuatro entradas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | Estructura [**BATTERY \_ INFORMATION.**](battery-information-str.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | Estructura [**BATTERY \_ MANUFACTURE \_ DATE.**](battery-manufacture-date-str.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | Cadena Unicode terminada en NULL que especifica el nombre del fabricante de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | Cadena Unicode terminada en NULL que especifica el número de serie de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | **ULONG que** especifica la temperatura actual de la batería, en 10ths of a degree Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | Cadena Unicode terminada en NULL que identifica de forma única la batería. Este valor se puede usar para realizar un seguimiento de una batería específica. En el caso de las baterías inteligentes, este identificador sería la concatenación del nombre del fabricante, el nombre del dispositivo, la fecha de fabricación y una representación imprimible del número de serie. <br/> Este valor no está pensado para mostrarse al usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

Este miembro solo se usa si **InformationLevel** es BatteryEstimatedTime.

Si este miembro es distinto de cero, es una velocidad de purga que se usará para calcular el tiempo hasta que se descargue la batería para el valor BatteryEstimatedTime de una batería individual. Debe especificarse en mW y debe ser un valor negativo para representar una velocidad de descarga de la batería.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cierta información sobre las baterías es opcional o puede no tener sentido para algunas baterías. Si el tipo concreto de datos solicitado no está disponible para la batería actual, se devuelve ERROR \_ INVALID \_ FUNCTION.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE \_ BATERÍA**](battery-information-str.md)
</dt> <dt>

[**FECHA DE \_ FABRICACIÓN DE \_ LA BATERÍA**](battery-manufacture-date-str.md)
</dt> <dt>

[**ESCALADO \_ DE INFORMES DE \_ BATERÍA**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**INFORMACIÓN DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**ETIQUETA DE CONSULTA \_ DE BATERÍA \_ DE IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




