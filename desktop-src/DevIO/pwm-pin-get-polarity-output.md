---
description: Contiene un valor de polaridad que se devuelve.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: PWM_PIN_GET_POLARITY_OUTPUT estructura (Pwm.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164321"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>Pin de PWM \_ \_ GET POLARITY OUTPUT (Estructura de salida de \_ \_ POLARIDAD)

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Contiene un valor de polaridad que se devuelve.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Polaridad**
</dt> <dd>

Polaridad del pin o canal como un valor [**\_ POLARITY de PWM.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) La polaridad es Alta activa o Baja activa.

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

[**IOCTL \_ PWM \_ PIN \_ GET \_ POLARITY**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**POLARIDAD DE PWM \_**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

