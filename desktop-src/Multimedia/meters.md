---
title: Metros
description: Metros
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, medidores
- mezcladores, controles
- mezcladores, medidores
- controles de medidor
- Estructura de MIXERCONTROLDETAILS_BOOLEAN
- Estructura de MIXERCONTROLDETAILS_SIGNED
- Estructura de MIXERCONTROLDETAILS_UNSIGNED
- Boolean (control)
- control de pico
- control firmado
- control sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487719"
---
# <a name="meters"></a>Metros

Los controles de medidor miden los datos que pasan a través de una línea de audio. Estos controles usan las estructuras [**MIXERCONTROLDETAILS \_ Boolean**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS \_ signed**](/previous-versions//dd757297(v=vs.85))y [**MIXERCONTROLDETAILS \_ sin firmar**](/previous-versions//dd757298(v=vs.85)) para recuperar y establecer las propiedades del control. En la tabla siguiente se describen los tipos de medidores.



| Control  | Descripción                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean  | Mide si un valor entero es FALSE/OFF (cero) o TRUE/ON (distinto de cero).                                                                            |
| Peak     | Mide la desviación de 0 en las direcciones positivas y negativas. El intervalo de valores enteros para el medidor de picos es de – 32.768 a 32.767. |
| Firmado   | Mide valores enteros en el intervalo de – 231 a (231 – 1). El controlador del mezclador define los límites de este medidor.                                     |
| Sin signo | Mide valores enteros en el intervalo de 0 a (232 – 1). El controlador del mezclador define los límites de este medidor.                                        |



 

 

 