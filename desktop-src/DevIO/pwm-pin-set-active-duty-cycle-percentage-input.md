---
description: Contiene un porcentaje de ciclo de servicio deseado para un pin o canal en un controlador de pulse Width Width (PWM).
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
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164310"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>ESTRUCTURA DE ENTRADA DE \_ PORCENTAJE DE CICLO DE SERVICIO \_ \_ \_ \_ ACTIVO \_ DE \_ PIN DE PWM

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Contiene un porcentaje de ciclo de servicio deseado para un pin o canal en un controlador de pulse Width Width (PWM).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Porcentaje**
</dt> <dd>

Ciclo de servicio de señal de PWM deseado, como porcentaje de \_ PWM, que es un valor ULONGLONG.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                      |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                             |
| Versión mínima de KMDF<br/>     | 1.19<br/>                                                                                  |
| Versión mínima de UMDF<br/>     | 2.19<br/>                                                                                  |
| Encabezado<br/>                   | <dl> <dt>Pwm.h (incluir Pwm.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PORCENTAJE DE CICLO DE \_ SERVICIO ACTIVO DEL CONJUNTO DE PIN DE PWM \_ \_ \_ \_ \_ DE \_ IOCTL**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




