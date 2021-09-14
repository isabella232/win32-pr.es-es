---
description: Contiene el estado actual de generación de señales de un pin.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: PWM_PIN_IS_STARTED_OUTPUT estructura (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164314"
---
# <a name="pwm_pin_is_started_output-structure"></a>Estructura DE SALIDA DE PIN DE PWM \_ \_ \_ \_ INICIADA

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Contiene el estado actual de generación de señales de un pin.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**IsStarted**
</dt> <dd>

Estado actual de generación de señal de pin. Un valor true significa que se inicia el pin. Un valor false significa que el pin está detenido.

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

[**SE HA INICIADO \_ EL PIN DE PWM \_ \_ DE \_ IOCTL**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




