---
description: Compatibilidad de VMR con la aceleración de vídeo de DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Compatibilidad de VMR con la aceleración de vídeo de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f1998f5e55d7aa4d191ac2a312995db69d9e248349034e119ded8e99774c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696735"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Compatibilidad de VMR con la aceleración de vídeo de DirectX

La aceleración de vídeo de DirectX es una interfaz de programación de aplicaciones (API) y una interfaz de controlador de dispositivo (DDI) correspondiente para la aceleración de hardware del procesamiento de la descodización de vídeo digital, con compatibilidad con la combinación alfa para fines como la compatibilidad con subpictura de DVD. DirectX VA se documenta en el Windows DDK. La [**interfaz IAMVideoAccelerator,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) que proporciona acceso en modo de usuario a la funcionalidad va de DirectX en un dispositivo de hardware, se documenta en este SDK.

VMR admite [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)y su implementación es idéntica a la versión anterior de overlay Mixer excepto por una diferencia importante. El Mixer superposición garantiza que la salida se representa en una superficie superpuesta, mientras que vmr puede enviar la salida para su posterior procesamiento, por ejemplo, una operación 3D, o bien puede enviar la salida a una superficie fuera de pantalla que luego se divide en la superficie principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la aceleración de vídeo de DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



