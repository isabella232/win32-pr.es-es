---
title: Remuestreo de audio
description: Remuestreo de audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows SDK de formato multimedia, remuestreo de audio
- Windows SDK de formato multimedia, audio de remuestreo
- Formato de sistemas avanzados (ASF), remuestreo de audio
- ASF (formato de sistemas avanzados), remuestreo de audio
- Formato de sistemas avanzados (ASF), audio de remuestreo
- ASF (formato de sistemas avanzados), audio de remuestreo
- remuestreo de audio
- resampling audio,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5d95ed50117ac9d0fe7d71a2148314e1b9faf3ba8a26b99bb69083029b991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434479"
---
# <a name="audio-resampling"></a>Remuestreo de audio

Cada formato comprimido de un códec de audio tiene una frecuencia de muestreo y un tamaño de muestra específicos. No es necesario que coincidan con la configuración del formato de entrada o el formato de salida. Si un formato de entrada tiene una configuración diferente al formato comprimido descrito en el perfil, el escritor volverá a muestrear el audio, durante el proceso de codificación, para que coincida con el formato comprimido. El escritor acepta solo determinados formatos como entrada. Al enumerar los formatos de entrada de una secuencia de audio comprimida, todos los formatos recuperados se pueden volver a muestrear para que coincidan con el formato del perfil.

Al leer audio comprimido, el lector volverá a muestrear el contenido para que coincida con el formato de salida. Debe usar uno de los formatos de salida enumerados por el lector, por lo que se garantiza que el audio se puede volver a muestrear a la configuración del formato de salida.

Cada remuestreo afecta potencialmente a la calidad del audio. Cuando sea posible, debe usar formatos de entrada y salida con valores que coincidan con el formato comprimido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




