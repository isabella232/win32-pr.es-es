---
description: Contiene un porcentaje de ciclo de servicio deseado para un PIN o canal en un controlador de modulación de ancho de pulso (PWM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Estructura de PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423203"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>\_Estructura de \_ \_ \_ \_ \_ entrada porcentual del porcentaje de ciclo de servicio activo \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Contiene un porcentaje de ciclo de servicio deseado para un PIN o canal en un controlador de modulación de ancho de pulso (PWM).

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

El ciclo de servicio de la señal de PWM deseado, como un porcentaje de PWM \_ , que es un valor de ULONGLONG.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                             |
| Versión mínima de KMDF<br/>     | 1.19<br/>                                                                                  |
| Versión mínima de UMDF<br/>     | 2.19<br/>                                                                                  |
| Encabezado<br/>                   | <dl> <dt>PWM. h (incluir PWM. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_porcentaje de \_ \_ ciclo de \_ arancel activo del conjunto \_ de \_ pines \_ de ioctl**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




