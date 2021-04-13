---
description: La modulación de ancho de pulsos (PWM) es la técnica de generación de una onda de impulso rectangular que tiene un ancho de pulsos que se modula para producir la variación del valor medio de la forma de onda.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: API DE PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538884"
---
# <a name="pwm-api"></a>API DE PWM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La modulación de ancho de pulsos (PWM) es la técnica de generación de una onda de impulso rectangular que tiene un ancho de pulsos que se modula para producir la variación del valor medio de la forma de onda. Entre los usos más comunes se incluyen motores cinemáticos de conducción, LED de atenuación u otras funciones relacionadas. PWM está pensado para usarse principalmente en escenarios de Internet de las cosas.

## <a name="about-pulse-width-modulation"></a>Acerca de la modulación del ancho del pulso

Una forma de onda de PWM se puede clasificar por dos parámetros:

-   Un período de onda (T)

-   El ciclo de servicio, donde la frecuencia de la forma de onda (f) es el recíproco del período f = 1/T

El ciclo de servicio describe la proporción de **en** el / tiempo **activo** con respecto al intervalo normal o al **período** de tiempo. Un ciclo de derechos reducidos corresponde a un promedio de energía de salida baja, ya que la energía está desactivada durante la mayor parte del tiempo. El ciclo de servicio se expresa como un porcentaje. Totalmente encendido es el 100%. Totalmente desactivado es 0%. La mitad **activa** es el 50%.

Los desarrolladores que deseen implementar PWM en sus aplicaciones de IoT deben investigar la documentación de los de [WinRT.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Tipos de modulación de ancho de pulsos

PWM usa [estos códigos de control de e/s](pwm-control-codes.md), [estructuras](pwm-structures.md)y [enumeraciones.](pwm-enumeration-types.md)

PWM también utiliza la función siguiente: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
