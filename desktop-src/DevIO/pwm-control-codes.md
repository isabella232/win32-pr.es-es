---
description: En este tema se enumeran las IOCTL para la amplitud de ancho de pulso.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: Códigos de control de PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7de81b26a1970bbecde76729be2f1c84e6c067
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164337"
---
# <a name="pwm-control-codes"></a>Códigos de control de PWM

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

En este tema se enumeran las IOCTL para la amplitud de ancho de pulso.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOCTL \_ PWM \_ CONTROLLER GET REAL \_ \_ \_ PERIOD**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Recupera el período de señal de salida efectivo del controlador Desasoción de ancho de pulso (PWM) tal como se mediría en sus canales de salida.<br/>                                                                                                                                                                                  |
| [**IOCTL \_ PWM \_ CONTROLLER \_ GET \_ INFO**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Recupera información acerca de un controlador de pulsación de ancho de pulso (PWM). Esta información no cambia después de inicializar el controlador. <br/>                                                                                                                                                                                |
| [**IOCTL \_ PWM \_ CONTROLLER \_ SET \_ DESIRED \_ PERIOD**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Establece el período de señal de salida de un controlador pwm de ancho de pulso (PWM) en un valor sugerido. <br/>                                                                                                                                                                                                                            |
| [**PORCENTAJE DE CICLO DE \_ SERVICIO ACTIVO DEL PIN DE PWM \_ \_ \_ DE \_ \_ \_ IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Recupera el porcentaje actual del ciclo de servicio para un pin o canal. El código de control devuelve el porcentaje como una estructura [**GET ACTIVE DUTY CYCLE PERCENTAGE OUTPUT \_ \_ \_ \_ \_ \_ \_ del PIN de PWM.**](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/>                                                                                  |
| [**PORCENTAJE DE CICLO ACTIVO DEL CONJUNTO DE \_ PIN DE PWM \_ \_ \_ \_ \_ DE \_ IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Establezca un valor de porcentaje de ciclo de servicio deseado para el pin o canal del controlador. El código de control especifica el porcentaje como una estructura [**SET ACTIVE DUTY CYCLE PERCENTAGE INPUT \_ \_ \_ \_ \_ \_ \_ del PIN de PWM.**](pwm-pin-set-active-duty-cycle-percentage-input.md) <br/>                                                                      |
| [**IOCTL \_ PWM \_ PIN \_ GET \_ POLARITY**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Recupera la polaridad de señal actual del pin o canal. El código de control obtiene la polaridad de señal como una estructura [**\_ GET \_ \_ POLARITY OUTPUT \_ del PIN de PWM.**](pwm-pin-get-polarity-output.md) La polaridad de señal es Alta activa o Baja activa, tal como se define en la [**enumeración \_ POLARITY de PWM.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) <br/> |
| [**POLARIDAD DEL \_ CONJUNTO DE PIN DE PWM \_ \_ \_ DE IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Establece la polaridad de señal del pin o canal. El código de control establece la polaridad de señal en función de una estructura [**\_ PWM PIN \_ SET \_ POLARITY \_ INPUT.**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) La polaridad de señal es Alta activa o Baja activa, tal como se define en la [**enumeración \_ POLARITY de PWM.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity)<br/>           |
| [**INICIO DEL \_ PIN DE PWM \_ DE IOCTL \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Inicia la generación de la señal pulse Width Width (PWM) en un pin o canal. Para comprobar si se ha iniciado un pin, use [**EL PIN DE PWM DE IOCTL \_ \_ IS \_ \_ STARTED**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**IOCTL \_ PWM \_ PIN \_ STOP**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Detiene la generación de la señal pulse Width Width Desaconsoce (PWM) en un pin o canal. Para comprobar si se ha iniciado un pin, use [**EL PIN DE PWM DE IOCTL \_ \_ IS \_ \_ STARTED**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**SE HA INICIADO \_ EL PIN DE PWM \_ \_ DE \_ IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Recupera el estado de generación de señal para un pin o canal. Cada pin tiene un estado iniciado o detenido como una estructura [**DE SALIDA IS STARTED del PIN \_ \_ \_ \_ de PWM.**](pwm-pin-is-started-output.md)<br/>                                                                                                                                 |



 

 

 




