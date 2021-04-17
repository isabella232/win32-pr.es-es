---
description: Contiene información de la batería.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION estructura (Poclass. h)
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
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667226"
---
# <a name="battery_information-structure"></a>Estructura de información de la batería \_

Contiene información de la batería. Esta estructura la devuelve el código de control de la [**\_ información de \_ consulta \_**](ioctl-battery-query-information.md) de la batería de ioctl cuando se solicita el nivel de información de BatteryInformation.

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

Las capacidades de la batería. Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**Batería \_ de 0x40000000 \_ relativo**</dt> a la capacidad <dt></dt> </dl>                    | Indica que la capacidad de la batería y la información de velocidad son relativas, y no en unidades específicas. Si no se establece este bit, las unidades de informe son milivatios-Hours (mWh) para Capacity y milivatios (mW) para Rate. Si se establece este bit, se pueden omitir todas las referencias a las unidades de la documentación de la otra batería. Toda la información de tarifas se registra en unidades por hora. Por ejemplo, si la capacidad de carga completa se indica como 100, una tarifa de 200 indica que la batería usará toda su capacidad en media hora.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**Batería \_ de ES 0x20000000 a \_ corto \_ plazo**</dt> <dt></dt> </dl>                               | Indica que la operación normal es para una función a la que se ha producido un error. Si no se establece este bit, se espera que la batería se use durante el uso normal del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**Batería \_ de SET \_ Charge \_ support compatible**</dt> <dt>0x00000001</dt> </dl>          | Indica que este dispositivo de batería admite las solicitudes Set Information del tipo BatteryCharge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**Batería \_ de ESTABLECER la \_ descarga \_ compatible**</dt> <dt>0x00000002</dt> </dl> | Indica que este dispositivo de batería admite las solicitudes Set Information del tipo BatteryDischarge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**Batería \_ de \_Batería del sistema**</dt> <dt>0x80000000</dt> </dl>                             | Indica que la batería puede proporcionar alimentación general para ejecutar el sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Technology**
</dt> <dd>

La tecnología de la batería. Este miembro puede ser uno de los valores siguientes.



| Value                                                                        | Significado                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Batería no recargable, por ejemplo, alcalina.<br/> |
| <dl> <dt>1</dt> </dl> | Batería recargable, por ejemplo, acid plomo.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Químicos**
</dt> <dd>

Cadena de caracteres abreviada que indica la química de la batería. Esta cadena no es necesariamente terminada en cero. La siguiente es una lista parcial de abreviaturas que se pueden devolver y los chemistries asociados.



| Cadena de Unicode                                                                                                                                           | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Acid inicial<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**LION**</dt> </dl>                        | Ion de litio<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Ion de litio<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**NiCd**</dt> </dl> | Níquel cadmio<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**NiMH**</dt> </dl> | Hidruro de níquel metal<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**NiZn**</dt> </dl> | Cinc de níquel<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Alkaline-Manganese recargable<br/> |



 

Otros chemistries pueden aparecer en el futuro y el código debería ser capaz de controlarlos.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

La capacidad teórica de la batería cuando es nuevo, en mWh a menos que se establezca la capacidad de la batería \_ \_ relativa. En ese caso, las unidades son indefinidas.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

La capacidad total actual de la batería en mWh (o relativa). Compare este valor con **DesignedCapacity** para estimar el desgaste de la batería.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

La capacidad sugerida del fabricante, en mWh, en la que debe producirse una alerta de batería baja. Las definiciones de Low varían según el fabricante. En general, un estado de advertencia se produce antes de un estado bajo, pero no se debe suponer que siempre lo sea. Para reducir el riesgo de pérdida de datos, este valor se utiliza normalmente como configuración predeterminada para la alarma de batería crítica.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

La capacidad sugerida del fabricante, en mWh, en la que debe producirse una alerta de batería de advertencia. Las definiciones de advertencia varían de un fabricante a un fabricante. En general, un estado de advertencia se produce antes de un estado bajo, pero no se debe suponer que siempre lo sea. Para reducir el riesgo de pérdida de datos, este valor se utiliza normalmente como configuración predeterminada para la alarma de batería baja.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Una diferencia de cero, en mWh, que se aplica a los informes de batería. Algunas baterías reservan una pequeña carga que se sesga de los valores de capacidad de la batería para mostrar "0" como nivel crítico de batería. La diferencia crítica es análoga a la configuración de un medidor de combustible para mostrar "vacío" cuando hay varios litros de combustible a la izquierda.

</dd> <dt>

**CycleCount**
</dt> <dd>

El número de ciclos de carga/descarga que ha experimentado la batería. Esto proporciona un medio para determinar el desgaste de la batería. Si la batería no admite un contador de ciclo, este miembro es cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Por lo general, un estado de advertencia se produce antes de un estado bajo, pero no se debe suponer que lo sea. Es posible sondear una batería y detectar que no se ha producido el nivel de alerta y, a continuación, volver a sondear la batería y encontrarla descargada en la medida en que se hayan conseguido ambos niveles. Esto puede indicar que no está sondeando a menudo lo suficiente. También puede indicar que la batería no puede ocupar mucho tiempo y se está descargando más rápidamente de lo esperado. Es posible que esta batería esté llegando al final de su vida útil o que esté dañada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_información de \_ consulta de batería ioctl \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




