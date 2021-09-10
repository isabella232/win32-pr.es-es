---
title: Controles deslizantes (Windows Multimedia)
description: Controles deslizantes
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mezcladores de audio, controles
- mezcladores de audio, controles deslizantes
- mezcladores, controles
- mezcladores, controles deslizantes
- controles deslizantes
- MIXERCONTROLDETAILS_SIGNED estructura
- control de panorámica
- Control de panorámica Q Sound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372134"
---
# <a name="sliders-windows-multimedia"></a>Controles deslizantes (Windows Multimedia)

Los controles deslizantes suelen ser controles horizontales que se pueden ajustar a la izquierda o derecha. Estos controles usan la [**estructura MIXERCONTROLDETAILS \_ SIGNED**](/previous-versions//dd757297(v=vs.85)) para recuperar y establecer propiedades de control. En la tabla siguiente se describen los tipos de controles deslizantes.



| Control    | Descripción                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Control deslizante     | Tiene un intervalo de -32 768 a 32 767. El controlador mezclador define los límites de este control.                               |
| Movimiento panorámico        | Tiene un intervalo de -32 768 a 32 767. El controlador mezclador define los límites de este control, con 0 como valor de rango medio. |
| Q Sound Pan | Proporciona un control de sonido expandido a través de Q Sound. Este control tiene un intervalo de –15 a 15.                               |



 

 

 
