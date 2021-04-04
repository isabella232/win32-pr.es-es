---
description: En este tema se enumeran los ioctl para la modulación de ancho de impulso.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: Códigos de control PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7de81b26a1970bbecde76729be2f1c84e6c067
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998116"
---
# <a name="pwm-control-codes"></a>Códigos de control PWM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

En este tema se enumeran los ioctl para la modulación de ancho de impulso.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**el \_ controlador de PWM de ioctl \_ obtiene el \_ \_ \_ período real**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Recupera el período de la señal de salida efectiva del controlador de modulación de ancho de pulsos (PWM) tal y como se mediría en sus canales de salida.<br/>                                                                                                                                                                                  |
| [**\_ \_ \_ obtener información del controlador de PWM de ioctl \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Recupera información sobre un controlador de modulación de ancho de pulsos (PWM). Esta información no cambia después de inicializar el controlador. <br/>                                                                                                                                                                                |
| [**\_ \_ \_ tiempo deseado del conjunto de controladores \_ de \_ ioctl de ioctl**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Establece el período de la señal de salida de un controlador de modulación de ancho de pulso (PWM) en un valor sugerido. <br/>                                                                                                                                                                                                                            |
| [**\_porcentaje de \_ \_ ciclo de \_ \_ servicio activo \_ \_ de ioctl de ioctl**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Recupera el porcentaje actual del ciclo de servicio de un PIN o canal. El código de control devuelve el porcentaje como una estructura de [**\_ salida de \_ \_ \_ \_ \_ porcentaje del \_ ciclo de servicio activo**](pwm-pin-get-active-duty-cycle-percentage-output.md) de un PIN de PWM.<br/>                                                                                  |
| [**\_porcentaje de \_ \_ ciclo de \_ arancel activo del conjunto \_ de \_ pines \_ de ioctl**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Establezca un valor de porcentaje de ciclo de servicio deseado para el PIN o canal del controlador. El código de control especifica el porcentaje como una estructura de [**\_ entrada de \_ \_ \_ \_ \_ porcentaje \_ del ciclo de servicio activo del PIN de PWM**](pwm-pin-set-active-duty-cycle-percentage-input.md) . <br/>                                                                      |
| [**PIN de PWM de IOCTL \_ \_ \_ obtener \_ polarización**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Recupera la polaridad de señal actual del PIN o canal. El código de control obtiene la polaridad de la señal como una estructura de salida de la [**\_ \_ \_ polaridad \_ del PIN de PWM**](pwm-pin-get-polarity-output.md) . La polaridad de la señal es activo alto o activo bajo, tal como se define en la enumeración de [**\_ polaridad de PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . <br/> |
| [**\_polaridad de \_ conjunto de PIN de PWM de ioctl \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Establece la polaridad de la señal del PIN o canal. El código de control establece la polaridad de la señal basándose en una estructura de [**entrada de polaridad de conjunto de pines de PWM \_ \_ \_ \_**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) . La polaridad de la señal es activo alto o activo bajo, tal como se define en la enumeración de [**\_ polaridad de PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .<br/>           |
| [**\_Inicio del \_ PIN de PWM de ioctl \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Inicia la generación de la señal de modulación de ancho de pulsos (PWM) en un PIN o canal. Para comprobar si se ha iniciado un PIN, use el [**PIN de PWM de ioctl \_ \_ \_ \_ iniciado**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**\_detención del \_ PIN de PWM de ioctl \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Detiene la generación de la señal de modulación de ancho de pulsos (PWM) en un PIN o canal. Para comprobar si se ha iniciado un PIN, use el [**PIN de PWM de ioctl \_ \_ \_ \_ iniciado**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**\_ \_ \_ se inició el PIN de PWM de ioctl \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Recupera el estado de generación de la señal de un PIN o canal. Cada pin tiene un estado iniciado o detenido, ya que [**\_ se ha \_ \_ iniciado \_**](pwm-pin-is-started-output.md) la estructura de salida de un PIN de PWM.<br/>                                                                                                                                 |



 

 

 




