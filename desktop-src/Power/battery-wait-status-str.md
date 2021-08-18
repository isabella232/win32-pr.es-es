---
description: Contiene información sobre las condiciones en las que se va a recuperar el estado de la batería.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: BATTERY_WAIT_STATUS estructura (Poclass.h)
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
ms.openlocfilehash: 52885b75c7f9afba7ff336b3210ecf1b852f85b0091afe13026616816e43d7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143598"
---
# <a name="battery_wait_status-structure"></a>Estructura BATTERY \_ WAIT \_ STATUS

Contiene información sobre las condiciones en las que se va a recuperar el estado de la batería. El código de control ESTADO DE LA CONSULTA [**DE LA BATERÍA de IOCTL usa \_ \_ \_ esta**](ioctl-battery-query-status.md) estructura.

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

La etiqueta de batería actual de la batería. Solo se puede devolver información de una batería que coincida con la etiqueta. Siempre que este valor no coincida con la etiqueta actual de la batería, se producirá un error en la operación [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con un código de error ERROR FILE NOT FOUND, que indica al autor de la llamada que la batería para la que tiene una etiqueta ya no está instalada. El autor de la llamada puede optar por usar la operación \_ \_ \_ [**IOCTL BATTERY \_ \_ QUERY \_ TAG**](ioctl-battery-query-tag.md) para determinar la etiqueta de la batería recién instalada, si existe. Además, si la solicitud está en curso cuando se quita la batería o la etiqueta cambia, la operación se anula con el estado ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO. (Consulte [Etiquetas de batería](battery-information.md) para obtener más información).

</dd> <dt>

**Tiempo de espera**
</dt> <dd>

Número de milisegundos que la solicitud esperará a la condición especificada por los miembros **PowerState,** **LowCapacity** y **HighCapacity** antes de completarse. Un valor de -1 indica que la solicitud esperará indefinidamente a que se cumplen las condiciones. Un valor de cero indica que la información de la batería solicitada se devolverá inmediatamente, independientemente de las demás condiciones. Cualquier otro valor indica que la solicitud debe esperar ese período de tiempo o hasta que se cumple cualquiera de las otras condiciones.

Si el equipo ha entrado en modo de suspensión, el reloj seguirá en ejecución, pero agotando el recuento no reactivará el equipo. Si el recuento se agota cuando se desaconsja el equipo y se cumplen otras condiciones, la llamada volverá inmediatamente al volver a la mente.

</dd> <dt>

**PowerState**
</dt> <dd>

Cero, uno o varios de los siguientes bits de estado, que indican el estado de la batería. Es idéntico al miembro **PowerState** de la estructura [**BATTERY \_ STATUS.**](battery-status-str.md)



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**BATTERY \_ Carga**</dt> <dt>0x00000004</dt> </dl>                  | Indica que la batería se está cargando actualmente.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**BATTERY \_ Información**</dt> <dt>0x00000008</dt> </dl>                  | Indica que el error de batería es inminente. Vea la sección Comentarios para obtener más información.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**BATTERY \_ Descarga de**</dt> <dt>0x00000002</dt> </dl>         | Indica que la batería se está descargando actualmente.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**BATTERY \_ Power \_ ON \_ LINE**</dt> <dt>0x00000001</dt> </dl> | Indica que la batería tiene acceso a la alimentación de ca.<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

La capacidad actual de la batería, en mWh (o relativa). Este valor es idéntico al miembro **Capacity de** la estructura [**BATTERY \_ STATUS.**](battery-status-str.md)

</dd> <dt>

**HighCapacity**
</dt> <dd>

La capacidad actual de la batería, en mWh (o relativa). Este valor es idéntico al miembro **Capacity de** la estructura [**BATTERY \_ STATUS.**](battery-status-str.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las solicitudes de información de batería se posponen hasta que se produce una de las siguientes situaciones:

-   El tiempo de espera expira (suponiendo que **timeout** no sea -1).
-   El estado actual de la batería no coincide con **PowerState.**
-   La capacidad de la batería está por **debajo de LowCapacity.**
-   La capacidad de la batería está por encima **de HighCapacity.**
-   La etiqueta de batería cambia.

Cuando se cumple alguna de estas condiciones, se recopilan los datos y se devuelve la operación. Esto permite a las aplicaciones supervisar la información típica de la batería dinámica sin sondear el dispositivo.

Antes de usar cualquiera de las dos condiciones de capacidad, asegúrese de que la batería las admite mediante el código de control ESTADO DE CONSULTA DE LA BATERÍA DE IOCTL con un tiempo de espera de cero. [**\_ \_ \_**](ioctl-battery-query-status.md) Examine los resultados para determinar si se admite el miembro **Capacity** (es decir, no BATTERY \_ UNKNOWN \_ CAPACITY).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ESTADO DE \_ LA BATERÍA**](battery-status-str.md)
</dt> <dt>

[**ESTADO DE CONSULTA \_ DE LA BATERÍA \_ DE IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**ETIQUETA DE CONSULTA \_ DE BATERÍA \_ DE IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

