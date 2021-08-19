---
title: Listas
description: Listas
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- mezcladores de audio, controles
- mezcladores de audio, listas
- mezcladores, controles
- mixers,lists
- controles de lista
- MIXERCONTROLDETAILS_BOOLEAN estructura
- MIXERCONTROLDETAILS_LISTTEXT estructura
- control de selección única
- control de selección múltiple
- control mezclador
- multiplexor (MUX)
- MUX (multiplexor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f15e1c89e564ddd3b6c263b91242a3e4dc0382fd36f86554ec6bd0556191ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139400"
---
# <a name="lists"></a>Listas

Los controles de lista proporcionan estados de selección única o selección múltiple para líneas de audio complejas. Estos controles usan la [**estructura \_ BOOLEAN MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar y establecer propiedades de control. La [**estructura MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) también se usa para recuperar todas las descripciones de texto de un control de varios elementos. En la tabla siguiente se describen los tipos de controles de lista.



| Control           | Descripción                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selección única     | Restringe la selección del control a un elemento a la vez. A diferencia del control multiplexor, este control se puede usar para controlar más que las líneas de origen de audio. Por ejemplo, podría usar este control para seleccionar un filtro de paso bajo de una lista de filtros admitidos por un dispositivo mezclador. |
| Multiplexor (MUX) | Restringe la selección de línea a una línea de origen a la vez.                                                                                                                                                                                                                       |
| Selección múltiple   | Permite al usuario seleccionar varios elementos de una lista simultáneamente. A diferencia del control mezclador, el control de selección múltiple se puede usar para controlar más que las líneas de origen de audio.                                                                                                  |
| Mixer             | Permite al usuario seleccionar líneas de origen de una lista simultáneamente.                                                                                                                                                                                                               |



 

 

 