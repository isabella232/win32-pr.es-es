---
title: Remuestreo de audio
description: Remuestreo de audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- SDK de Windows Media Format, remuestreo de audio
- SDK de Windows Media Format, volver a muestrear audio
- Advanced Systems Format (ASF), remuestreo de audio
- ASF (formato de sistemas avanzados), remuestreo de audio
- Advanced Systems Format (ASF), volver a muestrear audio
- ASF (formato de sistemas avanzados), volver a muestrear audio
- remuestreo de audio
- volver a muestrear audio, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357076"
---
# <a name="audio-resampling"></a>Remuestreo de audio

Cada formato comprimido de un códec de audio tiene una frecuencia de muestreo y un tamaño de muestra concretos. No es necesario que coincidan con la configuración del formato de entrada o de salida. Si un formato de entrada tiene una configuración diferente a la del formato comprimido descrito en el perfil, el escritor volverá a muestrear el audio, durante el proceso de codificación, para que coincida con el formato comprimido. El escritor solo acepta determinados formatos como entrada. Al enumerar los formatos de entrada de una secuencia de audio comprimida, se pueden volver a muestrear todos los formatos recuperados para que coincidan con el formato del perfil.

Al leer audio comprimido, el lector volverá a muestrear el contenido para que coincida con el formato de salida. Debe usar uno de los formatos de salida enumerados por el lector, por lo que se garantiza que el audio se puede volver a muestrear en la configuración del formato de salida.

Cada remuestreo puede afectar a la calidad del audio. Cuando sea posible, debe usar los formatos de entrada y salida con valores que coincidan con el formato comprimido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




