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
- Control de panorámica QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e902e3ead0416cb4b2a7d56d289f91779563109cb9494784635affc75069dfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805355"
---
# <a name="sliders-windows-multimedia"></a>Controles deslizantes (Windows Multimedia)

Los controles deslizantes suelen ser controles horizontales que se pueden ajustar a la izquierda o derecha. Estos controles usan la [**estructura MIXERCONTROLDETAILS \_ SIGNED**](/previous-versions//dd757297(v=vs.85)) para recuperar y establecer propiedades de control. En la tabla siguiente se describen los tipos de controles deslizantes.



| Control    | Descripción                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Control deslizante     | Tiene un intervalo de –32 768 a 32 767. El controlador mezclador define los límites de este control.                               |
| Movimiento panorámico        | Tiene un intervalo de –32 768 a 32 767. El controlador mezclador define los límites de este control, con 0 como valor de rango medio. |
| QSound Pan | Proporciona un control de sonido expandido a través de QSound. Este control tiene un intervalo de –15 a 15.                               |



 

 

 
