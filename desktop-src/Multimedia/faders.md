---
title: Atenua
description: Atenua
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, faders
- mezcladores, controles
- mezcladores, faders
- atenua
- Estructura de MIXERCONTROLDETAILS_UNSIGNED
- control de atenuación de volumen
- control de atenuación del volumen de graves
- control de atenuación de volumen de agudos
- control de ecualizador gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995151"
---
# <a name="faders"></a>Atenua

Los controles atenuador suelen ser controles verticales que se pueden ajustar hacia arriba o hacia abajo. Estos controles tienen una escala lineal y usan la [**estructura \_ sin firmar MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) para recuperar y establecer los detalles del control. En la tabla siguiente se describen los tipos de faders.



| Control   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fader     | Control de atenuación general. El intervalo de valores aceptables es de 0 a 65.535.                                                                                                                                                                                                                                                                                                                                       |
| Volumen    | Control general de atenuación de volumen. El intervalo de valores aceptables es de 0 a 65.535. Para obtener información acerca de cómo cambiar este intervalo, consulte la documentación del dispositivo de mezclador.                                                                                                                                                                                                                                        |
| Improvisa      | Control de atenuación del volumen de graves. El intervalo de valores aceptables es de 0 a 65.535. Los límites de la banda de la frecuencia de graves son específicos del hardware. Para obtener información sobre los límites de banda, consulte la documentación del dispositivo de mezclador.                                                                                                                                                                                      |
| Agudos    | Control de atenuación del volumen de agudos. El intervalo de valores aceptables es de 0 a 65.535. Los límites de la banda de frecuencia de agudos son específicos del hardware. Para obtener información sobre los límites de banda, consulte la documentación del dispositivo de mezclador.                                                                                                                                                                              |
| Ecualizador | Control de ecualizador gráfico. El intervalo de valores aceptables para una banda del ecualizador es de 0 a 65.535. El número de bandas de ecualizador y sus límites es específico del hardware. Para obtener información sobre el ecualizador, consulte la documentación del dispositivo de mezclador. Puede usar la estructura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) para recuperar etiquetas de texto para el ecualizador. |



 

 

 