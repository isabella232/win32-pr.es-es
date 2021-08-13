---
description: La diferenciación de ancho de pulso (PWM) es la técnica para generar una onda de pulso rectangular que tiene un ancho de pulso que se modulará para dar lugar a la variación del valor medio de la onda.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff257007180cf3da2b78c14415c8fa350b4bb395e0202f49d2d7ae056f025bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405199"
---
# <a name="pwm-api"></a>PWM API

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La diferenciación de ancho de pulso (PWM) es la técnica para generar una onda de pulso rectangular que tiene un ancho de pulso que se modulará para dar lugar a la variación del valor medio de la onda. Entre los usos más comunes se incluyen la conducción de motores de carreras, la atenuación de LED u otras funciones relacionadas. PWM está pensado para usarse principalmente para Internet de las cosas escenarios.

## <a name="about-pulse-width-modulation"></a>Acerca de la frecuencia de ancho de pulso

Una forma de onda de PWM se puede clasificar por dos parámetros:

-   Un período de forma de onda (T)

-   El ciclo de servicio, donde la frecuencia de forma de onda (f) es el recíproco del período f=1/T

El ciclo de servicio describe la proporción de en tiempo activo con respecto al /  intervalo normal o **período** de tiempo. Un ciclo de servicio bajo corresponde a un promedio de potencia de salida baja, porque la energía está apagada durante la mayor parte del tiempo. El ciclo de servicio se expresa como un porcentaje. Totalmente on es 100 %. Totalmente desactivado es 0 %. **La** mitad del tiempo activo es del 50 %.

Los desarrolladores que buscan implementar PWM en sus aplicaciones de IoT deben investigar la [documentación de PwM de WinRT.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Tipos de amplitud de ancho de pulso

PWM usa [estos códigos de control de E/S,](pwm-control-codes.md) [estructuras](pwm-structures.md)y [enumeraciones.](pwm-enumeration-types.md)

PWM también usa la siguiente función: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
