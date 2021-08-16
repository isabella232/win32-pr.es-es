---
description: Contiene la información de batería que se va a establecer.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION estructura (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: c53e9c539f8ef20b184c6c056999c7c541f3c1718bafaa58c0b1e20dcef16a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143618"
---
# <a name="battery_set_information-structure"></a>BATTERY \_ SET \_ INFORMATION (estructura)

Contiene la información de batería que se va a establecer. Esta estructura se usa con el código de control [**\_ IOCTL BATTERY \_ SET \_ INFORMATION.**](ioctl-battery-set-information.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BatteryTag**
</dt> <dd>

La etiqueta de batería actual de la batería. Solo se puede devolver información de una batería que coincida con la etiqueta. Siempre que este valor no coincida con la etiqueta actual de la batería, la solicitud IOCTL se completará con ERROR FILE NOT FOUND, que indica al autor de la llamada que la batería para la que tiene una etiqueta \_ \_ ya no \_ existe. El autor de la llamada puede optar por usar la operación [**IOCTL \_ BATTERY QUERY \_ \_ TAG**](ioctl-battery-query-tag.md) para determinar la etiqueta de la batería recién instalada, si existe. (Consulte [Etiquetas de batería](battery-information.md) para obtener más información).

Cuando se realiza una solicitud de información de consulta, se comprueba este valor. Además, si la solicitud está en curso mientras este valor cambia, la solicitud se anula con el estado ERROR \_ FILE \_ NOT \_ FOUND.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Información de la batería que se va a establecer. El tipo de datos del miembro **Buffer** depende del valor de este miembro. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Informa al dispositivo de batería que el usuario ha solicitado que la batería se cargue en este momento. Por ejemplo, con una batería inteligente, un cargador o un selector, la aplicación podría cargar una batería a la vez. Se **omite** el miembro Buffer de esta estructura.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Establece el ajuste de sesgo crítico de la batería. Tenga en cuenta que no está previsto que este valor lo cambie normalmente el software y solo esté presente en las interfaces como una característica de mantenimiento. No todas las baterías pueden mantener este tipo de configuración y se debe leer la información de la batería para confirmar que la batería aceptó la configuración.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Informa al dispositivo de batería que el usuario ha solicitado que la batería se esté descargando en este momento. Por ejemplo, esto podría usarse para indicar la batería que el usuario quiere actualmente para encender el sistema. Se **omite** el miembro Buffer de esta estructura.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

Información de la batería que se va a establecer. Los datos dependen del valor de **InformationLevel.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura BATTERY SET \_ \_ INFORMATION** es una estructura de longitud variable y debe asignar un búfer de tamaño adecuado para que la información se incluya en la estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DEL CONJUNTO \_ DE \_ BATERÍAS DE IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




