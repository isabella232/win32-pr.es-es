---
description: Contiene el período de señal de salida efectivo para un controlador de ancho de pulso (PWM).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT estructura (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 3f51f360e7b6ff3966ed58d8ec3a171d8bbbfb54672c50c31852e71ab6750f95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088145"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a>Estructura GET REAL PERIOD OUTPUT del CONTROLADOR \_ \_ \_ \_ \_ DE PWM

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Contiene el período de señal de salida efectivo para un controlador de ancho de pulso (PWM).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ActualPeriod**
</dt> <dd>

El período de señal de salida efectivo tal como se mediría en los canales de salida del controlador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                      |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                             |
| Versión mínima de KMDF<br/>     | 1.19<br/>                                                                                  |
| Versión mínima de UMDF<br/>     | 2.19<br/>                                                                                  |
| Header<br/>                   | <dl> <dt>Pwm.h (incluir Pwm.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOCTL \_ PWM \_ CONTROLLER GET REAL \_ \_ \_ PERIOD**](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




