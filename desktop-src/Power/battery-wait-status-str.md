---
description: Contiene información sobre las condiciones en las que se va a recuperar el estado de la batería.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: BATTERY_WAIT_STATUS estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667221"
---
# <a name="battery_wait_status-structure"></a>Estructura de estado de \_ espera de batería \_

Contiene información sobre las condiciones en las que se va a recuperar el estado de la batería. Esta estructura la usa el código de control de [**\_ Estado de \_ consulta \_**](ioctl-battery-query-status.md) de la batería de ioctl.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BatteryTag**
</dt> <dd>

La etiqueta de la batería actual para la batería. Solo se puede devolver información de una batería que coincida con la etiqueta. Cuando este valor no coincide con la etiqueta actual de la batería, se producirá un error en la operación [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con un código de error \_ \_ no \_ encontrado, lo que indica al autor de la llamada que la batería para la que tiene una etiqueta ya no está instalada, el autor de la llamada puede optar por usar la operación de etiqueta de consulta de batería de ioctl para determinar la etiqueta de la batería recién [**\_ \_ \_**](ioctl-battery-query-tag.md) Además, si la solicitud está en curso cuando se quita la batería o la etiqueta cambia, la operación se anula con el estado \_ \_ no se encontró el archivo de error \_ . (Consulte [etiquetas de batería](battery-information.md) para obtener más información).

</dd> <dt>

**Tiempo de espera**
</dt> <dd>

Número de milisegundos que la solicitud esperará a la condición especificada por los miembros **PowerState**, **LowCapacity** y **HighCapacity** antes de completarse. Un valor de-1 indica que la solicitud esperará indefinidamente a que se cumplan las condiciones. Un valor de cero indica que la información de batería solicitada se devolverá inmediatamente, independientemente de las demás condiciones. Cualquier otro valor indica que la solicitud debe esperar el período de tiempo o hasta que se cumpla alguna de las demás condiciones.

Si el equipo ha entrado en modo de suspensión, el reloj seguirá ejecutándose, pero el recuento no volverá a activar el equipo. Si el recuento se agota cuando el equipo es awoken y se cumplen otras condiciones, la llamada se devolverá inmediatamente al activar.

</dd> <dt>

**PowerState**
</dt> <dd>

Cero, uno o varios de los siguientes bits de estado, que indican el estado de la batería. Es idéntico al miembro **PowerState** de la estructura de [**\_ Estado**](battery-status-str.md) de la batería.



| Value                                                                                                                                                                                                                                                   | Significado                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Batería \_ de Cargando**</dt> <dt>0x00000004</dt> </dl>                  | Indica que la batería se está cargando actualmente.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Batería \_ de**</dt> <dt>0x00000008</dt> crítico </dl>                  | Indica que el error de la batería es inminente. Vea la sección Comentarios para obtener más información.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Batería \_ de Descargar**</dt> <dt>0x00000002</dt> </dl>         | Indica que la batería se está descargando actualmente.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Batería \_ de ENCENDIDO \_ en la \_ línea**</dt> <dt>0x00000001</dt> </dl> | Indica que la batería tiene acceso a la corriente alterna.<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

La capacidad actual de la batería, en mWh (o relativa). Este valor es idéntico al miembro **Capacity** de la estructura de [**\_ Estado**](battery-status-str.md) de la batería.

</dd> <dt>

**HighCapacity**
</dt> <dd>

La capacidad actual de la batería, en mWh (o relativa). Este valor es idéntico al miembro **Capacity** de la estructura de [**\_ Estado**](battery-status-str.md) de la batería.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las solicitudes de información de la batería se posponen hasta que se produce uno de los siguientes casos:

-   El tiempo de espera expira (suponiendo que el tiempo de **espera** no es-1).
-   El estado actual de la batería no coincide con **PowerState**.
-   La capacidad de la batería es inferior a **LowCapacity**.
-   La capacidad de la batería está por encima de **HighCapacity**.
-   La etiqueta de la batería cambia.

Cuando se cumple alguna de estas condiciones, se recopilan los datos y se devuelve la operación. Esto permite a las aplicaciones supervisar la información de batería dinámica normal sin sondear el dispositivo.

Antes de usar cualquiera de las dos condiciones de capacidad, asegúrese de que la batería las admita mediante el código de control de [**\_ Estado de \_ consulta \_**](ioctl-battery-query-status.md) de la batería de ioctl con un tiempo de espera de cero. Examine los resultados para determinar si se admite el miembro **Capacity** (es decir, no es una capacidad desconocida de la batería \_ \_ ).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estado de la batería \_**](battery-status-str.md)
</dt> <dt>

[**Estado de la \_ consulta de batería ioctl \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_etiqueta de \_ consulta ioctl Battery \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

