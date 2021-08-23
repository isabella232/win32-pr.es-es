---
title: Implementación de CEcho DoProcessOutput
description: Implementación de CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Reproductor de Windows Media complementos,método DoProcessOutput de ejemplo echo
- plug-ins,Echo sample DoProcessOutput method
- complementos de procesamiento de señales digitales, método DoProcessOutput de ejemplo de eco
- Complementos DE DSP, método DoProcessOutput de ejemplo de Eco
- Ejemplo de complemento DSP de eco, método DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07054950cabadbc835c9904d48cdb4e6ddf5f05c0822c997558381958a9857d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135648"
---
# <a name="implementing-cechodoprocessoutput"></a>Implementación de CEcho::D oProcessOutput

El **método DoProcessOutput** realiza el procesamiento de señal digital. Este es el método que realiza los cambios en los datos proporcionados por Reproductor de Windows Media. Son los resultados de este método que se escucharán como un efecto de eco cuando se complete el complemento de ejemplo de eco.

En este ejemplo, el complemento solo procesará audio de 8 o 16 bits. Deberá realizar algunos cambios en el código de ejemplo del asistente para complementos para quitar las secciones que procesan audio de mayor profundidad de bits. Sin embargo, merece la pena estudiar estas secciones, ya que puede decidir agregar su propia implementación de eco para esos formatos.

En las secciones siguientes se detallan los cambios que debe realizar en el código:

-   [Quitar el código para procesar más de 16 bits](removing-the-code-to-process-greater-than-16-bits.md)
-   [Procesamiento de los datos de audio](processing-the-audio-data.md)
-   [Variables para realizar el procesamiento](variables-to-perform-processing.md)
-   [Creación del efecto de eco](creating-the-echo-effect.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




