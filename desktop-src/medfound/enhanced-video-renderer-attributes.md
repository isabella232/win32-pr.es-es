---
description: Atributos evr
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: Atributos evr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5af186a909dc672876eb12846e842360ccabfd3f2cc1de8f203d3e40d94ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974544"
---
# <a name="evr-attributes"></a>Atributos evr

Los atributos siguientes se pueden usar para configurar el representador de vídeo mejorado (EVR).



| Atributo                                                                                                         | Descripción                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | Permite a evr procesar por lotes las llamadas al método **IDirect3DDevice9::P de Microsoft Direct3D.**                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | Permite que la EVR mejore el rendimiento mediante el desinterlazado bob.                                                        |
| [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)                                     | Permite que la EVR mejore el rendimiento omitiendo el segundo campo de cada fotograma entrelazado.                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | Permite que la EVR limite su salida para que coincida con el ancho de banda de GPU.                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | Permite que la EVR mezcle el vídeo dentro de un rectángulo que sea menor que el rectángulo de salida y, a continuación, escale el resultado. |
| [ForceBatching de EVRConfig \_](evrconfig-forcebatching.md)                                                           | Fuerza al EVR a llamar por lotes al **método IDirect3D9Device::P resent.**                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | Fuerza al EVR a usar el desinterlazado bob.                                                                                 |
| [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)                                                 | Fuerza al EVR a omitir el segundo campo de cada fotograma entrelazado.                                                       |
| [ForceScaling de EVRConfig \_](evrconfig-forcescaling.md)                                                             | Fuerza al EVR a mezclar el vídeo dentro de un rectángulo que es más pequeño que el rectángulo de salida y, a continuación, escalar el resultado. |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | Obliga al EVR a limitar su salida para que coincida con el ancho de banda de GPU.                                                               |
| [**ACTIVACIÓN DEL MEZCLADOR DE VÍDEO PERSONALIZADO DE MF \_ \_ \_ \_ \_ ACTIVATE**](mf-activate-custom-video-mixer-activate-attribute.md)         | Especifica un objeto de activación que crea un mezclador de vídeo personalizado para el representador de vídeo mejorado (EVR).                  |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID de un mezclador de vídeo personalizado para la EVR.                                                                               |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ FLAGS**](mf-activate-custom-video-mixer-flags-attribute.md)               | Especifica cómo crear un mezclador personalizado para el EVR.                                                                      |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ PRESENTER \_ ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Especifica un objeto de activación que crea un presentador de vídeo personalizado para la EVR.                                        |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ PRESENTER \_ CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID de un presentador de vídeo personalizado para la EVR.                                                                           |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ PRESENTER \_ FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md)       | Especifica cómo crear un presentador personalizado para la EVR.                                                                  |
| [**VENTANA \_ DE VÍDEO DE ACTIVACIÓN DE \_ \_ MF**](mf-activate-video-window-attribute.md)                                         | Identificador de la ventana de recorte de vídeo.                                                                                     |
| [**MF \_ SA \_ REQUIRED \_ SAMPLE \_ COUNT**](mf-sa-required-sample-count-attribute.md)                                  | Indica el número de búferes sin comprimir que el receptor de medios EVR requiere para desenlazar.                         |
| [**RECT \_ DE ZOOM \_ DE VÍDEO**](video-zoom-rect-attribute.md)                                                            | Especifica el rectángulo de zoom para el mezclador EVR.                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



