---
description: Contiene información de la consulta de la batería.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: BATTERY_QUERY_INFORMATION estructura (Poclass. h)
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
ms.openlocfilehash: 511980dd4307077b8b160550c661a15a5714b96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909702"
---
# <a name="battery_query_information-structure"></a>Estructura de información de \_ consulta de batería \_

Contiene información de la consulta de la batería. Esta estructura se usa con el código de control de la [**\_ información de \_ consulta \_**](ioctl-battery-query-information.md) de la batería de ioctl para especificar el tipo de información que se va a devolver.

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

La etiqueta de la batería actual para la batería. Solo se puede devolver información de una batería que coincida con la etiqueta. Siempre que este valor no coincida con la etiqueta actual de la batería, se completará la solicitud IOCTL con el archivo de ERROR \_ \_ no \_ encontrado. Esto indica al llamador que la batería asociada a la etiqueta ya existe. El autor de la llamada puede optar por usar la operación de etiqueta de consulta de la [**\_ batería \_ \_ ioctl**](ioctl-battery-query-tag.md) para determinar la etiqueta de la batería recién instalada, si existe alguna. (Consulte [etiquetas de batería](battery-information.md) para obtener más información).

Cuando se realiza una solicitud de información de consulta, se comprueba este valor. Además, si la solicitud está en curso mientras este valor cambia, la solicitud se anula con el estado \_ \_ no se encontró el archivo de error \_ .

</dd> <dt>

**InformationLevel**
</dt> <dd>

El nivel de la información de la batería que se consulta. Los datos devueltos por IOCTL dependen de este valor. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | Cadena Unicode terminada en null que contiene el nombre de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | **ULong** que especifica el tiempo de ejecución estimado de la batería, en segundos. Si la tasa de purga proporcionada en el miembro **AtRate** de la estructura de **\_ \_ información de consulta** de la batería es cero, este cálculo se basa en la tasa de consumo actual. Si **AtRate** es distinto de cero, la hora devuelta es el tiempo de ejecución esperado para la tasa especificada. Si el tiempo estimado es desconocido (por ejemplo, la batería no se está descargando y el **AtRate** especificado era cero), el valor devuelto es el tiempo de la batería \_ desconocida \_ . Tenga en cuenta que este valor no es muy preciso en algunos sistemas de batería y puede variar considerablemente en función del uso de energía presente, que podría verse afectado por la actividad del disco y otros factores. No hay ningún mecanismo de notificación para los cambios en este valor.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | Una matriz de estructuras de [**\_ \_ escalado de informes de batería**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) , nunca más de cuatro entradas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | Estructura [**de \_ información**](battery-information-str.md) de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | Una estructura de [**\_ \_ fecha de fabricación**](battery-manufacture-date-str.md) de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | Cadena Unicode terminada en null que especifica el nombre del fabricante de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | Cadena Unicode terminada en null que especifica el número de serie de la batería.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | **ULong** que especifica la temperatura actual de la batería, en décimas de grado Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | Cadena Unicode terminada en null que identifica de forma única la batería. Este valor se puede usar para realizar el seguimiento de una batería específica. En el caso de las baterías inteligentes, este identificador sería la concatenación del nombre del fabricante, el nombre del dispositivo, la fecha de fabricación y una representación imprimible del número de serie. <br/> Este valor no está diseñado para mostrarse al usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

Este miembro se usa solo si **InformationLevel** es BatteryEstimatedTime.

Si este miembro es distinto de cero, se trata de una tasa de desagüe que se usará para calcular el tiempo hasta que se haya descargado la batería para el BatteryEstimatedTime de una batería individual. Debe especificarse en mW y debe ser un valor negativo para representar una tasa de descarga de la batería.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Parte de la información sobre las baterías es opcional o puede no tener sentido para algunas baterías. Si el tipo de datos solicitado no está disponible para la batería actual, se devuelve un ERROR de \_ función no válida \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de la batería \_**](battery-information-str.md)
</dt> <dt>

[**\_fecha de fabricación de la batería \_**](battery-manufacture-date-str.md)
</dt> <dt>

[**\_escala de informes de batería \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**\_información de \_ consulta de batería ioctl \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_etiqueta de \_ consulta ioctl Battery \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




