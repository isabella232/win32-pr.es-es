---
title: Conmutadores
description: Conmutadores
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, conmutadores
- mezcladores, controles
- mezcladores, conmutadores
- cambiar controles
- Estructura de MIXERCONTROLDETAILS_BOOLEAN
- Boolean (control)
- Button (control)
- control ON/OFF
- control mono
- control de sonoridad
- control mejorado de estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904543"
---
# <a name="switches"></a>Conmutadores

Los controles Switch son modificadores de dos Estados. Estos controles usan la [**estructura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar y establecer las propiedades del control. En la tabla siguiente se describen los tipos de modificadores.



| Control         | Descripción                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean         | El modificador genérico. Se puede establecer en **true** o en **false**.                                                                                                                                                                           |
| Botón          | Establézcalo en **true** para todos los botones que el controlador debe controlar como si hubieran sido presionados. Si el valor es **false**, no se realiza ninguna acción.                                                                                         |
| Activado/Desactivado          | Modificador alternativo que se representa mediante un gráfico distinto del que se usa para el modificador booleano. Se puede establecer en ON u OFF.                                                                                                    |
| Silencio            | Silencia una línea de audio (suprimiendo el flujo de datos de la línea) o permite reproducir los datos de audio. Este modificador se usa con frecuencia para ayudar a controlar las líneas que alimentan el mezclador.                                                        |
| Mono            | Cambia entre la salida mono y estéreo para una línea de audio estéreo. Establézcalo en OFF para reproducir los datos estéreo como canales independientes. Establezca en ON para combinar datos de ambos canales en una línea de audio mono.                                            |
| Sonoridad        | Aumenta el bajo volumen bajo de una línea de audio. Establezca en ON para aumentar el número de bajos de volumen bajo. Establezca esta opción en desactivado para establecer los niveles de volumen en normal. La cantidad de aumento es específica del hardware. Para obtener más información, consulte la documentación del dispositivo de mezclador. |
| Estéreo mejorado | Aumenta la separación estéreo. Establezca en ON para aumentar la separación estéreo. Se establece en OFF para no mejorar.                                                                                                                                  |



 

 

 