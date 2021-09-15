---
title: Plantillas de conformidad de dispositivos de vídeo
description: Plantillas de conformidad de dispositivos de vídeo
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- Windows SDK de formato multimedia, plantillas de conformidad de dispositivos
- Formato de sistemas avanzados (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
- Windows SDK de formato multimedia, plantillas de conformidad de dispositivos de vídeo
- Formato de sistemas avanzados (ASF), plantillas de conformidad de dispositivos de vídeo
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos de vídeo
- Windows Códec Media Video 9, plantillas de conformidad de dispositivos de vídeo
- codecs,Windows códec Media Video 9
- plantillas de conformidad de dispositivos, vídeo
- plantillas de conformidad de dispositivos de vídeo
- templates,video device conformance templates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6735d029bc2339296fa2a0af8a48ace3303ae3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572133"
---
# <a name="video-device-conformance-templates"></a>Plantillas de conformidad de dispositivos de vídeo

En las tablas siguientes se muestran las plantillas de conformidad de dispositivos y los parámetros asociados para el códec Windows Media Video 9.

## <a name="simple-profile-low-level"></a>Perfil simple, bajo nivel



| Parámetro                                | Value                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "SP@LL"                                                                               |
| Dispositivos adecuados                      | Conjuntos de manos inalámbricos (Microsoft Windows-Powered SmartPhone Solution y dispositivos similares) |
| Resolución máxima                       | 176 x 144                                                                             |
| Velocidad máxima de fotogramas                       | 15 fps                                                                                |
| Velocidad de bits máxima                         | 96 Kbps                                                                               |
| Tamaño máximo del búfer (en unidades de 16384 bits) | 20 (aproximadamente 3,4 segundos a velocidad de bits máxima)                                            |
| Codificación entrelazada                      | No                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Perfil simple, nivel medio



| Parámetro                                | Value                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "SP@ML"                                                                              |
| Dispositivos adecuados                      | Equipos portátiles y asistentes de datos personalesHigh-end wireless handsets<br/> |
| Resolución máxima                       | 352 x 288                                                                            |
| Velocidad máxima de fotogramas                       | 15 fps @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Velocidad de bits máxima                         | 384 Kbps                                                                             |
| Tamaño máximo del búfer (en unidades de 16384 bits) | 77 (aproximadamente 3,3 segundos a velocidad de bits máxima)                                           |
| Codificación entrelazada                      | No                                                                                   |



 

## <a name="generic-simple-profile"></a>Perfil simple genérico

A una secuencia que cumpla las limitaciones algorítmicas del perfil simple, pero que no se ajuste a una de las especificaciones de nivel, se le asignará "SP" como su cadena de plantilla de conformidad de dispositivo.

## <a name="main-profile-low-level"></a>Perfil principal, nivel bajo



| Parámetro                                | Value                                       |
|------------------------------------------|---------------------------------------------|
| Cadena de plantilla                          | "MP@LL"                                     |
| Dispositivos adecuados                      | Establecer los cuadros superiores                               |
| Resolución máxima                       | 352 x 288                                   |
| Velocidad máxima de fotogramas                       | 30 fps                                      |
| Velocidad de bits máxima                         | 2 Mbps                                      |
| Tamaño máximo del búfer (en unidades de 16384 bits) | 306 (unos 2,5 segundos con velocidad de bits máxima) |
| Codificación entrelazada                      | No                                          |



 

## <a name="main-profile-medium-level"></a>Perfil principal, nivel medio



| Parámetro                                | Value                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "MP@ML"                                                                                                                |
| Dispositivos adecuados                      | Set-top boxesSlower computers using DirectX Video Acceleration<br/> Windows Reproductores de DVD habilitados para medios<br/> |
| Resolución máxima                       | 720 x 576                                                                                                              |
| Velocidad máxima de fotogramas                       | 30 fps @ 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Velocidad de bits máxima                         | 10 Mbps                                                                                                                |
| Tamaño máximo del búfer (en unidades de 16384 bits) | 611 (aproximadamente 1 segundo a velocidad de bits máxima)                                                                               |
| Codificación entrelazada                      | Sí                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Perfil principal, alto nivel



| Parámetro                                | Value                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadena de plantilla                          | "MP@HL"                                                                                                                                                               |
| Dispositivos adecuados                      | Equipos que usan reproductores de DVD habilitados para DirectX Video AccelerationHigh-Definition Windows Media<br/> Digital digital<br/> streaming de alta definición<br/> |
| Resolución máxima                       | 1920 x 1080                                                                                                                                                           |
| Velocidad máxima de fotogramas                       | 30 fps @ 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Velocidad de bits máxima                         | 20 Mbps                                                                                                                                                               |
| Tamaño máximo del búfer (en unidades de 16384 bits) | 2442 (aproximadamente 2,66 segundos a velocidad de bits máxima)                                                                                                                         |
| Codificación entrelazada                      | Sí                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Perfil principal genérico

A una secuencia que cumpla las limitaciones algorítmicas del perfil principal, pero que no se ajuste a una de las especificaciones de nivel, se le asignará "MP" como cadena de plantilla de conformidad de dispositivo.

## <a name="complex-profile"></a>Perfil complejo



| Parámetro       | Value                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Cadena de plantilla | "CP"                                                                                                                                   |
| Observaciones         | El perfil complejo no tiene limitaciones explícitas. Se usa para habilitar todos los algoritmos de códec, normalmente con fines de demostración. |



 

En las tablas siguientes se muestran los parámetros de las plantillas de conformidad del dispositivo para el códec Windows imagen de Media Video 9.

## <a name="video-image-level-1"></a>Imagen de vídeo nivel 1



| Parámetro                                | Value                                       |
|------------------------------------------|---------------------------------------------|
| Cadena de plantilla                          | "I1"                                        |
| Resolución máxima                       | 352 x 288                                   |
| Velocidad máxima de fotogramas                       | 30 fps                                      |
| Velocidad de bits máxima                         | 192 Kbps                                    |
| Tamaño máximo del búfer (en unidades de 16384 bits) | 39 (unos 3,26 segundos a velocidad máxima de bits) |
| Codificación entrelazada                      | No                                          |



 

## <a name="video-image-level-2"></a>Imagen de vídeo nivel 2



| Parámetro                                | Value                                       |
|------------------------------------------|---------------------------------------------|
| Cadena de plantilla                          | "I2"                                        |
| Resolución máxima                       | 1024 x 768                                  |
| Velocidad máxima de fotogramas                       | 30 fps                                      |
| Velocidad de bits máxima                         | 384 Kbps                                    |
| Tamaño máximo del búfer (en unidades de 16384 bits) | 77 (aproximadamente 3,26 segundos a velocidad de bits máxima) |
| Codificación entrelazada                      | No                                          |



 

## <a name="generic-video-image"></a>Imagen de vídeo genérica

A una secuencia de imagen de vídeo que no cabe en una de las especificaciones de nivel se le asignará "I" como su cadena de plantilla de conformidad de dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Plantillas de conformidad de dispositivos de audio**](audio-device-conformance-templates.md)
</dt> <dt>

[**Parámetros de plantilla de conformidad de dispositivos**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinaciones recomendadas de plantillas de conformidad de dispositivos**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





