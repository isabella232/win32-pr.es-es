---
title: Listas
description: Listas
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, listas
- mezcladores, controles
- mezcladores, listas
- controles de lista
- Estructura de MIXERCONTROLDETAILS_BOOLEAN
- Estructura de MIXERCONTROLDETAILS_LISTTEXT
- control de selección única
- control de selección múltiple
- control Mixer
- Multiplexor (MUX)
- MUX (multiplexor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358855"
---
# <a name="lists"></a>Listas

Los controles de lista proporcionan Estados de selección única o selección múltiple para las líneas de audio complejas. Estos controles usan la [**estructura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar y establecer las propiedades del control. La estructura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) también se usa para recuperar todas las descripciones de texto de un control de varios elementos. En la tabla siguiente se describen los tipos de controles de lista.



| Control           | Descripción                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selección única     | Restringe la selección del control a un elemento cada vez. A diferencia del control multiplexor, este control se puede usar para controlar más de líneas de origen de audio. Por ejemplo, podría utilizar este control para seleccionar un filtro de paso bajo de una lista de filtros admitidos por un dispositivo de mezclador. |
| Multiplexor (MUX) | Restringe la selección de línea a una línea de código fuente a la vez.                                                                                                                                                                                                                       |
| Selección múltiple   | Permite al usuario seleccionar varios elementos de una lista simultáneamente. A diferencia del control de mezclador, el control de selección múltiple se puede usar para controlar más de líneas de origen de audio.                                                                                                  |
| Mixer             | Permite al usuario seleccionar las líneas de origen de una lista simultáneamente.                                                                                                                                                                                                               |



 

 

 