---
description: Pulse Width Width Variation (PWM) es la técnica de generación de una onda de pulso rectangular que tiene un ancho de pulso que se modular para dar lugar a la variación del valor medio de la onda.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164334"
---
# <a name="pwm-api"></a>PWM API

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Pulse Width Width Variation (PWM) es la técnica de generación de una onda de pulso rectangular que tiene un ancho de pulso que se modular para dar lugar a la variación del valor medio de la onda. Entre los usos más comunes se incluyen la conducción de motores de carreras, LED atenuados u otras funciones relacionadas. PWM está pensado para usarse principalmente para Internet de las cosas escenarios.

## <a name="about-pulse-width-modulation"></a>Acerca de pulse width width width (Acerca del ancho de pulso)

Una forma de onda de PWM se puede clasificar por dos parámetros:

-   Un período de forma de onda (T)

-   El ciclo de servicio, donde la frecuencia de forma de onda (f) es el recíproco del período f=1/T

El ciclo de servicio describe la proporción de **en tiempo** activo con respecto al intervalo normal o /  **período** de tiempo. Un ciclo de servicio bajo corresponde a un promedio de potencia de salida baja, porque la energía está apagada la mayor parte del tiempo. El ciclo de servicio se expresa como un porcentaje. Totalmente en es 100 %. Totalmente desactivado es 0 %. **La** mitad del tiempo activa es del 50 %.

Los desarrolladores que buscan implementar PWM en sus aplicaciones de IoT deben investigar la [documentación de PwM de WinRT.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Tipos de pulse Width Width Width

PWM usa [estos códigos de control de E/S,](pwm-control-codes.md) [estructuras](pwm-structures.md)y [enumeraciones.](pwm-enumeration-types.md)

PWM también usa la siguiente función: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
