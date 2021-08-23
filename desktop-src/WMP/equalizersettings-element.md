---
title: Elemento EQUALIZERSETTINGS
description: Elemento EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Reproductor de Windows Media máscaras, elemento EQUALIZERSETTINGS
- elemento skins,EQUALIZERSETTINGS
- Elemento EQUALIZERSETTINGS
- referencia para máscaras, elemento EQUALIZERSETTINGS
- elements,EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: facd5d9630536947614166bc8444ad38e33020920ce679180824ef9a3b007bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650955"
---
# <a name="equalizersettings-element"></a>Elemento EQUALIZERSETTINGS

El **elemento EQUALIZERSETTINGS** proporciona una manera de manipular el equalizer gráfico y otras configuraciones de audio de Reproductor de Windows Media mediante los atributos y el método enumerados aquí.

El **elemento EQUALIZERSETTINGS** admite los atributos siguientes.



| Atributo                                                          | Descripción                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [bandas](equalizersettings-bands.md)                               | Recupera el número de bandas de frecuencia admitidas.                                                      |
| [Bypass](equalizersettings-bypass.md)                             | Especifica o recupera un valor que indica si el filtro de equalizer se omite en el gráfico de filtros. |
| [Crossfade](equalizersettings-crossfade.md)                       | Especifica o recupera un valor que indica si está habilitada la atenuación cruzada.                                |
| [crossFadeWindow](equalizersettings-crossfadewindow.md)           | Especifica o recupera la cantidad de superposición de atenuación cruzada en milisegundos.                                |
| [currentPreset](equalizersettings-currentpreset.md)               | Especifica o recupera el índice del valor preestablecido actual.                                                 |
| [currentPresetTitle](equalizersettings-currentpresettitle.md)     | Recupera el título del valor preestablecido actual.                                                              |
| [currentSpeakerName](equalizersettings-currentspeakername.md)     | Recupera el nombre de la configuración actual del hablante.                                                      |
| [enableSplineTension](equalizersettings-enablesplinetension.md)   | Especifica o recupera un valor que indica si la curva spline está habilitada o deshabilitada.                |
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
| [Normalización](equalizersettings-normalization.md)               | Especifica o recupera un valor que indica si la normalización está habilitada.                             |
| [normalizationAverage](equalizersettings-normalizationaverage.md) | Recupera el valor de normalización promedio.                                                              |
| [normalizationPeak](equalizersettings-normalizationpeak.md)       | Recupera el valor de normalización máxima.                                                                 |
| [presetCount](equalizersettings-presetcount.md)                   | Recupera el número de valores preestablecidos disponibles.                                                              |
| [speakerSize](equalizersettings-speakersize.md)                   | Especifica o recupera el índice del tamaño del altavoz actual.                                           |
| [splineTension](equalizersettings-splinetension.md)               | Especifica o recupera la curva spline para el control de igualador.                                    |
| [truBassLevel](equalizersettings-trubasslevel.md)                 | Especifica o recupera el nivel de TruBass de SRS.                                                           |
| [wowLevel](equalizersettings-wowlevel.md)                         | Especifica o recupera el nivel de efecto WOW de SRS.                                                        |



 

El **elemento EQUALIZERSETTINGS** admite los métodos siguientes.



| Método                                                 | Descripción                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [nextPreset](equalizersettings-nextpreset.md)         | Aplica el siguiente valor preestablecido del igualador.                                   |
| [presetTitle](equalizersettings-presettitle.md)       | Recupera el nombre del valor preestablecido del igualador con el índice especificado. |
| [previousPreset](equalizersettings-previouspreset.md) | Aplica el valor preestablecido del igualador anterior.                               |
| [reset](equalizersettings-reset.md)                   | Restablece los niveles de ganancia de todas las bandas a cero decibelios.                |



 

El **elemento EQUALIZERSETTINGS** puede implementar los [controladores de eventos \_ onchange](attribute-onchange.md) del atributo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




