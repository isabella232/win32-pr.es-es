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
ms.openlocfilehash: 7d4c3103663ceac65deff7744b0cf45a21a787959cc6e866bde5ac8673f7f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984435"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>ESTRUCTURA DE SALIDA \_ \_ GET \_ POLARITY DEL PIN \_ DE PWM

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Contiene un valor de polaridad que se devuelve.

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

Polaridad del pin o canal como un valor [**\_ POLARITY de PWM.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) La polaridad es alta activa o baja activa.

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

[**IOCTL \_ PWM \_ PIN \_ GET \_ POLARITY**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**POLARIDAD \_ DE PWM**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

