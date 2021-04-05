---
description: Contiene información sobre la inactividad del sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Estructura de SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001948"
---
# <a name="system_power_information-structure"></a>Estructura de información de \_ energía del sistema \_

Contiene información sobre la inactividad del sistema.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**MaxIdlenessAllowed**
</dt> <dd>

La inactividad en la que se considera que el sistema está inactivo y el tiempo de espera de inactividad comienza el recuento, expresado en forma de porcentaje. Si se coloca debajo de este número, se cancela el temporizador.

</dd> <dt>

**Inactividad**
</dt> <dd>

Nivel de inactividad actual, expresado como un porcentaje.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

Tiempo restante en el temporizador de inactividad, en segundos.

</dd> <dt>

**CoolingMode**
</dt> <dd>

El modo de refrigeración del sistema actual. Este miembro debe tener uno de los valores siguientes.



| Value                                                                                                                                                                                                                                 | Significado                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**Pedido de compra \_ TZ \_ activo**</dt> <dt>0</dt> </dl>                    | El sistema está actualmente en modo de enfriamiento activo.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**Pedido de compra \_ \_ \_ Modo no válido de TZ**</dt> <dt>2</dt> </dl> | El sistema no admite la limitación de la CPU o no hay ninguna zona térmica definida en el sistema.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**Pedido de compra \_ TZ \_ pasivo**</dt> <dt>1</dt> </dl>                 | El sistema está actualmente en modo de enfriamiento pasivo.<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que esta definición de estructura se omitió accidentalmente en Winnt. h. Este error se corregirá en el futuro. Mientras tanto, para compilar la aplicación, incluya la definición de la estructura contenida en este tema en el código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




