---
title: Números (Windows Multimedia)
description: Números
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mezcladores de audio, controles
- mezcladores de audio, números
- mezcladores, controles
- mezcladores, números
- controles de número
- MIXERCONTROLDETAILS_SIGNED estructura
- MIXERCONTROLDETAILS_UNSIGNED estructura
- control decibel
- control de porcentaje
- control firmado
- control sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169650"
---
# <a name="numbers-windows-multimedia"></a>Números (Windows Multimedia)

Los controles de número permiten al usuario escribir datos numéricos asociados a una línea. Los datos numéricos se expresan como enteros con signo, enteros sin signo o valores de decibelios enteros. Estos controles usan las estructuras [**MIXERCONTROLDETAILS \_ SIGNED**](/previous-versions//dd757297(v=vs.85)) y [**MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85)) para recuperar y establecer propiedades de control. En la tabla siguiente se describen los tipos de controles number.



| Control  | Descripción                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Firmado   | Permite valores enteros especificados en el intervalo de – 231 a (231 –1).                                                               |
| Sin signo | Permite valores enteros especificados en el intervalo de 0 a (232 –1).                                                                   |
| Decibelio  | Permite especificar valores de decibelios enteros, en décimas de decibelios. El intervalo de valores de este control es de -32.768 a 32.767. |
| Percent  | Permite especificar valores como porcentajes.                                                                                         |



 

 

 
