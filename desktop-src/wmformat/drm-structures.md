---
title: Estructuras de cliente DRM de Microsoft Windows Media
description: Estructuras de cliente DRM de Microsoft Windows Media
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- SDK de Windows Media Format, estructuras
- Administración de derechos digitales (DRM), estructuras
- DRM (administración de derechos digitales), estructuras
- API extendidas del cliente DRM, estructuras
- API extendidas de cliente, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43264c37ed9830026f87998823017d17c9d75f7e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421773"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Estructuras de cliente DRM de Microsoft Windows Media

Las siguientes estructuras son compatibles con las API extendidas del cliente DRM de Windows Media.



| Estructura o enumeración                                                                    | Descripción                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ identificadores de protección de salida de audio DRM \_**](drm-audio-output-protection-ids.md)              | Contiene una lista de identificadores de protección de salida de audio.                                                                                                     |
| [**\_ \_ \_ identificadores de protección de salida de \_ audio DRM \_**](drm-audio-output-protection-ids-ex.md)       | Contiene una lista de identificadores de protección de salida de audio. Esta estructura extiende **los \_ \_ \_ \_ identificadores de protección de salida de audio DRM** agregando un número de versión.          |
| [**el \_ OPL de copia de DRM \_**](drmdrm-copy-opl.md)                                                   | Contiene información sobre los niveles de protección de salida especificados en una licencia para las acciones de copia.                                                               |
| [**\_datos de \_ Estado de licencia de DRM \_**](drmdrm-license-state-data.md)                              | Contiene información sobre las restricciones de licencia para un derecho DRM.                                                                                        |
| [**\_niveles de \_ protección de salida mínima \_ de DRM \_**](drmdrm-minimum-output-protection-levels.md) | Contiene los niveles mínimos de protección de salida (OPLs) para la reproducción de varios tipos de contenido.                                                                 |
| [**ID. de salida de OPL de DRM \_ \_ \_**](drmdrm-opl-output-ids.md)                                      | Contiene varios identificadores de salida de OPL.                                                                                                                   |
| [**\_protección de salida de DRM \_**](drm-output-protection.md)                                    | Contiene información acerca de una tecnología de protección de la salida.                                                                                                    |
| [**\_protección de salida DRM \_ \_ ex**](drm-output-protection-ex.md)                             | Contiene información acerca de una tecnología de protección de la salida. Esta estructura extiende **la \_ \_ protección de salida de DRM** agregando un número de versión.                     |
| [**el \_ OPL de reproducción de DRM \_**](drmdrm-play-opl.md)                                                   | Contiene información acerca de los OPLs especificados en una licencia para las acciones de reproducción.                                                                                   |
| [**el \_ OPL de reproducción de DRM \_ \_ ex**](drm-play-opl-ex.md)                                               | Contiene información ampliada sobre el OPLs especificado en una licencia para las acciones de reproducción.                                                                          |
| [**\_ \_ \_ identificadores de protección de salida de vídeo DRM \_**](drmdrm-video-output-protection-ids.md)           | Contiene una matriz de estructuras de **\_ protección de \_ salida \_ de vídeo DRM** .                                                                                            |
| [**\_ \_ \_ identificadores de protección de salida de \_ vídeo DRM \_**](drm-video-output-protection-ids-ex.md)       | Contiene una matriz de estructuras de **\_ protección de \_ salida \_ de vídeo DRM** . Esta estructura extiende **los \_ \_ \_ \_ identificadores de protección de salida de vídeo DRM** agregando un número de versión. |
| [**Estado de restauración de copia de seguridad de WM \_ \_ \_**](wm-backup-restore-status.md)                             | Contiene información sobre una operación de copia de seguridad o restauración de una licencia pendiente.                                                                                      |
| [**Estado de la \_ individualización de WM \_**](drmwm-individualize-status.md)                             | Contiene información sobre un proceso de individualización pendiente.                                                                                                |
| [**\_restricciones de \_ vídeo \_ analógico de WMDRM**](wmdrm-analog-video-restrictions.md)               | Contiene información sobre una restricción para reproducir contenido como vídeo analógico.                                                                             |
| [**\_restricciones de vídeo analógico de WMDRM \_ \_ \_ ex**](wmdrm-analog-video-restrictions-ex.md)        | Contiene información ampliada sobre una restricción para reproducir contenido como vídeo analógico.                                                                    |
| [**\_bloque de \_ dispersión cifrado de WMDRM \_**](wmdrm-encrypt-scatter-block.md)                       | Contiene un bloque de datos que se van a cifrar.                                                                                                                   |
| [**\_cifrado de la \_ información de dispersión de WMDRM \_**](wmdrm-encrypt-scatter-info.md)                         | Contiene la información necesaria para configurar la interfaz [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para su uso.                                        |
| [**\_filtro de licencias de WMDRM \_**](wmdrm-license-filter.md)                                      | Contiene información de filtrado para crear enumeraciones de licencias.                                                                                           |
| [**\_niveles de \_ protección de salida de WMDRM \_**](wmdrm-output-protection-levels.md)                 | Contiene los niveles de protección de salida requeridos por una licencia para realizar diversas acciones.                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | Contiene información sobre el algoritmo criptográfico usado para cifrar y descifrar contenido.                                                                 |
| [**\_Directiva WMDRMNET**](wmdrmnet-policy.md)                                                 | Contiene la Directiva que se va a usar para las operaciones de DRM de Windows Media para dispositivos de red.                                                                        |
| [**\_ \_ requisitos globales de la Directiva WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)       | Contiene los requisitos globales para DRM de Windows Media para dispositivos de red.                                                                                        |
| [**\_ \_ entorno mínimo de directiva de WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)       | Contiene los requisitos de seguridad mínimos para Windows Media DRM para dispositivos de red.                                                                       |
| [**\_TRANSCRYPTPLAY de directiva de WMDRMNET \_**](wmdrmnet-policy-transcryptplay.md)                  | Contiene la información de la Directiva para reproducir contenido con DRM de Windows Media para dispositivos de red.                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](drm-programming-reference.md)
</dt> </dl>

 

 




