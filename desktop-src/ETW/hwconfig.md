---
description: La clase HWConfig es la clase primaria para los eventos de configuración de hardware en Windows XP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Clase HWConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913537"
---
# <a name="hwconfig-class"></a>Clase HWConfig

La clase **HWConfig** es la clase primaria para los eventos de configuración de hardware en Windows XP.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **HWConfig** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Estos eventos proporcionan la configuración de hardware del equipo. A diferencia de otros eventos del registrador del kernel de NT, la sesión del kernel genera automáticamente eventos de configuración de hardware; No habilite estos eventos al iniciar la sesión del registrador del kernel de NT.

**Windows 2000:** No compatible.

Para los eventos de configuración de hardware en Windows Vista y Windows Server 2003, vea la clase [SystemConfig](systemconfig.md) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de configuración de hardware llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de configuración de hardware real al consumir eventos.



| Tipo de evento                                                                      | Descripción                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de TRACE \_ Type \_ config \_ CPU**(el valor de tipo de evento es 10)<br/>          | Evento de configuración de CPU. Las clases MOF de [**HWConfig \_ CPU**](hwconfig-cpu.md) definen los datos de evento para este evento.                            |
| **Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ LOGICALDISK**(el valor de tipo de evento es 12)<br/>  | Evento de configuración de disco lógico. La clase MOF de las clases MOF de [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) define los datos de evento para este evento. |
| **Evento \_ de Tipo de seguimiento \_ \_ config de \_ NIC**(el valor de tipo de evento es 13)<br/>          | Evento de configuración de NIC. Las clases MOF de la [**\_ NIC HWConfig**](hwconfig-nic.md) definen los datos de evento para este evento.                            |
| **Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ DiscoFísico**(el valor de tipo de evento es 11)<br/> | Evento de configuración de disco físico. Las clases MOF de [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) definen los datos de evento para este evento.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_CPU HWConfig**](hwconfig-cpu.md)
</dt> <dt>

[**HWConfig \_ LogDisk**](hwconfig-logdisk.md)
</dt> <dt>

[**NIC de HWConfig \_**](hwconfig-nic.md)
</dt> <dt>

[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
