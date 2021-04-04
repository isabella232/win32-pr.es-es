---
description: Contiene un valor de polaridad que se va a devolver.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Estructura de PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998257"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>Estructura de salida de la \_ \_ \_ \_ estructura de los pines de PWM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Contiene un valor de polaridad que se va a devolver.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Polaridad**
</dt> <dd>

Polaridad del PIN o canal como valor de polaridad de [**PWM \_**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . La polaridad es alta o activa baja.

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

[**PIN de PWM de IOCTL \_ \_ \_ obtener \_ polarización**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**polaridad de PWM \_**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

