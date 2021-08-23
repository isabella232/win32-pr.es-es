---
title: Estructuras de cliente drm Windows multimedia de Microsoft
description: Estructuras de cliente drm Windows multimedia de Microsoft
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- Windows SDK de formato multimedia, estructuras
- administración de derechos digitales (DRM), estructuras
- DRM (administración de derechos digitales), estructuras
- API extendidas de cliente DRM, estructuras
- API extendidas de cliente, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 145381cc6d702dd338176ffa89983de137285dcd7aef946d3ece956eb450880c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447845"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Estructuras de cliente drm Windows multimedia de Microsoft

Las siguientes estructuras son compatibles con las API extendidas de Windows DRM multimedia.



| Estructura o enumeración                                                                    | Descripción                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ DRM**](drm-audio-output-protection-ids.md)              | Contiene una lista de identificadores de protección de salida de audio.                                                                                                     |
| [**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ \_ DRM, POR EJEMPLO,**](drm-audio-output-protection-ids-ex.md)       | Contiene una lista de identificadores de protección de salida de audio. Esta estructura amplía los identificadores **de PROTECCIÓN DE SALIDA DE AUDIO \_ \_ \_ \_ DE DRM** agregando un número de versión.          |
| [**OPL \_ DE COPIA DE DRM \_**](drmdrm-copy-opl.md)                                                   | Contiene información sobre los niveles de protección de salida especificados en una licencia para las acciones de copia.                                                               |
| [**DATOS DE \_ ESTADO DE \_ LICENCIA \_ DE DRM**](drmdrm-license-state-data.md)                              | Contiene información sobre las restricciones de licencia para un derecho DRM.                                                                                        |
| [**NIVELES \_ MÍNIMOS \_ DE PROTECCIÓN DE \_ SALIDA DE \_ DRM**](drmdrm-minimum-output-protection-levels.md) | Contiene los niveles mínimos de protección de salida (OPL) para la reproducción de varios tipos de contenido.                                                                 |
| [**IDENTIFICADORES \_ DE SALIDA DE OPL \_ \_ DE DRM**](drmdrm-opl-output-ids.md)                                      | Contiene varios identificadores de salida de OPL.                                                                                                                   |
| [**PROTECCIÓN DE SALIDA DE DRM \_ \_**](drm-output-protection.md)                                    | Contiene información sobre una tecnología de protección de salida.                                                                                                    |
| [**DRM \_ OUTPUT \_ PROTECTION \_ EX**](drm-output-protection-ex.md)                             | Contiene información sobre una tecnología de protección de salida. Esta estructura amplía DRM **\_ OUTPUT PROTECTION \_ agregando** un número de versión.                     |
| [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)                                                   | Contiene información sobre las OCL especificadas en una licencia para las acciones de reproducción.                                                                                   |
| [**DRM \_ PLAY \_ OPL \_ EX**](drm-play-opl-ex.md)                                               | Contiene información ampliada sobre las OCL especificadas en una licencia para las acciones de reproducción.                                                                          |
| [**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ DRM**](drmdrm-video-output-protection-ids.md)           | Contiene una matriz de estructuras **DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.**                                                                                            |
| [**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ \_ DRM, POR EJEMPLO,**](drm-video-output-protection-ids-ex.md)       | Contiene una matriz de estructuras **DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.** Esta estructura amplía los identificadores de PROTECCIÓN DE SALIDA DE VÍDEO **\_ \_ \_ \_ DE DRM** agregando un número de versión. |
| [**ESTADO DE \_ RESTAURACIÓN \_ DE COPIA DE SEGURIDAD \_ DE WM**](wm-backup-restore-status.md)                             | Contiene información sobre una operación de copia de seguridad o restauración de licencias pendiente.                                                                                      |
| [**ESTADO \_ DE INDIVIDUALIZACIÓN \_ DE WM**](drmwm-individualize-status.md)                             | Contiene información sobre un proceso de individualización pendiente.                                                                                                |
| [**RESTRICCIONES DE \_ VÍDEO ANÁLOGO \_ DE WMDRM \_**](wmdrm-analog-video-restrictions.md)               | Contiene información sobre una restricción para reproducir contenido como vídeo análogo.                                                                             |
| [**RESTRICCIONES DE VÍDEO ANÁLOGO DE WMDRM, \_ \_ POR \_ \_ EJEMPLO,**](wmdrm-analog-video-restrictions-ex.md)        | Contiene información ampliada sobre una restricción para reproducir contenido como vídeo análogo.                                                                    |
| [**BLOQUE DE DISPERSIÓN \_ DE CIFRADO DE WMDRM \_ \_**](wmdrm-encrypt-scatter-block.md)                       | Contiene un bloque de datos que se va a cifrar.                                                                                                                   |
| [**INFORMACIÓN DE DISPERSIÓN \_ DE CIFRADO \_ DE WMDRM \_**](wmdrm-encrypt-scatter-info.md)                         | Contiene la información necesaria para configurar [**la interfaz IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para su uso.                                        |
| [**FILTRO DE LICENCIA \_ \_ WMDRM**](wmdrm-license-filter.md)                                      | Contiene información de filtrado para crear enumeraciones de licencias.                                                                                           |
| [**NIVELES DE PROTECCIÓN DE \_ SALIDA \_ \_ WMDRM**](wmdrm-output-protection-levels.md)                 | Contiene los niveles de protección de salida requeridos por una licencia para realizar varias acciones.                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | Contiene información sobre el algoritmo criptográfico utilizado para cifrar y descifrar el contenido.                                                                 |
| [**DIRECTIVA DE \_ WMDRMNET**](wmdrmnet-policy.md)                                                 | Contiene la directiva que se va a usar para Windows DRM multimedia para las operaciones de dispositivos de red.                                                                        |
| [**REQUISITOS GLOBALES DE LA \_ DIRECTIVA DE WMDRMNET \_ \_**](wmdrmnet-policy-global-requirements.md)       | Contiene los requisitos globales para Windows DRM multimedia para dispositivos de red.                                                                                        |
| [**ENTORNO MÍNIMO DE DIRECTIVA \_ DE WMDRMNET \_ \_**](wmdrmnet-policy-minimum-environment.md)       | Contiene los requisitos mínimos de seguridad para Windows DRM multimedia para dispositivos de red.                                                                       |
| [**TRANSCRYPTPLAY DE \_ DIRECTIVA DE WMDRMNET \_**](wmdrmnet-policy-transcryptplay.md)                  | Contiene la información de directiva para reproducir contenido mediante Windows DRM multimedia para dispositivos de red.                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](drm-programming-reference.md)
</dt> </dl>

 

 




