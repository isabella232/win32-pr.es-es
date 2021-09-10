---
title: Faders
description: Faders
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mezcladores de audio, controles
- mezcladores de audio, faders
- mezcladores, controles
- mezcladores, faders
- Faders
- MIXERCONTROLDETAILS_UNSIGNED estructura
- control de atenuación de volumen
- control de atenuación de volumen de volumen de volumen
- Control de atenuación de volumen treble
- control de igualador gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372127"
---
# <a name="faders"></a>Faders

Los controles de atenuación suelen ser controles verticales que se pueden ajustar hacia arriba o hacia abajo. Estos controles tienen una escala lineal y usan la estructura [**MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85)) para recuperar y establecer los detalles del control. En la tabla siguiente se describen los tipos de atenuadores.



| Control   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fader     | Control de atenuación general. El intervalo de valores aceptables es de 0 a 65 535.                                                                                                                                                                                                                                                                                                                                       |
| Volumen    | Control de atenuación de volumen general. El intervalo de valores aceptables es de 0 a 65 535. Para obtener información sobre cómo cambiar este intervalo, consulte la documentación del dispositivo mezclador.                                                                                                                                                                                                                                        |
| Bajo      | Control de atenuación de volumen de sonido. El intervalo de valores aceptables es de 0 a 65 535. Los límites de la banda de frecuencia de frecuencia de frecuencia de frecuencia son específicos del hardware. Para obtener información sobre los límites de banda, consulte la documentación del dispositivo mezclador.                                                                                                                                                                                      |
| Agudos    | Control de atenuación de volumen triple. El intervalo de valores aceptables es de 0 a 65 535. Los límites de la banda de frecuencia triple son específicos del hardware. Para obtener información sobre los límites de banda, consulte la documentación del dispositivo mezclador.                                                                                                                                                                              |
| Ecualizador | Control de igualador gráfico. El intervalo de valores aceptables para una banda del igualador es de 0 a 65 535. El número de bandas de igualador y sus límites son específicos del hardware. Para obtener información sobre el igualador, consulte la documentación del dispositivo mezclador. Puede usar la estructura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) para recuperar etiquetas de texto para el igualador. |



 

 

 