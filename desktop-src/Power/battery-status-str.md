---
description: Contiene el estado actual de la batería.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: BATTERY_STATUS estructura (Poclass.h)
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
ms.openlocfilehash: 28b75a8eb1c7abf647f3f8ea61b29dedb40978f3ea639fc505364a12ae5e57cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143608"
---
# <a name="battery_status-structure"></a>BATTERY \_ STATUS (estructura)

Contiene el estado actual de la batería. El código de control IOCTL BATTERY QUERY STATUS usa [**\_ \_ \_ esta**](ioctl-battery-query-status.md) estructura.

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
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**BATERÍA \_ Carga de**</dt> <dt>0x00000004</dt> </dl>                  | Indica que la batería se está cargando actualmente.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**BATERÍA \_ Crítico**</dt> <dt>0x00000008</dt> </dl>                  | Indica que el error de la batería es inminente. Vea la sección Comentarios para obtener más información.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**BATERÍA \_ Descarga de**</dt> <dt>0x00000002</dt> </dl>         | Indica que la batería se está descargando actualmente.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**BATERÍA \_ Power \_ ON \_ LINE**</dt> <dt>0x00000001</dt> </dl> | Indica que el sistema tiene acceso a la alimentación de ca, por lo que no se descargan baterías.<br/>   |



 

</dd> <dt>

**Capacity**
</dt> <dd>

La capacidad actual de la batería, en mWh (o relativa). Este valor se puede usar para generar una presentación de "medidor de gas" dividiéndola por el miembro **FullChargedCapacity** de la estructura [**BATTERY \_ INFORMATION.**](battery-information-str.md) Si la capacidad no está disponible, este miembro es BATTERY \_ UNKNOWN \_ CAPACITY.

</dd> <dt>

**Voltaje**
</dt> <dd>

El voltaje actual de la batería en los terminales de la batería, en milivoltios (mv). Si el voltaje no está disponible, este miembro es BATTERY \_ UNKNOWN \_ VOLTAGE.

</dd> <dt>

**Tarifa**
</dt> <dd>

La tasa actual de carga o descarga de la batería. Este valor estará en milivatios a menos que la información de la velocidad de la batería sea relativa, en cuyo caso estará en unidades arbitrarias por hora. Para determinar si la información de la batería es relativa, examine la marca BATTERY CAPACITY RELATIVE en el \_ miembro Capabilities de la estructura BATTERY \_ [**\_ INFORMATION.**](battery-information-str.md)  Una tasa positiva distinta de cero indica la carga; una tasa negativa indica la descarga. Algunas baterías solo informan de las tarifas de descarga. Si la tarifa no está disponible, este miembro es BATTERY \_ UNKNOWN \_ RATE. Si cambia el estado de la batería o la fuente de alimentación, la velocidad puede estar disponible.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La marca BATTERY \_ CRITICAL en el miembro **PowerState** de esta estructura indica una condición de hardware "crítico para la batería". Este nivel crítico lo establece el fabricante de la batería, no el usuario en la "alarma de batería crítica". Por lo general, significa que el sistema de baterías ha calculado que la batería está totalmente agotada y que cualquier energía que se extrae está por encima de lo esperado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE \_ LA BATERÍA**](battery-information-str.md)
</dt> <dt>

[**ESTADO DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




