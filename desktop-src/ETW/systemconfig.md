---
description: 'Clase SystemConfig: esta clase es la clase primaria para los eventos de configuración de hardware. La sintaxis siguiente se simplifica a partir del código MOF.'
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
ms.openlocfilehash: 4f409887f70989c65475c8b854b4b610c9ffa6c122edc25e87b5ebdc8dbc9180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069645"
---
# <a name="systemconfig-class"></a>Clase SystemConfig

Esta clase es la clase primaria para los eventos de configuración de hardware.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase SystemConfig** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Estos eventos proporcionan la configuración de hardware del equipo. A diferencia de otros eventos del registrador de kernel de NT, la sesión del kernel genera automáticamente eventos de configuración de hardware; estos eventos no se habilitan al iniciar la sesión del registrador de kernel de NT.

Para los eventos de configuración de hardware Windows XP, consulte la [clase HWConfig.](hwconfig.md)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de configuración de hardware llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como el *parámetro pGuid.* Use los siguientes tipos de eventos para identificar el evento de configuración de hardware real al consumir eventos.



| Tipo de evento                                                                      | Descripción                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(el valor del tipo de evento es 10)<br/>          | Evento de configuración de CPU. Las [**clases SystemConfig \_ CPU**](systemconfig-cpu.md) MOF definen los datos de evento para este evento.                                                       |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ IDECHANNEL**(el valor del tipo de evento es 23)<br/>   | Evento de configuración del canal IDE principal y secundario. La clase MOF de las clases MOF de [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) define los datos de evento para este evento. |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ IRQ**(el valor del tipo de evento es 21)<br/>          | Evento de solicitud de interrupción (IRQ). La clase MOF de las clases MOF de [**SystemConfig \_ IRQ**](systemconfig-irq.md) define los datos de evento para este evento.                                       |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(el valor del tipo de evento es 12)<br/>  | Evento de configuración de disco lógico. La clase MOF de las clases MOF [**de SystemConfig \_ LogDisk**](systemconfig-logdisk.md) define los datos de evento para este evento.                            |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NETINFO**(el valor del tipo de evento es 17)<br/>      | Evento de iformación de red. La [**clase MOF SystemConfig \_ Network**](systemconfig-network.md) define los datos de evento para este evento.                                                |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NIC**(el valor del tipo de evento es 13)<br/>          | Evento de configuración de NIC. Las [**clases MOF \_ de la NIC SystemConfig**](systemconfig-nic.md) definen los datos de evento para este evento.                                                       |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(el valor del tipo de evento es 11)<br/> | Evento de configuración de disco físico. Las [**clases MOF \_ de SystemConfig PhyDisk**](systemconfig-phydisk.md) definen los datos de evento para este evento.                                     |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PNP**(el valor del tipo de evento es 22)<br/>          | Evento Plug and Play. La clase MOF de las clases MOF [**\_ de SystemConfig PNP**](systemconfig-pnp.md) define los datos de evento para este evento.                                                 |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ POWER**(el valor del tipo de evento es 16)<br/>        | Evento de configuración de energía. La [**clase SystemConfig \_ Power**](systemconfig-power.md) MOF define los datos de evento para este evento.                                                   |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ SERVICES**(el valor del tipo de evento es 15)<br/>     | Evento de configuración de servicios. La [**clase MOF de SystemConfig \_ Services**](systemconfig-services.md) define los datos de evento para este evento.                                          |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ VIDEO**(el valor del tipo de evento es 14)<br/>        | Evento de configuración del adaptador de gráficos. La [**clase MOF SystemConfig \_ Video**](systemconfig-video.md) define los datos de evento para este evento.                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig \_ CPU**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md)
</dt> <dt>

[**SystemConfig \_ IRQ**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md)
</dt> <dt>

[**SystemConfig \_ Network**](systemconfig-network.md)
</dt> <dt>

[**SystemConfig \_ NIC**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md)
</dt> <dt>

[**SystemConfig \_ PNP**](systemconfig-pnp.md)
</dt> <dt>

[**SystemConfig \_ Power**](systemconfig-power.md)
</dt> <dt>

[**SystemConfig \_ Services**](systemconfig-services.md)
</dt> <dt>

[**Vídeo \_ de SystemConfig**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 
