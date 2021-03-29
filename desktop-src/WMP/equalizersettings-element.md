---
title: Elemento EQUALIZERSETTINGS
description: Elemento EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Aspectos de Windows Media Player, elemento EQUALIZERSETTINGS
- aspectos, elemento EQUALIZERSETTINGS
- Elemento EQUALIZERSETTINGS
- referencia de las máscaras, elemento EQUALIZERSETTINGS
- elementos, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532164"
---
# <a name="equalizersettings-element"></a>Elemento EQUALIZERSETTINGS

El elemento **EQUALIZERSETTINGS** proporciona una manera de manipular el ecualizador gráfico y otras configuraciones de audio de Windows Media Player utilizando los atributos y el método que se enumeran aquí.

El elemento **EQUALIZERSETTINGS** admite los siguientes atributos.



| Atributo                                                          | Descripción                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [bandas](equalizersettings-bands.md)                               | Recupera el número de bandas de frecuencia admitidas.                                                      |
| [alto](equalizersettings-bypass.md)                             | Especifica o recupera un valor que indica si se omite el filtro del ecualizador en el gráfico de filtros. |
| [Encadenada](equalizersettings-crossfade.md)                       | Especifica o recupera un valor que indica si está habilitado el fundido cruzado.                                |
| [crossFadeWindow](equalizersettings-crossfadewindow.md)           | Especifica o recupera la cantidad de superposición entre fundidos en milisegundos.                                |
| [currentPreset](equalizersettings-currentpreset.md)               | Especifica o recupera el índice del valor preestablecido actual.                                                 |
| [currentPresetTitle](equalizersettings-currentpresettitle.md)     | Recupera el título del valor preestablecido actual.                                                              |
| [currentSpeakerName](equalizersettings-currentspeakername.md)     | Recupera el nombre de la configuración del orador actual.                                                      |
| [enableSplineTension](equalizersettings-enablesplinetension.md)   | Especifica o recupera un valor que indica si la tensión spline está habilitada o deshabilitada.                |
| [enhancedAudio](equalizersettings-enhancedaudio.md)               | Especifica o recupera un valor que indica si el audio mejorado está activado.                          |
| [gainLevels](equalizersettings-gainlevels.md)                     | Especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.                  |
| [gainLevel1](equalizersettings-gainlevel1.md)                     | Especifica o recupera el nivel de ganancia de la banda 1.                                                        |
| [gainLevel2](equalizersettings-gainlevel2.md)                     | Especifica o recupera el nivel de ganancia de la banda 2.                                                        |
| [gainLevel3](equalizersettings-gainlevel3.md)                     | Especifica o recupera el nivel de ganancia de la banda 3.                                                        |
| [gainLevel4](equalizersettings-gainlevel4.md)                     | Especifica o recupera el nivel de ganancia de la banda 4.                                                        |
| [gainLevel5](equalizersettings-gainlevel5.md)                     | Especifica o recupera el nivel de ganancia de la banda 5.                                                        |
| [gainLevel6](equalizersettings-gainlevel6.md)                     | Especifica o recupera el nivel de ganancia de la banda 6.                                                        |
| [gainLevel7](equalizersettings-gainlevel7.md)                     | Especifica o recupera el nivel de ganancia de la banda 7.                                                        |
| [gainLevel8](equalizersettings-gainlevel8.md)                     | Especifica o recupera el nivel de ganancia de la banda 8.                                                        |
| [gainLevel9](equalizersettings-gainlevel9.md)                     | Especifica o recupera el nivel de ganancia de la banda 9.                                                        |
| [gainLevel10](equalizersettings-gainlevel10.md)                   | Especifica o recupera el nivel de ganancia de la banda 10.                                                       |
| [normalización](equalizersettings-normalization.md)               | Especifica o recupera un valor que indica si está habilitada la normalización.                             |
| [normalizationAverage](equalizersettings-normalizationaverage.md) | Recupera el valor de normalización promedio.                                                              |
| [normalizationPeak](equalizersettings-normalizationpeak.md)       | Recupera el valor de normalización máximo.                                                                 |
| [presetCount](equalizersettings-presetcount.md)                   | Recupera el número de valores preestablecidos disponibles.                                                              |
| [Altavoces](equalizersettings-speakersize.md)                   | Especifica o recupera el índice del tamaño de altavoz actual.                                           |
| [splineTension](equalizersettings-splinetension.md)               | Especifica o recupera la tensión spline para el control de ecualizador.                                    |
| [truBassLevel](equalizersettings-trubasslevel.md)                 | Especifica o recupera el nivel de TruBass de SRS.                                                           |
| [wowLevel](equalizersettings-wowlevel.md)                         | Especifica o recupera el nivel de efecto SRS WOW.                                                        |



 

El elemento **EQUALIZERSETTINGS** admite los siguientes métodos.



| Método                                                 | Descripción                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [nextPreset](equalizersettings-nextpreset.md)         | Aplica el siguiente valor preestablecido del ecualizador.                                   |
| [presetTitle](equalizersettings-presettitle.md)       | Recupera el nombre del valor preestablecido del ecualizador con el índice especificado. |
| [previousPreset](equalizersettings-previouspreset.md) | Aplica el valor preestablecido del ecualizador anterior.                               |
| [reset](equalizersettings-reset.md)                   | Restablece los niveles de ganancia de todas las bandas a cero decibelios.                |



 

El elemento **EQUALIZERSETTINGS** puede implementar los controladores de eventos [ \_ onchange de atributo](attribute-onchange.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




