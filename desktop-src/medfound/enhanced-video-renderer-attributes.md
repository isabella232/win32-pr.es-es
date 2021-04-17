---
description: Atributos EVR
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: Atributos EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508b036a7880c48e65d3c07a80ba5baaa5a52306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714909"
---
# <a name="evr-attributes"></a>Atributos EVR

Los siguientes atributos se pueden usar para configurar el representador de vídeo mejorado (EVR).



| Atributo                                                                                                         | Descripción                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | Permite que EVR llame por lotes a la IDirect3DDevice9 de Microsoft Direct3D **::P método reenviado** .                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | Permite que el EVR mejore el rendimiento mediante el desentrelazado de Bob.                                                        |
| [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)                                     | Permite que el EVR mejore el rendimiento omitiendo el segundo campo de cada fotograma entrelazado.                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | Permite que el EVR limite su salida para que coincida con el ancho de banda de GPU.                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | Permite que el EVR mezcle el vídeo dentro de un rectángulo más pequeño que el rectángulo de salida y, a continuación, escalar el resultado. |
| [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)                                                           | Obliga al EVR a procesar por lotes las llamadas a **IDirect3D9Device::P método reenviado** .                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | Obliga a EVR a usar el desentrelazado de Bob.                                                                                 |
| [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)                                                 | Obliga al EVR a omitir el segundo campo de cada fotograma entrelazado.                                                       |
| [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)                                                             | Fuerza al EVR a mezclar el vídeo dentro de un rectángulo menor que el rectángulo de salida y, a continuación, escalar el resultado. |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | Fuerza a EVR a limitar su salida para que coincida con el ancho de banda de GPU.                                                               |
| [**MF \_ activar \_ \_ mezclador de vídeo personalizado \_ \_ activar**](mf-activate-custom-video-mixer-activate-attribute.md)         | Especifica un objeto de activación que crea un mezclador de vídeo personalizado para el representador de vídeo mejorado (EVR).                  |
| [**MF \_ activar \_ \_ mezclador de vídeo personalizado \_ \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID de un mezclador de vídeo personalizado para el EVR.                                                                               |
| [**MF \_ activar \_ \_ marcas de mezclador de vídeo personalizadas \_ \_**](mf-activate-custom-video-mixer-flags-attribute.md)               | Especifica cómo crear un mezclador personalizado para el EVR.                                                                      |
| [**MF \_ activar \_ el \_ presentador de vídeo personalizado \_ \_ activar**](mf-activate-custom-video-presenter-activate-attribute.md) | Especifica un objeto de activación que crea un presentador de vídeo personalizado para el EVR.                                        |
| [**MF \_ activar \_ \_ CLSID de \_ presentador de vídeo personalizado \_**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID de un presentador de vídeo personalizado para el EVR.                                                                           |
| [**MF \_ activar \_ \_ marcas de presentación de vídeo personalizadas \_ \_**](mf-activate-custom-video-presenter-flags-attribute.md)       | Especifica cómo crear un presentador personalizado para el EVR.                                                                  |
| [**\_ventana activar \_ vídeo de MF \_**](mf-activate-video-window-attribute.md)                                         | Identificador de la ventana de recorte de vídeo.                                                                                     |
| [**\_recuento \_ de \_ muestras \_ requerido de MF SA**](mf-sa-required-sample-count-attribute.md)                                  | Indica el número de búferes sin comprimir que el receptor de medios EVR requiere para el desentrelazado.                         |
| [**\_rectángulo de zoom de vídeo \_**](video-zoom-rect-attribute.md)                                                            | Especifica el rectángulo de zoom para el mezclador de EVR.                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



