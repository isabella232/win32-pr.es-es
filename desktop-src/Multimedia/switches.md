---
title: Modificadores
description: Modificadores
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mezcladores de audio, controles
- mezcladores de audio, conmutadores
- mezcladores, controles
- mezcladores, conmutadores
- controles switch
- MIXERCONTROLDETAILS_BOOLEAN estructura
- Control booleano
- control de botón
- control on/off
- control mono
- control de sonoridad
- control mejorado estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d2e23c5e6438fbc19208e3366283147462c2451a12e3ccdcae6c13fcd93d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805085"
---
# <a name="switches"></a>Modificadores

Los controles switch son modificadores de dos estados. Estos controles usan la [**estructura \_ BOOLEAN MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar y establecer propiedades de control. En la tabla siguiente se describen los tipos de modificadores.



| Control         | Descripción                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean         | Modificador genérico. Se puede establecer en **TRUE** o **FALSE.**                                                                                                                                                                           |
| Botón          | Establezca en **TRUE para** todos los botones que el controlador debe controlar como si se hubieran presionado. Si el valor es **FALSE,** no se hace ninguna acción.                                                                                         |
| Activado/Desactivado          | Un conmutador alternativo representado por un gráfico distinto del utilizado para el modificador booleano. Se puede establecer en ON u OFF.                                                                                                    |
| Silencio            | Silencia una línea de audio (suprime el flujo de datos de la línea) o permite reproducir los datos de audio. Este conmutador se usa con frecuencia para ayudar a controlar las líneas que se alimentan en el mezclador.                                                        |
| Mono            | Cambia entre la salida mono y estéreo para una línea de audio estéreo. Establezca esta configuración en OFF para reproducir datos estéreo como canales independientes. Establezca en ON para combinar datos de ambos canales en una línea de audio mono.                                            |
| Sonoridad        | Aumenta los bajos volúmenes para una línea de audio. Establezca en ON para aumentar el bajo volumen. Establezca en OFF para establecer los niveles de volumen en normal. La cantidad de aumento es específica del hardware. Para más información, consulte la documentación del dispositivo mezclador. |
| Estéreo mejorado | Aumenta la separación estéreo. Establezca en ON para aumentar la separación estéreo. Establezca en OFF para que no se mejore.                                                                                                                                  |



 

 

 