---
title: Controles deslizantes (Windows multimedia)
description: Controles deslizantes
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, controles deslizantes
- mezcladores, controles
- mezcladores, controles deslizantes
- controles deslizantes
- Estructura de MIXERCONTROLDETAILS_SIGNED
- control de panorámica
- Control pan de QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421799"
---
# <a name="sliders-windows-multimedia"></a>Controles deslizantes (Windows multimedia)

Los controles deslizantes suelen ser controles horizontales que se pueden ajustar a la izquierda o a la derecha. Estos controles usan la [**estructura \_ firmada MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) para recuperar y establecer las propiedades del control. En la tabla siguiente se describen los tipos de controles deslizantes.



| Control    | Descripción                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Control deslizante     | Tiene un intervalo de – 32.768 a 32.767. El controlador del mezclador define los límites de este control.                               |
| Movimiento panorámico        | Tiene un intervalo de – 32.768 a 32.767. El controlador de mezclador define los límites de este control, con 0 como valor de intervalo intermedio. |
| QSound pan | Proporciona un control de sonido expandido a través de QSound. Este control tiene un intervalo de – 15 a 15.                               |



 

 

 
