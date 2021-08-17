---
description: La clase HWConfig es la clase primaria para los eventos de configuración de hardware en Windows XP. La sintaxis siguiente se simplifica a partir del código MOF.
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
ms.openlocfilehash: e1d4b8f69784729ffe5d51f3068b03fc0b4154182b2d05f2896e4556a05f7eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394685"
---
# <a name="hwconfig-class"></a>HWConfig (clase)

La **clase HWConfig** es la clase primaria para los eventos de configuración de hardware en Windows XP.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase HWConfig** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Estos eventos proporcionan la configuración de hardware del equipo. A diferencia de otros eventos del registrador de kernel de NT, la sesión del kernel genera automáticamente eventos de configuración de hardware; no se habilitan estos eventos al iniciar la sesión del registrador de kernel nt.

**Windows 2000:** No se admite.

Para eventos de configuración de hardware en Windows Vista y Windows Server 2003, vea la [clase SystemConfig.](systemconfig.md)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de configuración de hardware llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y [**especificando EventTraceConfigGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar el evento de configuración de hardware real al consumir eventos.



| Tipo de evento                                                                      | Descripción                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(el valor del tipo de evento es 10)<br/>          | Evento de configuración de CPU. Las [**clases HWConfig \_ CPU**](hwconfig-cpu.md) MOF definen los datos de evento para este evento.                            |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(el valor del tipo de evento es 12)<br/>  | Evento de configuración de disco lógico. La clase MOF de las clases MOF [**de HWConfig \_ LogDisk**](hwconfig-logdisk.md) define los datos de evento para este evento. |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ NIC**(el valor del tipo de evento es 13)<br/>          | Evento de configuración de NIC. Las [**clases MOF \_ de NIC HWConfig**](hwconfig-nic.md) definen los datos de evento para este evento.                            |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(el valor del tipo de evento es 11)<br/> | Evento de configuración de disco físico. Las [**clases MOF \_ de HWConfig PhyDisk**](hwconfig-phydisk.md) definen los datos de evento para este evento.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                   |



## <a name="see-also"></a>Consulte también

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

 

 
