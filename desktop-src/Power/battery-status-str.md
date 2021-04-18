---
description: Contiene el estado actual de la batería.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: BATTERY_STATUS estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667222"
---
# <a name="battery_status-structure"></a>Estructura de estado de la batería \_

Contiene el estado actual de la batería. Esta estructura la usa el código de control de [**\_ Estado de \_ consulta \_**](ioctl-battery-query-status.md) de la batería de ioctl.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**PowerState**
</dt> <dd>

Estado de la batería. Este miembro puede ser cero, uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                   | Significado                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Batería \_ de Cargando**</dt> <dt>0x00000004</dt> </dl>                  | Indica que la batería se está cargando actualmente.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Batería \_ de**</dt> <dt>0x00000008</dt> crítico </dl>                  | Indica que el error de la batería es inminente. Vea la sección Comentarios para obtener más información.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Batería \_ de Descargar**</dt> <dt>0x00000002</dt> </dl>         | Indica que la batería se está descargando actualmente.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Batería \_ de ENCENDIDO \_ en la \_ línea**</dt> <dt>0x00000001</dt> </dl> | Indica que el sistema tiene acceso a la corriente alterna, por lo que no se está aplicando ninguna batería.<br/>   |



 

</dd> <dt>

**Capacity**
</dt> <dd>

La capacidad actual de la batería, en mWh (o relativa). Este valor se puede usar para generar una presentación de "medidor de gas" dividiéndolo por el miembro **FullChargedCapacity** de la estructura de [**\_ información**](battery-information-str.md) de la batería. Si la capacidad no está disponible, este miembro tiene una capacidad desconocida de la batería \_ \_ .

</dd> <dt>

**Voltaje**
</dt> <dd>

La tensión de la batería actual a través de los terminales de la batería, en milivoltios (MV). Si el voltaje no está disponible, este miembro es una tensión desconocida de la batería \_ \_ .

</dd> <dt>

**Tarifa**
</dt> <dd>

La tasa actual de carga o descarga de la batería. Este valor estará en milivatios a menos que la información sobre la frecuencia de la batería sea relativa, en cuyo caso estará en unidades arbitrarias por hora. Para determinar si la información de la batería es relativa, examine la \_ marca relativa de la capacidad de la batería \_ en el miembro **Capabilities** de la estructura de [**\_ información**](battery-information-str.md) de la batería. Un valor distinto de cero, la tasa positiva indica la carga; una tasa negativa indica la descargación. Algunas baterías solo indican tarifas de descargado. Si la tasa no está disponible, este miembro tiene una tasa de batería \_ desconocida \_ . Si cambia el estado de la batería o de la fuente de alimentación, la velocidad puede estar disponible.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La marca crítica de la batería del \_ miembro **PowerState** de esta estructura indica una condición de "batería crítica" de hardware. Este nivel crítico está establecido por el fabricante de la batería, no por el usuario en la "alarma de batería crítica". Por lo general, significa que el sistema de batería ha calculado que la batería está completamente drenada y cualquier potencia que se está dibujando está más allá de lo esperado.

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

[**Estado de la \_ consulta de batería ioctl \_ \_**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




