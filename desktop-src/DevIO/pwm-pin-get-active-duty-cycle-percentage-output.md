---
description: Contiene el porcentaje del ciclo de servicio actual para un pin o canal en un controlador de pulse Width Width (PWM).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT estructura (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164322"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>ESTRUCTURA DE SALIDA DE \_ PORCENTAJE DE CICLO DE SERVICIO \_ \_ \_ \_ ACTIVO \_ \_ DE PIN DE PWM

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Contiene el porcentaje del ciclo de servicio actual para un pin o canal en un controlador de pulse Width Width (PWM).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Porcentaje**
</dt> <dd>

El ciclo de servicio de señal de PWM actual, como porcentaje de \_ PWM, que es un valor ULONGLONG.

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

[**PORCENTAJE DEL CICLO DE \_ SERVICIO ACTIVO DEL PIN DE PWM \_ \_ \_ \_ \_ DE \_ IOCTL**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




