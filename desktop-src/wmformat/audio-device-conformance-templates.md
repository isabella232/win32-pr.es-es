---
title: Plantillas de conformidad de dispositivos de audio
description: Plantillas de conformidad de dispositivos de audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows SDK de formato multimedia, plantillas de conformidad de dispositivos
- Formato de sistemas avanzados (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
- Windows SDK de formato multimedia, plantillas de conformidad de dispositivos de audio
- Formato de sistemas avanzados (ASF), plantillas de conformidad de dispositivos de audio
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos de audio
- Windows Códec Media Audio 9, plantillas de conformidad de dispositivos de audio
- codecs,Windows códec Media Audio 9
- plantillas de conformidad de dispositivos, vídeo
- plantillas de conformidad de dispositivos de audio
- templates,audio device conformance templates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b66c3c414ef2132120cb0824e1e48847310396cf8002d95be13d7f841a0ff6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840255"
---
# <a name="audio-device-conformance-templates"></a>Plantillas de conformidad de dispositivos de audio

En la tabla siguiente se enumeran las plantillas de conformidad de dispositivos y los parámetros asociados para el códec Windows Media Audio 9 o posterior.



| Cadena de plantilla | Intervalo de velocidad de bits     | Notas                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "L1"            | 64 Kbps 160 Kbps | Esta plantilla está pensada para dispositivos de solo audio restringidos.                                                                                                                                                                        |
| "L2"            | <= 160 Kbps     | Esta plantilla corresponde a la clase 4 del kit de porte de Windows Media Audio, que admite toda la implementación del descodificador Windows Media Audio.                                                                                   |
| "L3"            | <= 384 Kbps     | Esta plantilla corresponde a la clase 4 del kit de porte de Windows Media Audio, que admite toda la implementación del descodificador Windows Media Audio. El intervalo de velocidad de bits es la única diferencia entre esta plantilla y L2.<br/> |
| "L"             | Todas las velocidades de bits      | Esta plantilla solo se usa con equipos personales y normalmente se usa para mostrar todas las funcionalidades del códec.                                                                                                           |



 

En la tabla siguiente se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec Windows Media Audio 9 Voice.



| Cadena de plantilla | Intervalo de velocidad de bits | Notas                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| "S1"            | <= 20 Kbps  | Esta plantilla está pensada solo para dispositivos de muy baja complejidad. Esta plantilla es de solo voz.<br/>                    |
| "S2"            | <= 20 Kbps  | Esta es la plantilla recomendada para la mayoría de las aplicaciones. Esta plantilla admite combinaciones de voz y música.<br/> |



 

En la tabla siguiente se enumeran las plantillas de conformidad de dispositivos y los parámetros asociados para el códec Windows Media Audio 9 Professional o posterior.



| Cadena de plantilla | Propiedades                                                                                   | Notas                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "M1"            | Velocidad de bits <= 384 KbpsSampling rate <= 48 kHz<br/> Canales <= 5,1<br/>   | Esta plantilla se recomienda para películas estándar con sonido envolvente.                                                                                                                                                                           |
| "M2"            | Velocidad de bits <= 768 KbpsSampling rate <= 96 kHz<br/> Canales <= 5,1<br/>   | Esta plantilla se recomienda para películas de alta definición con sonido envolvente.                                                                                                                                                                    |
| "M3"            | Velocidad de bits <= 1500 KbpsSampling rate <= 96 kHz<br/> Channels <= 7.1<br/> | Esta plantilla se recomienda para películas de alta definición con sonido envolvente de 8 canales, como contenido codificado para presentación en salas de cine.                                                                                                    |
| "M"             | Todas las velocidades de bitsTodas las velocidades de muestreo<br/> Todos los canales<br/>                           | Esta plantilla solo se usa con equipos personales y normalmente se usa para mostrar todas las funcionalidades del códec. Esta es también la designación de plantilla para todo el audio codificado con el códec Windows media audio 9 sin pérdida.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Parámetros de plantilla de conformidad de dispositivos**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinaciones recomendadas de plantillas de conformidad de dispositivos**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Plantillas de conformidad de dispositivos de vídeo**](video-device-conformance-templates.md)
</dt> </dl>

 

 





