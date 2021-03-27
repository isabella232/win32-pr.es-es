---
description: Esta clase es la clase primaria para los eventos de configuración de hardware. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: Clase SystemConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913906"
---
# <a name="systemconfig-class"></a>Clase SystemConfig

Esta clase es la clase primaria para los eventos de configuración de hardware.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **SystemConfig** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Estos eventos proporcionan la configuración de hardware del equipo. A diferencia de otros eventos del registrador del kernel de NT, la sesión del kernel genera automáticamente eventos de configuración de hardware; No habilite estos eventos al iniciar la sesión del registrador del kernel de NT.

Para los eventos de configuración de hardware en Windows XP, vea la clase [HWConfig](hwconfig.md) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de configuración de hardware llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de configuración de hardware real al consumir eventos.



| Tipo de evento                                                                      | Descripción                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de TRACE \_ Type \_ config \_ CPU**(el valor de tipo de evento es 10)<br/>          | Evento de configuración de CPU. Las clases MOF de [**SystemConfig \_ CPU**](systemconfig-cpu.md) definen los datos de evento para este evento.                                                       |
| **Evento \_ de TRACE \_ Type \_ config \_ IDECHANNEL**(el valor de tipo de evento es 23)<br/>   | Evento de configuración de canal IDE principal y secundario. La clase MOF de las clases MOF de [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) define los datos de evento para este evento. |
| **Evento \_ de TRACE \_ Type \_ config \_ IRQ**(el valor de tipo de evento es 21)<br/>          | Evento de solicitud de interrupción (IRQ). La clase MOF [**SystemConfig \_ IRQ**](systemconfig-irq.md) de las clases mof define los datos de evento para este evento.                                       |
| **Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ LOGICALDISK**(el valor de tipo de evento es 12)<br/>  | Evento de configuración de disco lógico. La clase MOF de las clases MOF de [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) define los datos de evento para este evento.                            |
| **Evento \_ de TRACE \_ Type \_ config \_ NETINFO**(el valor de tipo de evento es 17)<br/>      | Evento iformation de red. La clase MOF de [**\_ red SystemConfig**](systemconfig-network.md) define los datos de evento para este evento.                                                |
| **Evento \_ de Tipo de seguimiento \_ \_ config de \_ NIC**(el valor de tipo de evento es 13)<br/>          | Evento de configuración de NIC. Las clases MOF de la [**\_ NIC SystemConfig**](systemconfig-nic.md) definen los datos de evento para este evento.                                                       |
| **Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ DiscoFísico**(el valor de tipo de evento es 11)<br/> | Evento de configuración de disco físico. Las clases MOF de [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) definen los datos de evento para este evento.                                     |
| **Evento \_ de Configuración de tipo de seguimiento \_ \_ \_ PNP**(el valor de tipo de evento es 22)<br/>          | Evento plug and Play. La clase MOF de las clases MOF [**SystemConfig \_ PNP**](systemconfig-pnp.md) define los datos de evento para este evento.                                                 |
| **Evento \_ de TRACE \_ Type \_ config \_ Power**(el valor del tipo de evento es 16)<br/>        | Evento de configuración de energía. La clase [**SystemConfig \_ Power**](systemconfig-power.md) mof define los datos de evento para este evento.                                                   |
| **Evento \_ de Tipo de seguimiento de \_ \_ \_ servicios de configuración**(el valor de tipo de evento es 15)<br/>     | Evento de configuración de servicios. La clase MOF de [**SystemConfig \_ Services**](systemconfig-services.md) define los datos de evento para este evento.                                          |
| **Evento \_ de TRACE \_ Type \_ config \_ video**(valor de tipo de evento es 14)<br/>        | Evento de configuración del adaptador de gráficos. La clase MOF de [**\_ vídeo SystemConfig**](systemconfig-video.md) define los datos de evento para este evento.                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_CPU SystemConfig**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md)
</dt> <dt>

[**SystemConfig \_ IRQ**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md)
</dt> <dt>

[**\_Red SystemConfig**](systemconfig-network.md)
</dt> <dt>

[**NIC de SystemConfig \_**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md)
</dt> <dt>

[**SystemConfig \_ PNP**](systemconfig-pnp.md)
</dt> <dt>

[**Alimentación de SystemConfig \_**](systemconfig-power.md)
</dt> <dt>

[**Servicios de SystemConfig \_**](systemconfig-services.md)
</dt> <dt>

[**Vídeo de SystemConfig \_**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 
