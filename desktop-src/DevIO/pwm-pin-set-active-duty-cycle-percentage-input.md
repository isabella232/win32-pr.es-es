---
description: Contiene un porcentaje de ciclo de servicio deseado para un pin o canal en un controlador de ancho de pulso (PWM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT estructura (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: ca6b2ee6aa4d4d2da3f94aa7cc471de12c1f8040b597edf568bf061c8e392aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758855"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>ESTRUCTURA DE ENTRADA DE PORCENTAJE DE CICLO DE SERVICIO ACTIVO DE CONJUNTO DE PIN \_ \_ \_ \_ \_ \_ \_ DE PWM

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Contiene un porcentaje de ciclo de servicio deseado para un pin o canal en un controlador de ancho de pulso (PWM).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Porcentaje**
</dt> <dd>

El ciclo de servicio de señal de PWM deseado, como PWM \_ PERCENTAGE, que es un valor ULONGLONG.

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

[**PORCENTAJE DE CICLO ACTIVO DEL CONJUNTO DE \_ PIN DE PWM \_ \_ \_ \_ \_ DE \_ IOCTL**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




