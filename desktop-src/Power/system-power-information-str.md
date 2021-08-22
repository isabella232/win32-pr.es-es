---
description: Contiene información sobre la inactividad del sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: SYSTEM_POWER_INFORMATION estructura
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
ms.openlocfilehash: 665c19a99bffae46cf20af8c5c634e2e9594ecd07d02f003f56d42277ce9a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143308"
---
# <a name="system_power_information-structure"></a>Estructura \_ SYSTEM POWER \_ INFORMATION

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

La inactividad en la que el sistema se considera inactivo y el tiempo de espera de inactividad comienza a contarse, expresado como un porcentaje. Si se coloca por debajo de este número, se cancela el temporizador.

</dd> <dt>

**Inactividad**
</dt> <dd>

Nivel de inactividad actual, expresado como porcentaje.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

Tiempo restante en el temporizador inactivo, en segundos.

</dd> <dt>

**CoolingMode**
</dt> <dd>

Modo de refrigeración del sistema actual. Este miembro debe tener uno de los valores siguientes.



| Value                                                                                                                                                                                                                                 | Significado                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**Pedido de compra \_ TZ \_ ACTIVE**</dt> <dt>0</dt> </dl>                    | El sistema está actualmente en modo de refrigeración activa.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**Pedido de compra \_ MODO TZ \_ NO \_ VÁLIDO**</dt> <dt>2</dt> </dl> | El sistema no admite la limitación de CPU o no hay ninguna zona térmico definida en el sistema.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**Pedido de compra \_ TZ \_ PASSIVE**</dt> <dt>1</dt> </dl>                 | El sistema está actualmente en modo de refrigeración pasiva.<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que esta definición de estructura se omitió accidentalmente de WinNT.h. Este error se corregirá en el futuro. Mientras tanto, para compilar la aplicación, incluya la definición de estructura contenida en este tema en el código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




