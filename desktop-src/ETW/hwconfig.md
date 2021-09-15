---
description: La clase HWConfig es la clase primaria para los eventos de configuración de hardware Windows XP. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: HWConfig (clase)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476895"
---
# <a name="hwconfig-class"></a>HWConfig (clase)

La **clase HWConfig** es la clase primaria para los eventos de configuración de hardware Windows XP.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **clase HWConfig** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Estos eventos proporcionan la configuración de hardware del equipo. A diferencia de otros eventos del registrador de kernel de NT, la sesión del kernel genera automáticamente eventos de configuración de hardware; estos eventos no se habilitan al iniciar la sesión del registrador de kernel de NT.

**Windows 2000:** No se admite.

Para los eventos de configuración de hardware Windows Vista y Windows Server 2003, consulte la [clase SystemConfig.](systemconfig.md)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de configuración de hardware llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como el *parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento de configuración de hardware real al consumir eventos.



| Tipo de evento                                                                      | Descripción                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(el valor del tipo de evento es 10)<br/>          | Evento de configuración de CPU. Las [**clases HWConfig \_ CPU**](hwconfig-cpu.md) MOF definen los datos de evento para este evento.                            |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(el valor del tipo de evento es 12)<br/>  | Evento de configuración de disco lógico. La clase MOF de las clases MOF [**de HwConfig \_ LogDisk**](hwconfig-logdisk.md) define los datos de evento para este evento. |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NIC**(el valor del tipo de evento es 13)<br/>          | Evento de configuración de NIC. Las [**clases MOF \_ de NIC HWConfig**](hwconfig-nic.md) definen los datos de evento para este evento.                            |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(el valor del tipo de evento es 11)<br/> | Evento de configuración de disco físico. Las [**clases HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF definen los datos de evento para este evento.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**HWConfig \_ CPU**](hwconfig-cpu.md)
</dt> <dt>

[**HWConfig \_ LogDisk**](hwconfig-logdisk.md)
</dt> <dt>

[**HWConfig \_ NIC**](hwconfig-nic.md)
</dt> <dt>

[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
