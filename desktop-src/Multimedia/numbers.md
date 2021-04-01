---
title: Números (Windows multimedia)
description: Números
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, números
- mezcladores, controles
- mezcladores, números
- controles numéricos
- Estructura de MIXERCONTROLDETAILS_SIGNED
- Estructura de MIXERCONTROLDETAILS_UNSIGNED
- control de decibelios
- control de porcentaje
- control firmado
- control sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149789"
---
# <a name="numbers-windows-multimedia"></a>Números (Windows multimedia)

Los controles de número permiten al usuario escribir datos numéricos asociados a una línea. Los datos numéricos se expresan como enteros con signo, enteros sin signo o valores de decibelios enteros. Estos controles usan las estructuras [**\_ sin firmar**](/previous-versions//dd757298(v=vs.85)) [**MIXERCONTROLDETAILS \_ con signo**](/previous-versions//dd757297(v=vs.85)) y MIXERCONTROLDETAILS para recuperar y establecer las propiedades del control. En la tabla siguiente se describen los tipos de controles numéricos.



| Control  | Descripción                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Firmado   | Permite valores enteros escritos en el intervalo de – 231 a (231 – 1).                                                               |
| Sin signo | Permite valores enteros escritos en el intervalo de 0 a (232 – 1).                                                                   |
| Decibelio  | Permite escribir valores enteros de decibelios, en décimas de decibelios. El intervalo de valores para este control es de – 32.768 a 32.767. |
| Percent  | Permite especificar valores como porcentajes.                                                                                         |



 

 

 
