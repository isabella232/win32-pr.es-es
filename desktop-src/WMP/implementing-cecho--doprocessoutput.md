---
title: Implementación de CEcho DoProcessOutput
description: Implementación de CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076356"
---
# <a name="implementing-cechodoprocessoutput"></a>Implementación de CEcho::D oProcessOutput

El método **DoProcessOutput** realiza el procesamiento de la señal digital. Este es el método que realiza los cambios en los datos proporcionados por Media Player de Windows. Los resultados de este método se escuchan como un efecto de eco cuando se completa el complemento de ejemplo echo.

En este ejemplo, el complemento solo procesará audio de 8 o 16 bits. Tendrá que realizar algunos cambios en el código de ejemplo del Asistente para complementos para quitar las secciones que procesan audio de mayor profundidad de bits. Sin embargo, merece la pena estudiar estas secciones, ya que puede decidir agregar su propia implementación de Eco para esos formatos.

En las secciones siguientes se detallan los cambios que debe realizar en el código:

-   [Quitar el código para procesar más de 16 bits](removing-the-code-to-process-greater-than-16-bits.md)
-   [Procesamiento de los datos de audio](processing-the-audio-data.md)
-   [Variables para realizar el procesamiento](variables-to-perform-processing.md)
-   [Crear el efecto de eco](creating-the-echo-effect.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo echo**](the-echo-sample.md)
</dt> </dl>

 

 




