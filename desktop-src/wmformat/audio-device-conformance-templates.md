---
title: Plantillas de cumplimiento de dispositivos de audio
description: Plantillas de cumplimiento de dispositivos de audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- SDK de Windows Media Format, plantillas de conformidad de dispositivos
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
- SDK de Windows Media Format, plantillas de conformidad de dispositivos de audio
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos de audio
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos de audio
- Códec de Windows Media Audio 9, plantillas de conformidad de dispositivos de audio
- códecs, códec de Windows Media Audio 9
- plantillas de conformidad de dispositivos, vídeo
- plantillas de cumplimiento de dispositivos de audio
- plantillas, plantillas de conformidad de dispositivos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357077"
---
# <a name="audio-device-conformance-templates"></a>Plantillas de cumplimiento de dispositivos de audio

En la tabla siguiente se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec Windows Media Audio 9, o posterior.



| Cadena de plantilla | Intervalo de velocidad de bits     | Notas                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nivel            | 64 Kbps 160 Kbps | Esta plantilla está pensada para dispositivos solo de audio restringidos.                                                                                                                                                                        |
| L2            | <= 160 Kbps     | Esta plantilla corresponde a la clase 4 del kit de portabilidad de Windows Media Audio, que admite toda la implementación del descodificador de Windows Media Audio.                                                                                   |
| Caché            | <= 384 Kbps     | Esta plantilla corresponde a la clase 4 del kit de portabilidad de Windows Media Audio, que admite toda la implementación del descodificador de Windows Media Audio. El intervalo de velocidad de bits es la única diferencia entre esta plantilla y L2.<br/> |
| CG             | Velocidades de bits      | Esta plantilla solo se usa con equipos personales y se utiliza normalmente para mostrar todas las capacidades del códec.                                                                                                           |



 

En la tabla siguiente se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec de voz de Windows Media Audio 9.



| Cadena de plantilla | Intervalo de velocidad de bits | Notas                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| S1            | <= 20 Kbps  | Esta plantilla está pensada solo para dispositivos de poca complejidad. Esta plantilla es solo voz.<br/>                    |
| S2            | <= 20 Kbps  | Esta es la plantilla recomendada para la mayoría de las aplicaciones. Esta plantilla admite combinaciones de voz y música.<br/> |



 

En la tabla siguiente se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec Windows Media Audio 9 Professional o posterior.



| Cadena de plantilla | Propiedades                                                                                   | Notas                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conector            | Velocidad de bits <= 384 tasa de KbpsSampling <= 48 kHz<br/> Canales <= 5,1<br/>   | Esta plantilla se recomienda para películas estándar con sonido envolvente.                                                                                                                                                                           |
| ²            | Velocidad de bits <= 768 tasa de KbpsSampling <= 96 kHz<br/> Canales <= 5,1<br/>   | Esta plantilla se recomienda para películas de alta definición con sonido envolvente.                                                                                                                                                                    |
| M3            | Velocidad de bits <= 1.500 tasa de KbpsSampling <= 96 kHz<br/> Canales <= 7,1<br/> | Esta plantilla se recomienda para películas de alta definición con sonido envolvente de 8 canales, como contenido codificado para presentación en teatro.                                                                                                    |
| "M"             | Tasas de muestreo de todos los bits ratesAll<br/> Todos los canales<br/>                           | Esta plantilla solo se usa con equipos personales y se utiliza normalmente para mostrar todas las capacidades del códec. Esta es también la designación de plantilla para todo el audio codificado con el códec Windows Media Audio 9 Lossless.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Parámetros de plantilla de conformidad de dispositivos**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinaciones recomendadas de plantillas de cumplimiento de dispositivos**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Plantillas de cumplimiento de dispositivos de vídeo**](video-device-conformance-templates.md)
</dt> </dl>

 

 





