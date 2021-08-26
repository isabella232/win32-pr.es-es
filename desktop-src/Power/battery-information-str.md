---
description: Contiene información sobre la batería.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION estructura (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: c449f325e03fb4ea81fe0aa148eaddcf65800b5a56356e22232477e0b6d4fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033015"
---
# <a name="battery_information-structure"></a>Estructura BATTERY \_ INFORMATION

Contiene información sobre la batería. El código de control [**IOCTL \_ BATTERY QUERY \_ \_ INFORMATION**](ioctl-battery-query-information.md) devuelve esta estructura cuando se solicita el nivel de información BatteryInformation.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Capabilities**
</dt> <dd>

Capacidades de batería. Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**BATERÍA \_ CAPACIDAD \_ RELATIVA**</dt> <dt>0x40000000</dt> </dl>                    | Indica que la información de capacidad y velocidad de la batería es relativa y no está en ninguna unidad específica. Si no se establece este bit, las unidades de informes son milivatios-hora (mWh) para la capacidad y milivatios (mW) para la velocidad. Si se establece este bit, se pueden omitir todas las referencias a las unidades de la otra documentación de la batería. Toda la información de velocidad se notifica en unidades por hora. Por ejemplo, si la capacidad totalmente cargada se notifica como 100, una velocidad de 200 indica que la batería usará toda su capacidad en media hora.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**BATERÍA \_ ¿ES \_ \_ una 0x20000000**</dt> <dt></dt> </dl>                               | Indica que la operación normal es para una función con seguridad de errores. Si no se establece este bit, se espera que la batería se utilice durante el uso normal del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**BATERÍA \_ SET \_ CHARGE \_ SUPPORTED**</dt> <dt>0x00000001</dt> </dl>          | Indica que este dispositivo de batería admite las solicitudes de información establecidas del tipo BatteryCharge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**BATERÍA \_ ESTABLECER \_ LA LICENCIA ADMITIDA \_ 0X00000002**</dt> <dt></dt> </dl> | Indica que este dispositivo de batería admite las solicitudes de información establecidas del tipo BatteryDischarge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**BATERÍA \_ BATERÍA \_ DEL**</dt> <dt>SISTEMA 0x80000000</dt> </dl>                             | Indica que la batería puede proporcionar energía general para ejecutar el sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Technology**
</dt> <dd>

Tecnología de batería. Este miembro puede ser uno de los siguientes valores.



| Value                                                                        | Significado                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Batería no recuperable, por ejemplo, alkaline.<br/> |
| <dl> <dt>1</dt> </dl> | Batería de batería de batería, por ejemplo, acido de lead.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Química**
</dt> <dd>

Cadena de caracteres abreviada que indica la química de la batería. Esta cadena no termina necesariamente en cero. A continuación se muestra una lista parcial de abreviaturas que se pueden devolver y las entradas asociadas.



| Cadena de Unicode                                                                                                                                           | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Plomo<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**León**</dt> </dl>                        | Ion de iones de<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Ion de iones de<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**Nicd**</dt> </dl> | Níquel-cadmio<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**Nimh**</dt> </dl> | Hydride metal de metal de metal de metal<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**NiZn**</dt> </dl> | Desmaeso<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Alkaline-Manganese<br/> |



 

Puede que aparezcan otras entradas en el futuro y que el código pueda controlarlas.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

La capacidad teórica de la batería cuando es nueva, en mWh a menos que se establezca BATTERY \_ CAPACITY \_ RELATIVE. En ese caso, las unidades no están definidas.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

La capacidad de carga completa actual de la batería en mWh (o relativa). Compare este valor con **DesignedCapacity para** calcular el rendimiento de la batería.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

Capacidad sugerida por el fabricante, en mWh, en la que debe producirse una alerta de batería baja. Las definiciones de bajo varían de fabricante a fabricante. En general, se producirá un estado de advertencia antes de un estado bajo, pero no debe suponer que siempre lo hará. Para reducir el riesgo de pérdida de datos, este valor se usa normalmente como configuración predeterminada para la alarma de batería crítica.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

Capacidad sugerida por el fabricante, en mWh, en la que debe producirse una alerta de batería de advertencia. Las definiciones de advertencia varían de fabricante a fabricante. En general, se producirá un estado de advertencia antes de un estado bajo, pero no debe suponer que siempre lo hará. Para reducir el riesgo de pérdida de datos, este valor normalmente se usa como la configuración predeterminada para la alarma de batería baja.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Un sesgo de cero, en mWh, que se aplica a los informes de batería. Algunas baterías reservan una pequeña carga que se diferencia de los valores de capacidad de la batería para mostrar "0" como el nivel de batería crítico. El sesgo crítico es análogo a la configuración de un medidor de combustible para que se muestre "vacío" cuando quedan varios depósitos de combustible.

</dd> <dt>

**CycleCount**
</dt> <dd>

Número de ciclos de carga y descarga que ha experimentado la batería. Esto proporciona un medio para determinar el uso de la batería. Si la batería no admite un contador de ciclo, este miembro es cero.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Por lo general, se produce un estado de advertencia antes de un estado bajo, pero no debe suponer que lo hará. Es posible sondear una batería y averiguar que no se ha producido ningún nivel de alerta, sondear la batería de nuevo y encontrarla descargada en la medida en que se hayan alcanzado ambos niveles. Esto puede indicar que no está sondando con suficiente frecuencia. También puede indicar que la batería no puede contener una carga durante mucho tiempo y se descarga más rápidamente de lo esperado. Este tipo de batería puede estar cerca del final de su vida útil o puede estar dañada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




