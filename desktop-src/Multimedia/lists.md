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
- control multiple-select
- control mezclador
- multiplexor (MUX)
- MUX (multiplexor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473893"
---
# <a name="lists"></a>Listas

Los controles de lista proporcionan estados de selección única o selección múltiple para líneas de audio complejas. Estos controles usan la [**estructura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar y establecer propiedades de control. La [**estructura MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) también se usa para recuperar todas las descripciones de texto de un control de varios elementos. En la tabla siguiente se describen los tipos de controles de lista.



| Control           | Descripción                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selección única     | Restringe la selección del control a un elemento a la vez. A diferencia del control multiplexor, este control se puede usar para controlar más que las líneas de origen de audio. Por ejemplo, podría usar este control para seleccionar un filtro de paso bajo de una lista de filtros compatibles con un dispositivo mezclador. |
| Multiplexador (MUX) | Restringe la selección de línea a una línea de origen a la vez.                                                                                                                                                                                                                       |
| Selección múltiple   | Permite al usuario seleccionar varios elementos de una lista simultáneamente. A diferencia del control mezclador, el control de selección múltiple se puede usar para controlar más que las líneas de origen de audio.                                                                                                  |
| Mixer             | Permite al usuario seleccionar líneas de origen de una lista simultáneamente.                                                                                                                                                                                                               |



 

 

 