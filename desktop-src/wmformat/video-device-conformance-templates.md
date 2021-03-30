---
title: Plantillas de cumplimiento de dispositivos de vídeo
description: Plantillas de cumplimiento de dispositivos de vídeo
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- SDK de Windows Media Format, plantillas de conformidad de dispositivos
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
- SDK de Windows Media Format, plantillas de conformidad de dispositivos de vídeo
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos de vídeo
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos de vídeo
- Códec de Windows Media Video 9, plantillas de conformidad de dispositivos de vídeo
- códecs, códec de Windows Media Video 9
- plantillas de conformidad de dispositivos, vídeo
- plantillas de cumplimiento de dispositivos de vídeo
- plantillas, plantillas de conformidad de dispositivos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6735d029bc2339296fa2a0af8a48ace3303ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903862"
---
# <a name="video-device-conformance-templates"></a>Plantillas de cumplimiento de dispositivos de vídeo

En las tablas siguientes se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec Windows Media Video 9.

## <a name="simple-profile-low-level"></a>Perfil simple, bajo nivel



| Parámetro                                | Value                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "SP@LL"                                                                               |
| Dispositivos adecuados                      | Auriculares inalámbricos (solución de Microsoft Windows-Powered SmartPhone y dispositivos similares) |
| Resolución máxima                       | 176 x 144                                                                             |
| Velocidad de fotogramas máxima                       | 15 fps                                                                                |
| Velocidad de bits máxima                         | 96 Kbps                                                                               |
| Tamaño máximo de búfer (en unidades de 16384 bits) | 20 (aproximadamente 3,4 segundos con una velocidad de bits máxima)                                            |
| Codificación entrelazada                      | No                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Perfil simple, nivel medio



| Parámetro                                | Value                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "SP@ML"                                                                              |
| Dispositivos adecuados                      | Equipos de mano y datos personales assistantsHigh-end cables inalámbricos<br/> |
| Resolución máxima                       | 352 x 288                                                                            |
| Velocidad de fotogramas máxima                       | 15 fps @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Velocidad de bits máxima                         | 384 Kbps                                                                             |
| Tamaño máximo de búfer (en unidades de 16384 bits) | 77 (unos 3,3 segundos con una velocidad de bits máxima)                                           |
| Codificación entrelazada                      | No                                                                                   |



 

## <a name="generic-simple-profile"></a>Perfil sencillo genérico

Una secuencia que cumple con las limitaciones algorítmicas del perfil simple, pero no cabe en una de las especificaciones de nivel, se le asignará "SP" como su cadena de plantilla de conformidad de dispositivo.

## <a name="main-profile-low-level"></a>Perfil principal, bajo nivel



| Parámetro                                | Value                                       |
|------------------------------------------|---------------------------------------------|
| Cadena de plantilla                          | "MP@LL"                                     |
| Dispositivos adecuados                      | Set-top boxes                               |
| Resolución máxima                       | 352 x 288                                   |
| Velocidad de fotogramas máxima                       | 30 fps                                      |
| Velocidad de bits máxima                         | 2 Mbps                                      |
| Tamaño máximo de búfer (en unidades de 16384 bits) | 306 (unos 2,5 segundos con una velocidad de bits máxima) |
| Codificación entrelazada                      | No                                          |



 

## <a name="main-profile-medium-level"></a>Perfil principal, nivel medio



| Parámetro                                | Value                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "MP@ML"                                                                                                                |
| Dispositivos adecuados                      | Set-Top equipos boxesSlower con aceleración de vídeo de DirectX<br/> Reproductores de DVD habilitados para Windows Media<br/> |
| Resolución máxima                       | 720 x 576                                                                                                              |
| Velocidad de fotogramas máxima                       | 30 fps @ 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Velocidad de bits máxima                         | 10 Mbps                                                                                                                |
| Tamaño máximo de búfer (en unidades de 16384 bits) | 611 (aproximadamente un segundo a la velocidad de bits máxima)                                                                               |
| Codificación entrelazada                      | Sí                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Perfil principal, alto nivel



| Parámetro                                | Value                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "MP@HL"                                                                                                                                                               |
| Dispositivos adecuados                      | Equipos que usan vídeo de DirectX AccelerationHigh-Definition reproductores de DVD habilitados para Windows Media<br/> Cine digital<br/> streaming de alta definición<br/> |
| Resolución máxima                       | 1920 x 1080                                                                                                                                                           |
| Velocidad de fotogramas máxima                       | 30 fps @ 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Velocidad de bits máxima                         | 20 Mbps                                                                                                                                                               |
| Tamaño máximo de búfer (en unidades de 16384 bits) | 2442 (unos 2,66 segundos con una velocidad de bits máxima)                                                                                                                         |
| Codificación entrelazada                      | Sí                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Perfil principal genérico

Una secuencia que cumple con las limitaciones algorítmicas del perfil principal, pero no se ajusta a una de las especificaciones de nivel, se le asignará "MP" como su cadena de plantilla de cumplimiento de dispositivos.

## <a name="complex-profile"></a>Perfil complejo



| Parámetro       | Value                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Cadena de plantilla | CP                                                                                                                                   |
| Observaciones         | El perfil complejo no tiene limitaciones explícitas. Se usa para habilitar todos los algoritmos de códec, normalmente con fines de demostración. |



 

En las tablas siguientes se enumeran los parámetros de las plantillas de conformidad del dispositivo para el códec de imagen de Windows Media Video 9.

## <a name="video-image-level-1"></a>Nivel 1 de imagen de vídeo



| Parámetro                                | Value                                       |
|------------------------------------------|---------------------------------------------|
| Cadena de plantilla                          | I1                                        |
| Resolución máxima                       | 352 x 288                                   |
| Velocidad de fotogramas máxima                       | 30 fps                                      |
| Velocidad de bits máxima                         | 192 Kbps                                    |
| Tamaño máximo de búfer (en unidades de 16384 bits) | 39 (unos 3,26 segundos con una velocidad de bits máxima) |
| Codificación entrelazada                      | No                                          |



 

## <a name="video-image-level-2"></a>Nivel 2 de imagen de vídeo



| Parámetro                                | Value                                       |
|------------------------------------------|---------------------------------------------|
| Cadena de plantilla                          | I2                                        |
| Resolución máxima                       | 1024 x 768                                  |
| Velocidad de fotogramas máxima                       | 30 fps                                      |
| Velocidad de bits máxima                         | 384 Kbps                                    |
| Tamaño máximo de búfer (en unidades de 16384 bits) | 77 (unos 3,26 segundos con una velocidad de bits máxima) |
| Codificación entrelazada                      | No                                          |



 

## <a name="generic-video-image"></a>Imagen de vídeo genérica

Una secuencia de imágenes de vídeo que no quepa en una de las especificaciones de nivel se le asignará "I" como su cadena de plantilla de cumplimiento de dispositivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Plantillas de cumplimiento de dispositivos de audio**](audio-device-conformance-templates.md)
</dt> <dt>

[**Parámetros de plantilla de conformidad de dispositivos**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinaciones recomendadas de plantillas de cumplimiento de dispositivos**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





