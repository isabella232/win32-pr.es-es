---
description: Contiene la información de la batería que se va a establecer.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION estructura (Poclass. h)
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
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156520"
---
# <a name="battery_set_information-structure"></a>Estructura de información de \_ conjunto de batería \_

Contiene la información de la batería que se va a establecer. Esta estructura se usa con el código de control de [**información del conjunto de baterías de ioctl \_ \_ \_**](ioctl-battery-set-information.md) .

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

La etiqueta de la batería actual para la batería. Solo se puede devolver información de una batería que coincida con la etiqueta. Siempre que este valor no coincida con la etiqueta actual de la batería, se completará la solicitud IOCTL con el archivo de ERROR \_ \_ no \_ encontrado, que indica al autor de la llamada que ya no existe la batería para la que tiene una etiqueta. El autor de la llamada puede optar por usar la operación de etiqueta de consulta de la [**\_ batería \_ \_ ioctl**](ioctl-battery-query-tag.md) para determinar la etiqueta de la batería recién instalada, si existe alguna. (Consulte [etiquetas de batería](battery-information.md) para obtener más información).

Cuando se realiza una solicitud de información de consulta, se comprueba este valor. Además, si la solicitud está en curso mientras este valor cambia, la solicitud se anula con el estado \_ \_ no se encontró el archivo de error \_ .

</dd> <dt>

**InformationLevel**
</dt> <dd>

Información de la batería que se va a establecer. El tipo de datos del miembro de **búfer** depende del valor de este miembro. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Informa al dispositivo de la batería de que el usuario ha solicitado que la batería se debe cargar en este momento. Por ejemplo, con una batería/cargador/selector inteligentes, la aplicación podría cobrar una batería a la vez. Se omite el miembro de **búfer** de esta estructura.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Establece el ajuste de la diferencia crítica de la batería. Tenga en cuenta que no se ha aprovisionado que este valor lo cambiaría normalmente el software, y está presente en las interfaces solo como una característica de mantenimiento. No todas las baterías pueden mantener este valor y se debe leer la información de la batería para confirmar que la batería aceptó la configuración.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Informa al dispositivo de la batería de que el usuario ha solicitado que la batería se esté descargando en este momento. Por ejemplo, se podría usar para indicar qué batería desea que el usuario desee alimentar el sistema actualmente. Se omite el miembro de **búfer** de esta estructura.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

Información de la batería que se va a establecer. Los datos dependen del valor de **InformationLevel**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **\_ \_ información del conjunto de batería** es una estructura de longitud variable y debe asignar un búfer de tamaño adecuado para la información que se va a incluir en la estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_información del \_ conjunto de baterías de ioctl \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




